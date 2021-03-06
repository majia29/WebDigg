## 网易杭研中台实践：建中台有可行方法论吗？  

> 原创：  
> 赵钰莹  
> 发布: AI前线  
> 发布日期: 2019-09-03  

![image](images/1909-wyhyztsjjztykxfflm-0.jpeg)
 作者 | 赵钰莹  编辑 | 陈思  **AI 前线导读：** 自 2006 年从浙大计算机专业博士毕业，汪源就加入了之前参与筹建、刚成立的网易杭州研究院，专注负责一件事：为集团互联网业务创新和发展打造一个支撑平台。按照今天的概念来看，整体上可以说汪源在做集团的创新中台，因此对中台这个概念有了深刻理解。本文中，InfoQ 对网易副总裁，网易杭州研究院执行院长汪源进行了独家采访，试图了解网易杭研的中台搭建背景及中台实践方法论。

**更多优质内容请关注微信公众号“AI 前线”（ID：ai-front）** 如何理解中台？

中台怎么理解？时至今日，这个问题已经被太多人回答过。不仅仅要理解中台，现在还要理解业务中台、数据中台、技术中台等各种名词。汪源表示，一个概念要跟相关概念对照才好理解。中台是组织的概念，是一类有别于前台和后台的组织。通常，前台指的是直接面对用户、客户、合作方等外部实体的业务部门，后台一般指 HR 等职能部门。此外，中台和平台经常被混为一谈。汪源表示，一个好的定义应该很好的将中台与前台、后台、平台区分开。

在汪源的定义中，中台是支持多个前台业务且具备业务属性的共性能力组织。基于此，中台不是前台而是支持前台，也不是后台因为后台不具备业务属性。中台和平台之间的区分在于平台不具备业务属性，也往往不是组织。

在此之前，汪源就曾通过 文章 表示：所有的中台都是业务中台。数据中台是一种特殊的业务中台，一般指以负责数据采集、数据集成、数据治理，指标体系和数据仓库统一建设等数据管理活动的组织。当前阶段，汪源认为不存在技术中台，现在业界所谓的技术中台其实都是云计算、AI 算法等技术平台，这些技术平台没有业务属性，做这些平台的人也不懂业务，称做中台是不合适的。

网易杭研中台实践

自 2006 年加入网易杭州研究院，汪源一直负责为集团互联网业务创新和发展打造一个支撑平台。因为集团把新业务的孵化基本都交给网易杭州研究院做，比如网易考拉、网易严选、网易云音乐、网易云阅读、网易云课堂、Lofter 等，都是从杭研走出去的。为了加速新业务的孵化和发展，网易杭州研究院考虑打造一个强劲的创新平台来支撑。

在当时的杭研内部，好几个业务在并行运行，包括网易博客、相册、POPO 等，而哪个能成、哪个不能成，谁也说不准。当时，网易相册是国内最大的在线相册，拥有数十亿照片，网易博客也仅次于新浪博客，拥有数十亿文章，由此产生的数据管理挑战非常大。考虑到网易杭州研究院得是铁打的营盘，业务很可能是流水的兵，汪源开始带领团队不断增强共享的专业能力，考虑将营盘打造地更好，让兵成长地更快，各方面的战斗力更强。这样，打胜仗的概率就会上升。

与此同时，网易杭州研究院的骨干统统是来自浙大计算机专业的工科男。工科男的思维就是追求体系化，极度讨厌重复建设。在这些背景下，网易杭州研究院走上了一条不断建立共享能力的发展之路，并将这些共享能力综合起来，形成一个强大的创新中台，提高创新速度和效率。

基于这样的思路，网易杭州研究院第一年专心解决海量数据管理的核心技术难题。2006 年 9 月 1 日，随着网易博客的正式发布而上线的 DDB、DFS 分别解决了分布式数据库和分布式文件存储的问题，当时在国内是最早的。当时做博客差不多 20 个人，做 DDB 等平台也有 15 个人，在基础技术上的投入按比例看可谓巨大。

