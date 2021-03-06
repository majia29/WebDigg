## 深度学习CTR预估模型凭什么成为互联网增长的关键？  

> 作者: 王喆 ​  
> 发布日期: 2019 年 3 月 13 日  

![image](images/1903-sdxxctrygmxpsmcwhlwzcdgj-0.jpeg)

> 本文是王喆在 InfoQ 开设的原创技术专栏“深度学习 CTR 预估模型实践”的第一篇文章（以下“深度学习 CTR 预估模型实践”简称“深度 CTR 模型”）。回顾王喆老师过往精彩文章：[《重读 Youtube 深度学习推荐系统论文，字字珠玑，惊为神文》](https://mp.weixin.qq.com/s?__biz=MzU1NDA4NjU2MA==&mid=2247494669&idx=2&sn=b1ca666f647373b0de4be5da388e53bc&chksm=fbea55c2cc9ddcd4f909dd2ea65102d9e0637857dac813d35f71229d0c897a435077c987418f&scene=27#wechat_redirect)、[《YouTube 深度学习推荐系统的十大工程问题》](https://www.infoq.cn/article/SrjcfW5GrTwdrJ_8XFB7)。

开篇伊始，有两个问题是应该澄清的，一是该专栏的主题选择，二是该专栏的目标受众。

* **为什么着重讲深度 CTR 模型这个主题？** 除了跟我的计算广告、推荐系统的背景有关之外，更重要的是 CTR 预估模型以及 CTR 预估模型衍生出的泛效果预测的模型，已经成为了互联网当之无愧的“增长之心”。自 2012 年以来，站在 Yann LeCun、Geoffrey Hinton 和 Yoshua Bengio 等巨人肩膀上的 Alex Krizhevsky 凭借 AlexNet 一举引爆新一轮的深度学习浪潮以来，深度学习席卷各个计算机应用领域，作为广告、搜索、推荐业务核心的 CTR 预估模型也借助深度学习得到效果上的显著提升，成为几乎所有主流互联网公司的标准配置。

* **这个专栏希望哪些受众从中受益？** 我希望把专栏的受众分为两类，一是互联网行业相关方向，特别是广告、推荐、搜索领域的从业者，希望这些同学能够熟悉深度 CTR 模型的发展脉络，清楚每个关键模型的技术细节，进而能够在工作中应用甚至改进这些模型；二是有一定机器学习基础，想进入这个领域的爱好者、在校生。我会尽量用平实的语言从细节出发介绍每个 CTR 预估模型，希望大家能够从零开始构建深度 CTR 模型的知识体系。

对于互联网从业者来说，“ **增长** ”这个词就像是插在心中的一只矛，无时无刻不被其刺激和激励着。我对“增长”这个词的理解还是来源于上大学时实验室的一段经历。清华计算机系跟搜狗一直是长期的伙伴，因此实验室的师兄师姐也经常谈起与搜狗合作的项目，我一直记忆至今的一句话是“如果我们能把搜狗搜索引擎广告的点击率提升 1%，那就能为公司带来上千万的利润”。从那时，“点击率（Click Through Rate， CTR）”这个词深深的烙在我心中，可能也在潜意识中指引我走上计算广告工程师的职业道路。那么到底是怎样的一个指标能对公司的增长起到如此至关重要的效果，为什么 CTR 预估模型能够被称为互联网“增长之心”，下面我尝试用两个场景给出答案。

### 一、CTR 预估模型与计算广告的利润增长

CTR 预估模型在计算广告领域的关键地位来源于计算广告利润增长的需求。CTR 预估的准确与否，直接影响计算广告公司的收入。

假设我们是一个 DSP（Demand side platform）公司，需要对接第三方的流量资源，通过出价的方式竞得该流量，从而赢得这个广告曝光（impression）机会。

对于一个以效果为核心目标的中小广告主来说，往往会选择 CPC 的结算方式，也就是每带来一次点击，我为你支付 x 元。那么这时，CTR 模型的关键就体现出来了，因为只有拥有了准确的 CTR 模型，DSP 公司才能够正确的估计某次流量的成本价。

例如 CTR 预估模型预测某流量投放某广告的点击率是 0.5%（即 CTR=0.5%），广告主愿意为一次点击支付 1 元（即 CPC=1），那么我只有用少于 CPC\*CTR = 1 \* 0.5% = 0.005 元的价格竞得该流量，我才不会亏钱。如果 CTR 模型预测的 CTR 偏高，我将极可能以高于成本价的价格竞得该流量，这样的情况下，竞得越多这样的流量，公司的亏损也越大。另一方面，如果 CTR 模型预测的 CTR 过低，进而出价过低，很有可能损失大量竞得机会，导致客户的广告预算花不完，从而无法获得后续订单，也使公司利润受损。

因此，精准的 CTR 预估模型是计算广告系统的基础和核心，也是计算广告公司进行利润最大化的核心模块，所以说 CTR 预估模型是计算广告利润的增长之心丝毫不为过。

### 二、CTR 预估模型与推荐系统的用户使用时长增长

广义上来讲，计算广告和推荐系统的界限并不那么严格，比如淘宝的直通车广告，应该属于计算广告的范畴，但它又完全符合商品推荐的场景。这里我倾向于把一切跟“钱”直接相关的模型归为计算广告的范畴，把一切跟“用户体验”直接相关的模型归为推荐系统的范畴，虽然提高用户体验更本质的目标也是为了最终实现产品利润的增长，但这与计算广告时刻跟出价、转化率、投资回报等“钱”相关的模型还是有业务场景上的较大区别。

所谓提高“用户体验”，可以进一步做这样的解释——“推荐系统的优化目标应该是为了在不损害用户长期兴趣的基础上增加用户的使用时长”。以 YouTube 为例，其商业目标就是为了通过提高用户观看总时长，实现广告 inventory 的增长，进而增加公司利润。

实现这一目标的关键就在于预测用户 U（user）在某场景 C（context）下是否会观看某视频 V（video），以及观看该视频的观看时长是多少。这与计算广告中的 CTR 预估模型的区别仅在于将 A（ad）换成了 V（video），将构建 CTR=g\(A, U, C\) 的问题换成了构建 watch time=g（V, U, C）的问题。

事实上，YouTube 的工程师们在那篇著名的工程论文“Deep Neural Networks for YouTube Recommendations”也非常明确提出了改造 CTR 预估模型为预测用户时长的深度学习推荐模型的方法。由 CTR 预估模型衍生出的泛效果模型共同构成了驱动互利网场景下的用户增长、使用时长增长、转化效果增长等一系列的关键商业指标的增长之心。

### 三、深度学习 CTR 预估模型专栏的结构

专栏的正式内容将会分为两大部分，一是深度 CTR 模型的理论和技术发展脉络；二是深度 CTR 模型的系统设计和工程实践。

理论部分又将会分为“前深度学习时代“和”深度学习时代“两部分，这里仍要强调”前深度学习时代“CTR 预估模型的原因，是希望大家能够建立完整的学习框架，并打牢深度学习模型的理论基础，二者本质上是不可分割的。

而实践部分将分为”模型实现与部署“和”模型业界应用“两部分。能够掌握从”模型理论“到”模型实现“再到”上线部署“的一整套技术栈对于算法工程师来说是重要的。最终的”业界应用”部分包括了 Google，Airbnb，Facebook，Alibaba 等业界知名互利网公司的 CTR 预估模型的设计和应用案例，希望读者能够从应用中学到更多实践中应该注意的技术细节。

这是“深度学习 CTR 预估模型实践”的第一篇文章，期望你能从中受益。

### 作者介绍

**王喆** ，毕业于清华大学计算机系，现在美国最大的 smartTV 公司 Roku 任 senior machine learning engineer，曾任 hulu senior research SDE，7 年计算广告、推荐系统领域业界经验，相关专利 3 项，论文 7 篇，《机器学习实践指南》、《百面机器学习》作者之一。
