## Dubbo 整合 Pinpoint 做分布式服务请求跟踪  

> 作者: 搜云库技术团队  
> 发布日期: 2018-07-26  

在使用Dubbo进行服务化或者整合应用后，假设某个服务后台日志显示有异常，这个服务又被多个应用调用的情况下，我们通常很难判断是哪个应用调用的，问题的起因是什么，因此我们需要一套分布式跟踪系统来快速定位问题，Pinpoint可以帮助我们快速定位问题（当然，解决方案也不止这一种）。

### 什么是Pinpoint

摘自[Pinpoint学习笔记](https://skyao.gitbooks.io/learning-pinpoint)

<https://skyao.gitbooks.io/learning-pinpoint>

[Pinpoint](https://github.com/naver/pinpoint)是一个开源的 APM \(Application Performance Management/应用性能管理\)工具，用于基于java的大规模分布式系统。 仿照Google Dapper，Pinpoint通过跟踪分布式应用之间的调用来提供解决方案，以帮助分析系统的总体结构和内部模块之间如何相互联系。

> 注：对于各个模块之间的通讯英文原文中用的是transaction一词，但是我觉得如果翻译为"事务"容易引起误解，所以替换为"交互"或者"调用"这种比较直白的字眼。

Pinpoint是一个分析大型分布式系统的平台，提供解决方案来处理海量跟踪数据。2012年七月开始开发，2015年1月9日作为开源项目启动。

#### 服务器地图

ServerMap

通过可视化分布式系统的模块和他们之间的相互联系来理解系统拓扑。点击某个节点会展示这个模块的详情，比如它当前的状态和请求数量。

#### 实时活动线程图表

Realtime Active Thread Chart

实时监控应用内部的活动线程。

#### 请求/应答分布图表

Request/Response Scatter Chart

长期可视化请求数量和应答模式来定位潜在问题。通过在图表上拉拽可以选择请求查看更多的详细信息。

#### 调用栈

CallStack

在分布式环境中为每个调用生成代码级别的可视图，在单个视图中定位瓶颈和失败点。

#### 巡查

Inspector

查看应用上的其他详细信息，比如CPU使用率，内存/垃圾回收，TPS，和JVM参数。

#### 支持模块

* JDK 6+
* Tomcat 6 / 7 / 8，Jetty 8/9，JBoss EAP 6，Resin 4，Websphere 6 / 7 / 8，Vertx 3.3 / 3.4 / 3.5
* Spring，Spring Boot（嵌入式Tomcat，Jetty）
* Apache HTTP Client 3.x / 4.x，JDK HttpConnector，GoogleHttpClient，OkHttpClient，NingAsyncHttpClient
* Thrift Client，Thrift Service，DUBBO PROVIDER，DUBBO CONSUMER
* ActiveMQ，RabbitMQ
* MySQL，Oracle，MSSQL，CUBRID，POSTGRESQL，MARIA
* Arcus，Memcached，Redis，CASSANDRA
* iBATIS，MyBatis
* DBCP，DBCP2，HIKARICP
* gson，Jackson，Json Lib
* log4j，Logback

### 部署

**本次基础环境搭建我就不讲了** ，如不会，请自行搜索或者参考我博客文章<https://www.souyunku.com>

* 说下我的测试环境：hadoop-2.7.4 集群，hbase-1.3.1 集群，zookeeper-3.4.9 单机，一共四台机器
* 为避免部分端口不通等可疑问题, 建议关闭防火墙

#### 下载

进入GitHub 找到需要的版本：<https://github.com/naver/pinpoint/releases>

```
wget https://github.com/naver/pinpoint/releases/download/1.7.3/pinpoint-agent-1.7.3.tar.gz
wget https://github.com/naver/pinpoint/releases/download/1.7.3/pinpoint-collector-1.7.3.war
wget https://github.com/naver/pinpoint/releases/download/1.7.3/pinpoint-web-1.7.3.war

wget https://mirrors.tuna.tsinghua.edu.cn/apache/hbase/1.4.5/hbase-1.4.5-bin.tar.gz
```

#### 准备环境

1. 配置 JDK 环境 \(笔者使用 Oracle 1.8, openJdk 可以\)
2. 搭建 Zookeeper 环境
3. 搭建 Hbase \(单节点即可\)
4. 在 Hbase/bin 下执行 `./hbase shell hbase-create.hbase` 创建相关存储结构
5. 准备 Tomcat 环境
6. 准备可分布式部署的项目用于测试

#### 修改 Pinpoint

**pinpoint-collector-1.7.3.war**

```
修改  WEB-INF\classes\hbase.properties 文件
hbase.client.host 设置为 hbase 所用的 zk 地址

修改 WEB-INF\classes\pinpoint-collector.properties 文件
cluster.zookeeper.address 修改为给 Pinpoint 准备的 zk 地址
```

**pinpoint-web-1.7.3.war**

```
修改  WEB-INF\classes\hbase.properties 文件
hbase.client.host 设置为 hbase 所用的 zk 地址

修改 WEB-INF\classes\pinpoint-web.properties 文件
cluster.zookeeper.address 修改为给 Pinpoint 准备的 zk 地址
```

#### 部署 collector 和 web

1. 将准备好的 tomcat 中 webapps 目录清空
2. 将上一步修好的两个 war 包放置到 webapps
3. 将 `pinpoint-web-1.7.3.war` 修改为 `ROOT.war`
4. 将 `pinpoint-collector-1.7.3.war` 修改为 `collector.war`
5. 启动 Tomcat

查看 tomcat/logs 下的日志, 注意观察有没有连接不到 2181 端口的日志, 如果有, 可能是 war 中的配置没有修改正确, 建议清空 tomcat 下 work、temp 文件夹后重试

#### 部署 agent

* 安装agent，不需要修改哪怕一行代码
* Pinpoint对性能的影响最小（资源使用量增加约3％）

1. 将 pinpoint-agent-1.7.3.tar.gz 解压,
2. 把 pinpoint.config 文件中 `profiler.collector.ip` 属性值修改为部署 collector 机器的主机名或 IP

> 注意： 每个项目所在的服务器都需要部署 agent

#### 准备Dubbo示例程序

我的测试项目：[https://github.com/souyunku/s...](https://github.com/souyunku/spring-boot-examples/tree/master/spring-boot-dubbo)

配置 `application.properties`，修改地址 `zookeeper.connect=127.0.0.1:2181` 为自己的zk

```
mvn clean package
```

#### 修改自己项目的启动参数

需要添加三个启动参数

```
-javaagent： 指向 agent 目录下的 pinpoint-bootstrap-1.7.3.jar
-Dpinpoint.agentId：设置全局唯一标示 ID
-Dpinpoint.applicationName： 设置项目的名称(如果同一项目部署两台实例,这两台的参数应该一致)
```

Tomcat 和 Jar 项目有不同的添加方式,可参考如下方式修改

**Tomcat**

找到 bin/catalina.sh 添加下面的代码

```
CATALINA_OPTS="$CATALINA_OPTS -javaagent:$AGENT_PATH/pinpoint-bootstrap-1.7.3.jar"
CATALINA_OPTS="$CATALINA_OPTS -Dpinpoint.agentId=tomcat1"
CATALINA_OPTS="$CATALINA_OPTS -Dpinpoint.applicationName=webcontroller"
```

**SpringBoot**

```
### DUBBO 提供者
java -javaagent:/opt/pinpoint-bootstrap-1.7.3.jar -Dpinpoint.agentId=dubbo-provider-1 -Dpinpoint.applicationName=dubbo-provider -jar dubbo-provider-1.0-SNAPSHOT.jar

### DUBBO 消费者
java -javaagent:/opt/pinpoint-bootstrap-1.7.3.jar -Dpinpoint.agentId=dubbo-consumer-1 -Dpinpoint.applicationName=dubbo-consumer -jar dubbo-consumer-1.0-SNAPSHOT.jar
```

在自己的项目添加完毕启动后,即可登录 web 后台查看集群的状态, 跟踪请求

#### 测试

访问消费方地址模拟用户请求

`http://localhost:8080/sayHello?name=souyunku`

##### 截图

**首页**
![image](images/1807-dubbozhpinpointzfbsfwqqgz-0.png)
**指定时间点的，选中区域的请求明细**
![image](https://static.segmentfault.com/v-5d8c9d24/global/img/squares.svg)
![image](images/1807-dubbozhpinpointzfbsfwqqgz-2.png)
**请求响应明细和系统拓扑**
![image](https://static.segmentfault.com/v-5d8c9d24/global/img/squares.svg)
**视图中定位瓶颈和失败点**
![image](https://static.segmentfault.com/v-5d8c9d24/global/img/squares.svg)
![image](images/1807-dubbozhpinpointzfbsfwqqgz-3.png)
**消费者机器的， CPU使用率，内存/垃圾回收，TPS，和JVM参数**
![image](https://static.segmentfault.com/v-5d8c9d24/global/img/squares.svg)
![image](https://static.segmentfault.com/v-5d8c9d24/global/img/squares.svg)

参考：

<https://segmentfault.com/a/1190000011290541>

<http://dubbo.apache.org/#!/blog/pinpoint.md?lang=en-us>

### Contact

* 作者：鹏磊
* 出处：<http://www.ymq.io/2018/07/26/Dubbo-Pinpoint>
* 版权归作者所有，转载请注明出处
* Wechat：关注公众号，搜云库，专注于开发技术的研究与知识分享

![image](https://static.segmentfault.com/v-5d8c9d24/global/img/squares.svg)