2007 年，团队又投入做了 MapReduce 系统 NEMR、融合多维查询系统等。这几个系统在当时的环境下，基本上就把主要的技术挑战解决了。

既然技术上可以通过专职的团队做的很好，那么其他方面也应该可以。这样，杭研就走上了一条不断建立共享能力团队的发展之路，我们希望这些共享能力综合起来，能够形成一个强大的创新中台（当然之前没有中台这次词，叫平台），提高创新的速度和效率，提供成功率。

2007 到 2008 年，最早成立的非技术类共享能力团队是用户体验和软件质量，因为团队希望每一个产品的交互体验和质量都能过关。当然这很大程度上来自于老板的压力，这方面的问题一出很快就会被老板看到，用户体验和软件质量团队一直延续到今天。

2009 到 2010 年，团队主要做了数据挖掘、内容安全、移动研发。因为内容安全大量用到数据挖掘的算法，所以数据挖掘和内容安全这两个团队一开始是在一起的。内容安全这两年主要拼死啃一个硬骨头：邮箱反垃圾。后来通过机器学习算法比较好的解决了，直到今天邮箱反垃圾的核心算法还是杭研的团队在做。内容安全则在后来发展成了全集团的信息安全部。

2011 到 2014 年，团队建了项目管理、商业智能、运维部等，从原来偏技术开始走向管理和运营。项目管理部是 PMO 的概念，一方面培养并派出专业的项目经理到各个业务负责项目管理工作，确保研发项目的交付，另一方面这两年也开始主导研发效能工具的开发。商业智能部曾经负责了音乐、易信、教育等所有杭研体系业务的数字化运营分析工作。运维部负责了考拉、音乐、金融、新闻等业务的运维保障，包括 SA、DBA、PE 和运维平台研发、运维体系建设等职能。

2015 年，团队开始投入建设集团级用户中心。以统一的账号体系为基础，整合多业务的数据，实现用户标识的统一，并建立起规模较大、覆盖较全、准确率较高的用户标签体系。

在这个过程中，共享能力有很多自然而然就建成了中台。当然，整个团队要解决的问题也很多，比如技术挑战、保障用户体验和软件质量、保障信息安全、通过推荐或搜索提升业务 KPI、打通和建设用户标签数据、提升人均效能降低成本等。目前的重点主要是与网易考拉、网易严选、网易云音乐等合作共建业务和数据中台，以及持续强化用户中台。

技术与管理挑战

目前，网易绝大多数互联网业务都跑在该中台之上，偏职能和管理的主要有用户中心、用户体验设计中心、运维部、PMO 等。在整个研发过程中，技术上的挑战一直都存在。汪源表示，最早做分布式数据库和文件系统没有可行经验参考，虽然当时 Google 已经发表了 GFS、BigTable 等文章，但那样做投入太大，而当时的整个团队只有半年时间。再比如，团队 2009 年做邮箱反垃圾，当时贝叶斯网络这样的常规手段完全达不到团队的要求，最后，网易杭州研究院选择了大规模分布式数据挖掘算法才有效解决问题，这样的做法也没有前人经验可以参考。

总结下来，汪源表示，技术上的挑战很大一部分来自要准确选择开源技术，比如 2012 年做云计算是选择 KVM 还是 Xen、选择 OpenStack 还是 CloudStack；2015 年做容器是选择 Kubernetes 还是 Swarm 等。每一次，网易杭州研究院都选择了不成熟但架构设计合理、社区趋势好的技术，这让整个团队近十年没有出现过大的方向错误。当然，这也不是单纯的运气好，在这件事情上，团队也是吃过亏的。汪源透露，早期，整个团队在技术选型上也是犯过错误的，比如早期搜索选了 CLucene 而不是 Lucene。

