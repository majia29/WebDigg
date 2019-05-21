## Apache 基金会与 GitHub 均受美国出口法律约束，这对开发者有何影响？  

> 作者: 田晓旭  
> 发布日期: 2019 年 5 月 21 日  

![image](images/1905-apachejjhygithubjsmgckflyszdkfzyhyx-0.jpeg)

> 近日，不仅华为站在了风口浪尖，开源软件也被推到了台前。ASF 和 GitHub 官网先后更新了两则消息，消息的主旨如出一辙，旗下的项目、产品将受到美国出口法律的约束。

### ASF 受到美国出口法律约束

近日，ASF 官网出现了一则关于[ASF 产品出口控制状态](https://www.apache.org/licenses/exports/)的说明。文中指出，ASF 是位于美国的非盈利性慈善机构，所有产品通过公共论坛在线协作开发，并从美国的中央服务器发布，所以 Apache 项目的发行版需要遵循美国的出口法律和法规，并且随着产品和技术再出口到不同的地方依旧保持有效。

也就是说，出口、再出口、记录保存、ASF 产品捆绑和嵌入、加密报告和装运文件都需要遵循出口管制分类和相关限制信息。如果说得再明白一点就是，除非经美国政府正式授权，否则 ASF 软件、技术或数据不得直接或间接出口 / 再出口到受美国禁运或贸易制裁的地方。美国政府保留[出口禁止名单](http://www.bis.doc.gov/ComplianceAndEnforcement/ListsToCheck.htm)，包括但不限于[财政部的特别指定国民名单](http://www.treas.gov/offices/eotffc/ofac/sdn/index.html)和 [商务部的实体和被拒绝人名单](http://bxa.doc.gov/dpl/Default.shtm)。

划重点，美国时间 2019 年 5 月 15 日，特朗普签署了一份行政命令，宣布因为国家经济紧急状态，禁止企业使用对国家安全造成风险的外国制造设备。随后美国商务部声明，把华为及 70 个附属公司增列入出口管制的实体清单。

### GitHub 受到美国出口法律约束

不止 ASF，GitHub 官网也发消息称，“[GitHub.com](http://GitHub.com)、GitHub Enterprise Server 以及您上传到任一产品的信息可能受美国出口管制法律的约束，包括美国出口管理条例（EAR）。”

GitHub 官网发布的内容主要有以下几个要点：

* 根据 GitHub[的服务条款](https://help.github.com/en/articles/github-terms-of-service)，[用户只能按照适用法律访问和使用 GitHub.com](http://xn--GitHub-vt9ir51axnbjy4d6qgbsct54c8mn0ineae8265cgz3bl2rzn2a.com)，包括美国出口管制和制裁法律。根据美国和其他适用法律，特别指定国民名单和其它被拒绝、被封锁的人士禁止访问、[使用 GitHub.com](http://xn--GitHub-vt9i248w.com)，[用户不得代表此类各方使用 GitHub.com](http://xn--GitHub-vp7i60de0bt5xg65amugxjmm3tkp7aia5892ac48b.com)，包括受制裁国家 / 地区的政府。
* 根据美国财政部海外资产控制办公室（OFAC）发布的授权，Github 可允许受美国制裁的管辖区内或通常居住在管辖区内的用户访问某些 Github.com 服务。在访问 GitHub 服务时，这些管辖区内的人员和居民不得使用 IP 代理、VPN 或其他方法来伪装其位置，并且只能使用 GitHub 进行非商业的个人通信。
* GitHub Enterprise Server 不得出售、出口或再出口到清单中的国家，目前清单中已经包含古巴、伊朗、朝鲜、苏丹与叙利亚。

### 对开发者有何影响

在听到 ASF 和 GitHub 均受到美国出口法律约束时，很多技术人担心国内的开源项目也将迎来“至暗时刻”。那么，这两则消息到底真正约束的是什么？对于中国开发者来说，有什么影响？是否有比较好的应对措施呢？

ASF 到底限制了什么？知乎网友李道兵分析称：“只是 ASF 提供的服务受到了美国法律的限制，例如会员服务、下载服务、网站服务等。”而 ASF 在官网发表的文章指出，公开可用软件只有 ECCN 为 5D002 或 5D992 时才会受到 EAR 约束。

至于 GitHub，首先中国还没有被加入到清单中，还有缓冲时间。其次，主要受影响的是 GitHub 企业版，但是大多数企业在采购之后，都是在企业内部部署使用。最后，目前只有 ERA 限制的加密技术不可出口，其它开源软件项目很难被限制。

面对这些限制，开发者应该如何破解难题呢？根据李道兵的分析，想要解决限制的问题也不难，“用户只是不能从 ASF 网站下载软件，但是可以从任何发行版、镜像站或者其它能够获取到软件的地方（包括从你的朋友手上拷贝一份）去下载。而且受到 License 的保障，用户仍可以继续使用、修改、分发软件。如果该软件更换了不自由的软件协议，那么用户还可以继续使用比较自由的老版本。”

那么这是不是意味着美国这一举措毫无“攻击力”呢？当然不是，这一举措还是有很多隐忧的，例如，美国 ERA 条款中是否会增加更多的技术，如果通讯、大数据等相关技术被限制的话，那么对于中国企业和开发者也会有很多影响。另外，还有人担心编程语言是否会受到限制，毕竟像 Java 等各大语言的核心都在美国。

附 ASF 产品分类矩阵：

[Apache Accumulo Project](http://accumulo.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Accumulo Project development 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/accumulo.git), [Bouncy Castle](http://www.bouncycastle.org/download/bcmail-jdk15-137.tar.gz)
1.6.0 and on 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/accumulo.git), [Bouncy Castle](http://www.bouncycastle.org/download/bcmail-jdk15-137.tar.gz)
1.5.x 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/accumulo.git)
[Apache ActiveMQ Project](http://activemq.apache.org/)
Product Name Versions ECCN Controlled Source
Apache ActiveMQ development 5D002 [ASF](http://svn.apache.org/repos/asf/activemq/)
4.1 and later 5D002 [ASF](http://archive.apache.org/dist/activemq/apache-activemq)
Apache Camel development 5D002 [ASF](http://svn.apache.org/repos/asf/activemq/camel)
1.0.0 and later 5D002 [ASF](http://archive.apache.org/dist/activemq/apache-camel)
[Apache Ant Project](http://ant.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Ant development 5D002 [ASF](http://svn.apache.org/repos/asf/ant/core/)
1.1 and later 5D002 [ASF](http://archive.apache.org/dist/ant/)
Apache Ivy development 5D002 [ASF](http://svn.apache.org/repos/asf/ant/ivy/)
2.0.0-alpha-\*-incubating 5D002 [ASF](http://people.apache.org/dist/incubator/ivy/)
2.0.0-alpha-\*-incubating-bin-with-deps 5D002 [ASF](http://people.apache.org/dist/incubator/ivy/), [JCraft, Inc.](http://www.jcraft.com/jsch/)
2.0.0-beta1-\* and later 5D002 [ASF](http://archive.apache.org/dist/ant/ivy/)
2.0.0-beta1-bin-with-deps and later 5D002 [ASF](http://archive.apache.org/dist/ant/ivy/), [JCraft, Inc.](http://www.jcraft.com/jsch/)
[Apache Cassandra Project](http://cassandra.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Cassandra development 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/cassandra.git), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html), [The OpenSSL Project](http://www.openssl.org/source/)
0.8 and later 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/cassandra.git), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
[Apache Cayenne Project](http://cayenne.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Cayenne development 5D002 [ASF](http://svn.apache.org/repos/asf/cayenne/main/trunk/cayenne-crypto/), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
3.2.M2 and later 5D002 [ASF](http://svn.apache.org/repos/asf/cayenne/main/trunk/cayenne-crypto/), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
[Apache Commons Project](http://commons.apache.org/sandbox/openpgp/)
Product Name Versions ECCN Controlled Source
Apache Commons Compress development 5D002 [ASF](http://svn.apache.org/repos/asf/commons/proper/compress/trunk/)
1.6 and later 5D002 [ASF](http://archive.apache.org/dist/commons/compress)
Apache Commons Crypto development 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/commons-crypto.git), [The OpenSSL Project](http://www.openssl.org/source/), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
1.0.0 and later 5D002 [ASF](https://www.apache.org/dist/commons/crypto/), [The OpenSSL Project](http://www.openssl.org/source/), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
Apache Commons OpenPGP development 5D002 [ASF](http://svn.apache.org/repos/asf/commons/sandbox/openpgp/trunk/)
[Apache CouchDB Project](http://couchdb.apache.org/)
Product Name Versions ECCN Controlled Source
Apache CouchDB development 5D002 [ASF](http://svn.apache.org/repos/asf/couchdb/)
0.9.0 and later 5D002 [ASF](http://archive.apache.org/dist/couchdb/), [ibrowse](http://github.com/cmullaparthi/ibrowse/tree/master)
[Apache CXF Project](http://cxf.apache.org/)
Product Name Versions ECCN Controlled Source
Apache CXF development 5D002 [ASF](http://svn.apache.org/repos/asf/cxf/), [ASF](http://archive.apache.org/dist/xml/security/java-library/), [Bouncy Castle](ftp://ftp.bouncycastle.org/pub/release1.36/bcprov-jdk14-136.tar.gz)
all 2.\* 5D002 [ASF](http://people.apache.org/dist/cxf/), [ASF](http://archive.apache.org/dist/xml/security/java-library/), [Bouncy Castle](ftp://ftp.bouncycastle.org/pub/release1.36/bcprov-jdk14-136.tar.gz)
all 2.\*-incubating 5D002 [ASF](http://people.apache.org/dist/incubator/cxf/), [ASF](http://archive.apache.org/dist/xml/security/java-library/), [Bouncy Castle](ftp://ftp.bouncycastle.org/pub/release1.36/bcprov-jdk14-136.tar.gz)
[Apache DB Project](http://db.apache.org/derby/)
Product Name Versions ECCN Controlled Source
Apache Derby development 5D002 [ASF](http://svn.apache.org/repos/asf/db/derby/code/)
derby-10.\* 5D002 [ASF](http://archive.apache.org/dist/db/derby/)
Apache DdlUtils development 5D002 [ASF](http://svn.apache.org/repos/asf/db/ddlutils/)
ddlutils-1.0 and higher 5D002 [ASF](http://archive.apache.org/dist/db/ddlutils/)
Apache ObjectRelationalBridge - OJB development 5D002 [ASF](http://svn.apache.org/repos/asf/db/ojb/)
ojb-1.0.0 and higher 5D002 [ASF](http://archive.apache.org/dist/db/ojb/)
Apache Torque development 5D002 [ASF](http://svn.apache.org/repos/asf/db/torque/)
torque-3.1 and later 5D002 [ASF](http://archive.apache.org/dist/db/torque/)
[Apache Directory Project](http://directory.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Directory Server development 5D002 [ASF](http://svn.apache.org/repos/asf/directory/apacheds)
1.0 and later 5D002 [ASF](http://archive.apache.org/dist/directory/apacheds)
1.5 and later 5D002 [ASF](http://archive.apache.org/dist/directory/apacheds), [Bouncy Castle](http://www.bouncycastle.org/download/bcprov-jdk15-136.tar.gz)
Apache Directory Studio 1.2 and later 5D002 [ASF](http://svn.apache.org/repos/asf/directory/studio), [Bouncy Castle](http://www.bouncycastle.org/download/bcprov-jdk15-136.tar.gz)
[Apache Drill](http://drill.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Drill 1.2 and later 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/drill.git), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html), [The Eclipse Foundation](http://eclipse.org/jetty), [The Cyrus SASL project](https://www.cyrusimap.org/sasl/), [MIT](http://web.mit.edu/kerberos/), [The OpenSSL Project](http://www.openssl.org/source/)
[Apache Forrest Project](http://forrest.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Forrest development 5D002 [ASF](http://svn.apache.org/repos/asf/forrest/)
apache-forrest-0.6 and later 5D002 [ASF](http://archive.apache.org/dist/forrest/), [JCraft, Inc.](http://www.jcraft.com/jsch/)
[Apache Geode Project](http://geode.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Geode development 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/geode.git), [ASF](https://git-wip-us.apache.org/repos/asf/geode-native.git), [ASF](https://git-wip-us.apache.org/repos/asf/geode-examples.git), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html), [The OpenSSL Project](http://www.openssl.org/source/)
all releases 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/geode.git), [ASF](https://git-wip-us.apache.org/repos/asf/geode-native.git), [ASF](https://git-wip-us.apache.org/repos/asf/geode-examples.git), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html), [The OpenSSL Project](http://www.openssl.org/source/)
[Apache Geronimo Project](http://geronimo.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Geronimo development 5D002 [ASF](http://svn.apache.org/repos/asf/geronimo/)
1.0 and later 5D002 [ASF](http://archive.apache.org/dist/geronimo/)
[Apache Hadoop Project](http://hadoop.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Hadoop development 5D002 [ASF](http://svn.apache.org/repos/asf/hadoop/)
17.0 and later 5D002 [ASF](http://archive.apache.org/dist/hadoop/)
[Apache Harmony Project](http://harmony.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Harmony development 5D002 [ASF](http://svn.apache.org/repos/asf/harmony/)
5.0M1 and later 5D002 [ASF](http://archive.apache.org/dist/harmony/), [Bouncy Castle](http://www.bouncycastle.org/download/bcmail-jdk15-137.tar.gz)
[Apache HAWQ \(incubating\) Project](http://hawq.incubator.apache.org/)
Product Name Versions ECCN Controlled Source
Apache HAWQ \(incubating\) Project development 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/incubator-hawq.git)
[Apache HttpComponents Project](http://hc.apache.org/)
Product Name Versions ECCN Controlled Source
Apache HttpComponents Core development 5D002 [ASF](http://svn.apache.org/repos/asf/httpcomponents/httpcore/)
4.0 and later 5D002 [ASF](http://archive.apache.org/dist/httpcomponents/httpcore/)
Apache HttpComponents Client development 5D002 [ASF](http://svn.apache.org/repos/asf/httpcomponents/httpclient/)
4.0 and later 5D002 [ASF](http://archive.apache.org/dist/httpcomponents/httpclient/)
1.x, 2.x, 3.x 5D002 [ASF](http://archive.apache.org/dist/httpcomponents/commons-httpclient/)
[Apache HTTP Server Project](http://httpd.apache.org/)
Product Name Versions ECCN Controlled Source
Apache HTTP Server development 5D002 [ASF](http://svn.apache.org/repos/asf/httpd/)
apache\_1.3.x n/a
httpd-2.0.x 5D002 [ASF](http://archive.apache.org/dist/httpd/)
httpd-2.2.x 5D002 [ASF](http://archive.apache.org/dist/httpd/)
apache\_2.2.x-win32- _-openssl-_ 5D002 [ASF](http://archive.apache.org/dist/httpd/), [The OpenSSL Project](http://www.openssl.org/source/)
httpd-2.4.x 5D002 [ASF](http://archive.apache.org/dist/httpd/)
Apache Flood development 5D002 [ASF](http://svn.apache.org/repos/asf/httpd/test/flood/)
flood-0.4 5D002 [ASF](http://archive.apache.org/dist/httpd/flood/)
Apache libapreq development 5D002 [ASF](http://svn.apache.org/repos/asf/httpd/apreq/)
libapreq2 5D002 [ASF](http://archive.apache.org/dist/httpd/libapreq/)
libapreq n/a
Apache mod\_ftp development 5D002 [ASF](http://svn.apache.org/repos/asf/httpd/mod_ftp/)
Apache mod\_python development 5D002 [ASF](http://svn.apache.org/repos/asf/httpd/mod_python/)
mod\_python-\* 5D002 [ASF](http://archive.apache.org/dist/httpd/modpython/)
[Apache Incubator Project](http://incubator.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Abdera development 5D002 [ASF](http://svn.apache.org/repos/asf/incubator/abdera/java/)
all 0.\*-incubating 5D002 [ASF](http://people.apache.org/dist/incubator/abdera/), [ASF](http://archive.apache.org/dist/xml/security/java-library/), [Bouncy Castle](http://www.bouncycastle.org/download/bcmail-jdk15-134.tar.gz), [Bouncy Castle](http://www.bouncycastle.org/download/bcmail-jdk14-134.tar.gz)
Apache Airavata development 5D002 [ASF](http://svn.apache.org/repos/asf/incubator/airavata/), [Bouncy Castle](http://svn.apache.org/repos/asf/incubator/pdfbox/trunk/external/bcprov-jdk14-132.jar), [The Cryptix project](http://www.cryptix.org/), [Claymore Systems Puretls](http://www.rtfm.com/puretls/), [Globus Project](http://www.globus.org/security/overview.html)
Apache CloudStack development 5D002 [JaSypt.org](http://jasypt.svn.sourceforge.net/svnroot/jasypt/trunk), [Oracle](https://code.launchpad.net/~mysql/mysql-server/trunk), [Bouncy Castle](http://www.bouncycastle.org/download/), [ASF](http://svn.apache.org/repos/asf/webservices/wss4j/trunk/), [OpenSwan.org](http://git.openswan.org/openswan.git), [JCraft, Inc.](http://www.jcraft.com/jsch/), [ASF](http://git-wip-us.apache.org/repos/asf/incubator-cloudstack.git)
Apache Impala development 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/incubator-impala.git)
2.7.0 and later 5D002 [ASF](http://archive.apache.org/dist/incubator/impala)
Apache NiFi development 5D002 [JaSypt.org](http://jasypt.svn.sourceforge.net/svnroot/jasypt/trunk), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html), [Bouncy Castle](http://www.bouncycastle.org/download/), [JCraft, Inc.](http://www.jcraft.com/jsch/), [ASF](http://git-wip-us.apache.org/repos/asf/incubator-nifi.git)
0.0.1-incubating and later 5D002 [JaSypt.org](http://jasypt.svn.sourceforge.net/svnroot/jasypt/trunk), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html), [Bouncy Castle](http://www.bouncycastle.org/download/), [JCraft, Inc.](http://www.jcraft.com/jsch/), [ASF](http://git-wip-us.apache.org/repos/asf/incubator-nifi.git)
Apache PDFBox development 5D002 [ASF](http://svn.apache.org/repos/asf/incubator/pdfbox/trunk/), [Bouncy Castle](http://svn.apache.org/repos/asf/incubator/pdfbox/trunk/external/bcprov-jdk14-132.jar), [Bouncy Castle](http://svn.apache.org/repos/asf/incubator/pdfbox/trunk/external/bcmail-jdk14-132.jar)
Apache Pirk development 5D002 [ASF](https://git1-us-west.apache.org/repos/asf?p=incubator-pirk.git)
0.1.0-incubating and later 5D002 [ASF](https://dist.apache.org/repos/dist/dev/incubator/pirk/)
Apache Pulsar development 5D002 [ASF](https://github.com/apache/incubator-pulsar), [Bouncy Castle](ftp://ftp.bouncycastle.org/pub/release1.55/bcprov-jdk15on-155.jar)
1.20-incubating and greater 5D002 [ASF](https://github.com/apache/incubator-pulsar), [Bouncy Castle](ftp://ftp.bouncycastle.org/pub/release1.55/bcprov-jdk15on-155.jar)
Apache Shindig development 5D002 [ASF](http://svn.apache.org/repos/asf/incubator/shindig/)
Apache Slider development 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/incubator-slider.git), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html), [The Eclipse Foundation](http://eclipse.org/jetty)
0.30-incubating 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/incubator-slider.git), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
0.40-incubating and later 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/incubator-slider.git), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html), [The Eclipse Foundation](http://eclipse.org/jetty)
Apache Taverna development 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/incubator-taverna-language.git), [ASF](https://git-wip-us.apache.org/repos/asf/incubator-taverna-osgi.git), [ASF](https://git-wip-us.apache.org/repos/asf/incubator-taverna-engine.git), [ASF](https://git-wip-us.apache.org/repos/asf/incubator-taverna-common-activities.git), [ASF](https://git-wip-us.apache.org/repos/asf/incubator-taverna-commandline.git), [ASF](https://git-wip-us.apache.org/repos/asf/incubator-taverna-server.git), [ASF](https://git-wip-us.apache.org/repos/asf/incubator-taverna-workbench.git), [ASF](https://git-wip-us.apache.org/repos/asf/incubator-taverna-workbench-common-activities.git), [ASF](https://git-wip-us.apache.org/repos/asf/incubator-taverna-workbench-product.git), [ASF](https://git-wip-us.apache.org/repos/asf/incubator-taverna-plugin-component.git), [ASF](https://git-wip-us.apache.org/repos/asf/incubator-taverna-plugin-bioinformatics.git), [ASF](https://git-wip-us.apache.org/repos/asf/incubator-taverna-plugin-gis.git), [ASF](https://git-wip-us.apache.org/repos/asf/incubator-taverna-mobile.git), [ASF](https://git-wip-us.apache.org/repos/asf/incubator-taverna-databundle-viewer.git), [Bouncy Castle](http://bouncycastle.org/download/bcprov-jdk15on-154.tar.gz), [The Eclipse Foundation](http://eclipse.org/jetty), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html), [ASF](http://www.apache.org/dist/santuario/java-library/), [ASF](http://svn.apache.org/viewvc/santuario/xml-security-java/branches/1.5.x-fixes/), [ASF](http://people.apache.org/dist/cxf/), [ASF](http://archive.apache.org/dist/xml/security/java-library/), [ASF](http://archive.apache.org/dist/db/derby/), [Dropbox](https://www.dropbox.com/developers-v1/core/sdks/android), [Google](https://android.googlesource.com/), [Ruby Programming Language](https://github.com/ruby/openssl), [The OpenSSL Project](http://www.openssl.org/source/)
all releases 5D002 [ASF](https://archive.apache.org/dist/incubator/taverna/), [Bouncy Castle](http://bouncycastle.org/download/bcprov-jdk15on-154.tar.gz), [The Eclipse Foundation](http://eclipse.org/jetty), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html), [ASF](http://www.apache.org/dist/santuario/java-library/), [ASF](http://svn.apache.org/viewvc/santuario/xml-security-java/branches/1.5.x-fixes/), [ASF](http://people.apache.org/dist/cxf/), [ASF](http://archive.apache.org/dist/xml/security/java-library/), [ASF](http://archive.apache.org/dist/db/derby/), [Dropbox](https://www.dropbox.com/developers-v1/core/sdks/android), [Google](https://android.googlesource.com/), [Ruby Programming Language](https://github.com/ruby/openssl), [The OpenSSL Project](http://www.openssl.org/source/)
Apache Trafodion development 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/incubator-trafodion.git), [The OpenSSL Project](http://www.openssl.org/source/), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
all releases 5D002 [ASF](https://archive.apache.org/dist/incubator/trafodion/), [The OpenSSL Project](http://www.openssl.org/source/), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
Apache Whirr development 5D002 [ASF](http://svn.apache.org/repos/asf/incubator/whirr)
all 0.\*-incubating 5D002 [ASF](http://archive.apache.org/dist/incubator/whirr/), [Bouncy Castle](http://www.bouncycastle.org/download/bcmail-jdk14-129.tar.gz), [JCraft, Inc.](http://www.jcraft.com/jsch/), [Not-Yet-Commons-SSL](http://juliusdavies.ca/commons-ssl/)
[Apache Jakarta JMeter Project](http://jakarta.apache.org/jmeter)
Product Name Versions ECCN Controlled Source
Apache Jakarta JMeter 1.0 and later 5D002 [ASF](http://svn.apache.org/repos/asf/jakarta/jmeter/)
[Apache JAMES Project](http://james.apache.org/)
Product Name Versions ECCN Controlled Source
Apache JAMES Server development 5D002 [ASF](http://svn.apache.org/repos/asf/james/server/), [Bouncy Castle](http://www.bouncycastle.org/download/bcmail-jdk14-129.tar.gz)
2.3.0 and later 5D002 [ASF](http://archive.apache.org/dist/james/server/source/), [Bouncy Castle](http://www.bouncycastle.org/download/bcmail-jdk14-129.tar.gz)
Apache JAMES jDKIM 0.1 and later 5D002 [ASF](http://svn.apache.org/repos/asf/james/jdkim/), [Not-Yet-Commons-SSL](http://juliusdavies.ca/commons-ssl/)
Apache JAMES Mailet Crypto 0.1 and later 5D002 [ASF](http://svn.apache.org/repos/asf/james/mailet/trunk/crypto/), [Bouncy Castle](http://www.bouncycastle.org/download/bcmail-jdk16-146.jar)
Apache JAMES Mime4J 0.4 and later 5D002 [ASF](http://svn.apache.org/repos/asf/james/mime4j/)
[Apache Jena](http://jena.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Jena \(distribution\) development 5D002 [ASF](https://repository.apache.org/content/repositories/snapshots/org/apache/jena/)
binary distribution 5D002 [ASF](http://archive.apache.org/dist/jena/), [ASF](https://repository.apache.org/content/repositories/releases/org/apache/jena/)
[Apache Kafka Project](https://kafka.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Kafka development 5D002 [ASF](https://gitbox.apache.org/repos/asf?p=kafka.git), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
0.10.2 and later 5D002 [ASF](https://gitbox.apache.org/repos/asf?p=kafka.git), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
0.9.0 and later 5D002 [ASF](https://gitbox.apache.org/repos/asf?p=kafka.git), [Oracle](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
[Apache Kudu Project](http://kudu.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Kudu development 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/kudu.git)
1.1.0 and later 5D002 [ASF](http://archive.apache.org/dist/kudu/)
[Apache Labs Project](http://labs.apache.org/)
Product Name Versions ECCN Controlled Source
Apache BaDCA development 5D002 [ASF](http://svn.apache.org/repos/asf/labs/badca/)
Apache Vysper development 5D002 [ASF](http://svn.apache.org/repos/asf/labs/vysper/), [Bouncy Castle](http://www.bouncycastle.org/download/bcprov-jdk15-135.tar.gz)
[Apache Lucene Project](http://lucene.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Nutch development 5D002 [ASF](http://svn.apache.org/repos/asf/lucene/nutch/trunk/)
0.7 and later 5D002 [ASF](http://www.apache.org/dist/lucene/nutch/), [PDFBox](http://sourceforge.net/project/showfiles.php?group_id=78314&package_id=79377&release_id=454954)
Apache Solr development 5D002 [ASF](http://svn.apache.org/repos/asf/lucene/solr/trunk/)
1.4 and later 5D002 [ASF](http://www.apache.org/dist/lucene/solr/), [Apache Tika](http://svn.apache.org/repos/asf/lucene/tika/trunk/)
Apache Tika development 5D002 [ASF](http://svn.apache.org/repos/asf/lucene/tika/trunk/)
0.2-incubating and later 5D002 [ASF](http://www.apache.org/dist/lucene/tika/), [Bouncy Castle](http://www.bouncycastle.org/download/bcprov-jdk14-136.tar.gz), [Bouncy Castle](http://www.bouncycastle.org/download/bcmail-jdk14-136.tar.gz)
[Apache MyFaces Project](http://myfaces.apache.org/)
Product Name Versions ECCN Controlled Source
Apache MyFaces development 5D002 [ASF](http://svn.apache.org/repos/asf/myfaces/)
1.1.2 and later 5D002 [ASF](http://archive.apache.org/dist/myfaces/)
[Apache Mynewt \(incubating\) Project](http://mynewt.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Mynewt development 5D002 [ARM mbed](https://git-wip-us.apache.org/repos/asf?p=incubator-mynewt-core.git;a=tree;f=crypto/mbedtls;h=d5f6a7013f36a68d25b9232769a273e990278477;hb=HEAD), [TinyCrypt](https://git-wip-us.apache.org/repos/asf?p=incubator-mynewt-core.git;a=tree;f=crypto/tinycrypt;h=13294d0db5cdf2b0e882839f8c204d7d2ddd3bd1;hb=HEAD), [PolarSSL](https://git-wip-us.apache.org/repos/asf?p=incubator-mynewt-core.git;a=tree;f=net/ip/lwip_base/src/netif/ppp/polarssl;h=47a41b927b1faff57e562b0dac21c82c040e8025;hb=HEAD)
[Apache Oltu Project](http://oltu.apache.org//)
Product Name Versions ECCN Controlled Source
Apache Oltu development 5D002 [ASF](http://svn.apache.org/repos/asf/oltu/)
[Apache Open For Business Project](http://ofbiz.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Open For Business development 5D002 [ASF](http://svn.apache.org/repos/asf/ofbiz/trunk/)
4.0 release branch 5D002 [ASF](http://svn.apache.org/repos/asf/ofbiz/branches/release4.0/)
[Apache OpenEJB Project](http://openejb.apache.org/)
Product Name Versions ECCN Controlled Source
Apache OpenEJB development 5D002 [ASF](http://svn.apache.org/repos/asf/openejb/)
1.0 and later 5D002 [ASF](http://archive.apache.org/dist/openejb/)
All 0.x n/a
[Apache Perl Project](http://perl.apache.org/)
Product Name Versions ECCN Controlled Source
mod\_perl Perl- _-win32-bin-_.exe 5D002 [ASF](http://archive.apache.org/dist/perl/win32-bin/), [The OpenSSL Project](http://www.openssl.org/source/)
[Apache POI Project](http://poi.apache.org/)
Product Name Versions ECCN Controlled Source
Apache POI development 5D002 [ASF](http://svn.apache.org/repos/asf/poi/)
3.5 and later 5D002 [ASF](http://archive.apache.org/dist/poi/)
[Apache Polygene Project](http://polygene.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Polygene development 5D002 [ASF](https://git-wip-us.apache.org/repos/asf?p=polygene-java.git;a=tree;hb=develop), [Bouncy Castle](https://www.apache.org/licenses/exports/www.bouncycastle.org/download/bcprov-jdk15on-156.tar.gz)
2.1 5D002 [ASF](https://git-wip-us.apache.org/repos/asf?p=polygene-java.git;a=tree;hb=a789141d5af7f9137dddb9bfc0f0e0af47ebec2d), [Bouncy Castle](https://www.apache.org/licenses/exports/www.bouncycastle.org/download/bcprov-jdk15on-152.tar.gz)
[Apache Shiro Project](http://shiro.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Shiro development 5D002 [ASF](http://svn.apache.org/repos/asf/shiro/)
1.1 and later 5D002 [ASF](http://archive.apache.org/dist/shiro/)
1.0 5D002 [ASF](http://www.apache.org/dist/incubator/shiro)
All 0.x n/a
[Apache ServiceMix Project](http://servicemix.apache.org/)
Product Name Versions ECCN Controlled Source
Apache ServiceMix 3.x development 5D002 [ASF](http://svn.apache.org/repos/asf/servicemix/smx3/trunk), [ASF](http://archive.apache.org/dist/xml/security/java-library/), [Bouncy Castle](ftp://ftp.bouncycastle.org/pub/release1.36/bcprov-jdk14-136.tar.gz)
All 3.x versions 5D002 [ASF](http://archive.apache.org/dist/servicemix/servicemix-3), [ASF](http://archive.apache.org/dist/xml/security/java-library/), [Bouncy Castle](ftp://ftp.bouncycastle.org/pub/release1.36/bcprov-jdk14-136.tar.gz)
Apache ServiceMix 4.x development 5D002 [ASF](http://svn.apache.org/repos/asf/servicemix/smx4/features/trunk)
4.0-m1 n/a
Apache ServiceMix NMR development 5D002 [ASF](http://svn.apache.org/repos/asf/servicemix/smx4/nmr/trunk)
1.0-m1, 1.0-m2 n/a
Apache ServiceMix Kernel development n/a
All 1.0 milestones n/a
[Apache Portable Runtime Project](http://apr.apache.org/)
Product Name Versions ECCN Controlled Source
APR development 5D002 [ASF](http://svn.apache.org/repos/asf/apr/apr/)
APR-Util development 5D002 [ASF](http://svn.apache.org/repos/asf/apr/apr-util/)
0.9.x, 1.2.x n/a
1.4.x and later 5D002 [ASF](http://svn.apache.org/repos/asf/apr/apr-util/)
[Apache Santuario Project](http://santuario.apache.org/)
Product Name Versions ECCN Controlled Source
Apache XML Security for Java development 5D002 [ASF](http://svn.apache.org/viewvc/santuario/xml-security-java/trunk/)
1.5.x 5D002 [ASF](http://svn.apache.org/viewvc/santuario/xml-security-java/branches/1.5.x-fixes/)
Apache XML Security for C++ development 5D002 [ASF](http://svn.apache.org/viewvc/santuario/xml-security-cpp/trunk/)
[Apache SpamAssassin Project](http://spamassassin.apache.org/)
Product Name Versions ECCN Controlled Source
Apache SpamAssassin development 5D002 [ASF](http://svn.apache.org/repos/asf/spamassassin), [The OpenSSL Project](http://www.openssl.org/source/), [Steffen Ullrich](http://search.cpan.org/dist/IO-Socket-SSL/)
3.0.x and later 5D002 [ASF](http://archive.apache.org/dist/spamassassin/), [The OpenSSL Project](http://www.openssl.org/source/), [Steffen Ullrich](http://search.cpan.org/dist/IO-Socket-SSL/)
[Apache Spark Project](https://spark.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Spark 2.2.0 through 2.3.x 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/commons-crypto.git), [Bouncy Castle](http://bouncycastle.org/download/bcprov-jdk15on-158.jar)
2.4.0 and later 5D002 [ASF](https://git-wip-us.apache.org/repos/asf/commons-crypto.git)
[Apache Tomcat Project](http://tomcat.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Tomcat development 5D002 [ASF](http://svn.apache.org/repos/asf/tomcat/)
3.x and later 5D002 [ASF](http://archive.apache.org/dist/tomcat/)
Apache Tomcat native connector development 5D002 [ASF](http://svn.apache.org/repos/asf/tomcat/connectors/), [The OpenSSL Project](http://www.openssl.org/source/)
1.x and later 5D002 [ASF](http://svn.apache.org/repos/asf/tomcat/connectors/), [The OpenSSL Project](http://www.openssl.org/source/)
[Apache UIMA Project](http://uima.apache.org/)
Product Name Versions ECCN Controlled Source
Apache UIMA-AS development 5D002 [ASF](http://svn.apache.org/repos/asf/incubator/uima/sandbox/trunk/uima-as)
all releases starting with 2.2.2-incubating 5D002 [ASF](http://people.apache.org/dist/incubator/uima/source/uima-as/)
Apache UIMA Addons development 5D002 [ASF](http://svn.apache.org/repos/asf/uima/addons/trunk)
2.3.0 and later 5D002 [ASF](http://svn.apache.org/repos/asf/uima/addons/trunk)
Apache UIMA Addon Tika Annotator development 5D002 [ASF](http://svn.apache.org/repos/asf/uima/addons/trunk/TikaAnnotator)
2.3.0 and later 5D002 [ASF](http://svn.apache.org/repos/asf/uima/addons/trunk/TikaAnnotator)
Apache UIMA-DUCC development 5D002 [ASF](http://svn.apache.org/repos/asf/uima/sandbox/uima-ducc)
all releases starting with 1.0 5D002 [ASF](http://archive.apache.org/dist/uima/ducc)
[Apache VCL Project](http://vcl.apache.org/)
Product Name Versions ECCN Controlled Source
Apache VCL development 5D002 [ASF](http://svn.apache.org/repos/asf/vcl/trunk/)
2.1 to 2.2.2 5D002 [ASF](http://archive.apache.org/dist/vcl/)
2.3 and later 5D002 [ASF](http://archive.apache.org/dist/vcl/), [phpseclib](https://github.com/phpseclib/phpseclib)
[Apache Web Services Project](http://ws.apache.org/)
Product Name Versions ECCN Controlled Source
Apache WSS4J development 5D002 [ASF](http://svn.apache.org/repos/asf/webservices/wss4j/trunk/), [Bouncy Castle](https://www.apache.org/licenses/exports/www.bouncycastle.org/download/bcprov-jdk15on-151.tar.gz), [ASF](http://www.apache.org/dist/santuario/java-library/)
1.6 5D002 [ASF](http://svn.apache.org/repos/asf/webservices/wss4j/branches/1_6_x-fixes/), [Bouncy Castle](https://www.apache.org/licenses/exports/www.bouncycastle.org/download/bcprov-jdk15on-151.tar.gz), [ASF](http://www.apache.org/dist/santuario/java-library/)
1.0 to 1.5 5D002 [ASF](http://archive.apache.org/dist/ws/wss4j/), [Bouncy Castle](http://www.bouncycastle.org/download/bcprov-jdk13-132.tar.gz), [Bouncy Castle](http://www.bouncycastle.org/download/bcmail-jdk15-132.tar.gz), [ASF](http://archive.apache.org/dist/santuario/java-library/)
Apache Rampart/Java development 5D002 [ASF](http://svn.apache.org/repos/asf/webservices/rampart/trunk/java), [Bouncy Castle](http://www.bouncycastle.org/download/bcprov-jdk13-132.tar.gz), [Bouncy Castle](http://www.bouncycastle.org/download/bcmail-jdk15-132.tar.gz), [Apache Santuario](http://xml.apache.org/security/dist/java-library/)
1.1 and later 5D002 [ASF](http://archive.apache.org/dist/ws/rampart/), [Bouncy Castle](http://www.bouncycastle.org/download/bcprov-jdk13-132.tar.gz), [Bouncy Castle](http://www.bouncycastle.org/download/bcmail-jdk15-132.tar.gz), [Apache Santuario](http://xml.apache.org/security/dist/java-library/)
Apache Rampart/C development 5D002 [ASF](http://svn.apache.org/repos/asf/webservices/rampart/trunk/c/), [The OpenSSL Project](http://www.openssl.org/source/)
0.09 and later 5D002 [ASF](http://archive.apache.org/dist/ws/rampart/c/), [The OpenSSL Project](http://www.openssl.org/source/)
Apache Synapse 1.0, 1.1, 1.1.1, 1.2, 2.0.0 5D002 [ASF](http://archive.apache.org/dist/synapse/), [Bouncy Castle](http://www.bouncycastle.org/download/bcprov-jdk13-132.tar.gz), [Bouncy Castle](http://www.bouncycastle.org/download/bcmail-jdk15-132.tar.gz), [Bouncy Castle](http://www.bouncycastle.org/download/bcprov-ext-jdk15-140.jar), [Bouncy Castle](http://www.bouncycastle.org/download/bcprov-jdk14-140.tar.gz), [Apache Santuario](http://xml.apache.org/security/dist/java-library/)
[Apache Synapse Project](http://synapse.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Synapse development 5D002 [ASF](http://svn.apache.org/repos/asf/synapse), [Bouncy Castle](http://www.bouncycastle.org/download/bcprov-jdk13-132.tar.gz), [Bouncy Castle](http://www.bouncycastle.org/download/bcmail-jdk15-132.tar.gz), [Bouncy Castle](http://www.bouncycastle.org/download/bcprov-ext-jdk15-140.jar), [Bouncy Castle](http://www.bouncycastle.org/download/bcprov-jdk14-140.tar.gz), [Apache Santuario](http://xml.apache.org/security/dist/java-library/)
1.1.1 and later 5D002 [ASF](http://archive.apache.org/dist/synapse/), [Bouncy Castle](http://www.bouncycastle.org/download/bcprov-jdk13-132.tar.gz), [Bouncy Castle](http://www.bouncycastle.org/download/bcmail-jdk15-132.tar.gz), [Apache Santuario](http://xml.apache.org/security/dist/java-library/)
[Apache Wicket Project](http://wicket.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Wicket 1.3, development 5D002 [ASF](http://svn.apache.org/repos/asf/wicket/)
[Apache MINA Project](http://mina.apache.org/)
Product Name Versions ECCN Controlled Source
Apache MINA development 5D002 [ASF](http://svn.apache.org/repos/asf/mina/trunk)
1.0, 1.1, 2.0 5D002 [ASF](http://archive.apache.org/dist/mina/)
Apache Vysper development 5D002 [ASF](http://svn.apache.org/repos/asf/mina/sandbox/vysper), [Bouncy Castle](http://www.bouncycastle.org/download/bcprov-jdk15-140.tar.gz)
Apache FtpServer development 5D002 [ASF](http://svn.apache.org/repos/asf/mina/ftpserver)
1.0 5D002 [ASF](http://archive.apache.org/dist/mina/ftpserver/)
Apache SSHD development 5D002 [ASF](http://svn.apache.org/repos/asf/mina/sshd), [Bouncy Castle](http://www.bouncycastle.org/download/bcprov-jdk15-140.tar.gz)
[Apache Wookie Project](http://wookie.apache.org/)
Product Name Versions ECCN Controlled Source
Apache Wookie development 5D002 [ASF](http://svn.apache.org/repos/asf/wookie/), [Apache Santuario](http://archive.apache.org/dist/santuario/java-library/)
0.13 and later 5D002 [ASF](http://archive.apache.org/dist/wookie/), [Apache Santuario](http://archive.apache.org/dist/santuario/java-library/)