除了选型上的抉择，技术挑战往往还来自于要用较少的人力创造出较大产出，比如 2012 年做云计算，整个团队 IaaS 和 PaaS 只有 60 多人，1 年时间就要上线。这时，汪源就必须做好总架构师的角色，认真梳理整体架构设计，不做任何重复或无效投入，同时有些系统必须逐步演进，不能一开始就追求理想化。在一些更大的组织中，公司可能会采用赛马机制让多个团队并行做，然后再 PK，但汪源表示，网易支撑不了这样的投入，必须追求尽可能一次性把事做对。

在管理上，困难主要来自于技术属性较弱的 PMO、推荐搜索、数据分析等专业能力部门，这些部门的发展存在很大的不稳定性，如果能力不能持续提升和沉淀，就可能导致部门分拆。汪源感叹：这么多年，分分合合都有。正是基于这些经历，汪源提出以能力组、技术平台和方法论为主的标准能力组织、包含专向组的胖中台组织、中台组织到平台组织的转化等中台组织的方法，以应对不同情况。

建设效果

在这个过程中，网易杭州研究院从零开始建设了集团的信息安全部，负责网络安全、内容安全、业务安全、系统安全等主要的安全工作。其中，内容安全方向除了邮箱，还服务于音乐、新闻、Lofter 等几乎所有互联网产品，不但提供算法和系统，还负责安全策略运营和人工审核。同时，作为网易云安全服务（易盾）对外输出，为中国互联网每天过滤超 10 亿内容。

以统一的账号体系为基础，整合多业务数据，实现用户标识的统一，并建立起规模较大、覆盖较全、准确率较高的用户标签体系。网易杭州研究院协助网易考拉和网易云音乐在在线业务中台建设上取得较好成果，需求响应时间缩短了一倍。在线业务中台建成之后，网易考拉日均应用部署次数达到 1374 次、网易云音乐达到 492 次，业务迭代演进效率基本符合预期。同时，软件产品质量也提升了 52%。目前，网易在线业务中台的支撑技术——网易轻舟微服务已经对外输出，应用于德邦快递、申万宏源、浙江大华、中国工商银行、百胜中国等企业。

此外，网易杭州研究院协助网易考拉在数据中台建设上取得了较好成果，指标数量经中台梳理减少了一半，极大缓解了指标重复、口径不一致等问题。数据产品指标覆盖率达到 100%，数据质量大幅提升到 99.8% 的 SLA，实现了 100% 自助取数，同时降低了 20% 的成本。作为网易数据中台的支撑技术，网易猛犸也已经实现对外输出，并成功应用在温氏股份、名创优品等企业。

早期，网易杭州研究院研发一款新产品需要至少 9 个月的时间才能上线，发版本至少还需要两周，同时也做不了几个。通过建设中台，网易杭州研究院研发一款全新的产品只需要两、三个月就能上线，且每天都可上线多个版本，同时并行开展的产品研发可以达到上百个。汪源表示，这说明创新中台整体可以大大提升业务创新和发展效率。

中台实践方法论

当初，网易杭州研究院迫于要并行发展多条业务线的压力，加上理工科厌恶重复建设的思维，不断的建设各种专业能力组织，从而走上了一条摸索建设中台的道路，再到后来一些业务发展大了，又支撑着各业务建中台。在这个过程中，有经验、有教训也有心得。

在汪源看来，一个标准的中台组织必须有一系列的可以共享的能力沉淀，这些能力沉淀要通过团队、技术和方法论三种方式。团队方面，就是一系列的能力组，比如对数据挖掘中台专业的 NLP、视觉算法和标准化的内容加工团队就是能力组，再比如对质量中台专业的性能测试、移动端兼容性测试等团队就是能力组。技术方面就是要尽可能的将能力和知识软件化、产品化，如项目管理部要主导研发效能工具等。方法论方面就是要形成流程、规范、check list、最佳实践等各种方法论。

一般来讲，技术和方法论都可以买到，但组织买不到。所以，最关键的是要对中台组织怎么构建有明确的方案，并下决心去推行。通常，企业需要做一些组织架构的调整，如果有平台组织存在则可以平台组织为基础，整合一些懂业务的人，否则可能得整合更多资源。技术上，绝不要重复造轮子；组织上，要根据情况在胖中台组织、标准中台组织、平台组织之间灵活切换，不要担心组织调整影响到了某些人，调整带来的重新分配对大多数人来说都是更好的去处。

中台和各前台业务团队应该是支撑和合作的关系，这两类团队需要一起制定工作规划，一起确定绩效目标，因为有一些绩效目标是中台和前台业务团队一起背。除此之外，中台团队应该有部分人员是专职对接和服务每个核心的前台业务，这些人应该和前台业务团队坐在一起，团建应该一起去，汪源称之为“专人就位”，这样才能塑造信任和默契。如果前台团建都不叫中台团队去，那这个中台就危险了。

对于前台业务团队来说，最大的变化是得放弃完全的控制权，承担一定风险，换回来的是更低成本、更高效率、更高质量的服务和更强的能力。

在人员组成上，外部招聘对构建中台团队往往很难，因为中台团队一要懂业务，二要得到前台业务的信任，所以最好是从内部培养和选拔，可以从平台团队选拔但此时要配置懂业务的人配合，也可以从业务线抽调。中台团队的核心管理层要求具备业务经验和敏感度，因为这类人一要懂业务；二要有强的执行力、目标感和沟通能力，因为中台要跨部门推动工作落地；三要有强的逻辑分析能力，因为中台工作比较抽象，要提炼。

建设中台是一个非常复杂的过程，这不是简单的决策而是战略层面的调整。汪源在采访最后表示：“建设中台是比较复杂的，所以首先要判断是否有必要，比如是否觉得核心能力确实存在较大短板；跨业务或项目的共享做得不够；需求变化快且多；数据经常出错或者不一致等。如果需求不大，时机不成熟，可以再观察观察。”

中台可以在很多层次建设，可以是公司级的，也可以是事业群、事业部甚至更低层次。网易杭州研究院建的中台可以说是企业级的，但支持考拉等业务建的中台都是事业部级的。一般而言，事业部的业务发展到一定阶段，都可以建中台，也相对比较好建；企业级的中台就要看公司战略和业务状况，建设难度也更大。

如果一个公司的业务集中在一个行业，比如都是零售业，这样建设公司级中台的基础就比较好，但这样的中台对新业务可能没有什么价值。如果公司期望多元化发展，汪源认为，可以参考网易杭州研究院这样的创新中台型组织。如果不属于上述任何一种情况，那么可以在各个事业部建各自的中台，这时公司可以考虑建设一个共享中台支撑技术研发团队，支持各事业部建中台，因为中台的形式和支撑技术是比较统一的。

对于确实规划建设中台的，汪源还是建议要从组织、支撑技术和方法论三个方面都要做好准备，这方面的内容很多，很难给出几条简单的建议就能起到很大的作用。建议第一步先做自主研究，对建设中台有一个总体的理解和把握；第二步找有建设经验的团队学习。

结束语

汪源始终认为，要把营盘打造的好一点，把能力打造的好一点，以便组织能更快速的响应变化，是对的方向。未来，网易杭州研究院将在容器化、在线离线业务混部、Service Mesh、单元化多活、数据中台技术体系、全面 EC 存储等基础技术领域下功夫，这也将是整个团队接下来两年的核心方向，目前已经有一定基础，接下来两年的目标就是全面应用。

**嘉宾介绍：**

汪源，网易副总裁，网易杭州研究院执行院长。2006 年获浙江大学计算机专业博士学位，之后加入网易公司。现作为网易杭州研究院执行院长，全面负责网易集团公共技术支撑工作与云计算、大数据业务，主要包括云计算与服务端架构、前端技术、大数据挖掘分析、信息安全、多媒体、运维、质量保障等方向，个人公众号“冷技术热思考”（ID：gh\_eb8c77c9a83b）。

原文链接：

https://www.infoq.cn/article/DKOKJiD3i7rV1HjxXZqy

