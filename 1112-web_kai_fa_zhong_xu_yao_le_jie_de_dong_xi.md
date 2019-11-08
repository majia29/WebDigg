## Web开发中需要了解的东西  

> 作者: 陈皓  
> 发布日期: 2011年12月07日  

在StackExchange上有人问了这样一个问题：[What should every programmer know about web development?](http://programmers.stackexchange.com/questions/46716/what-should-every-programmer-know-about-web-development)（关于Web开发，什么是所有程序员需要知道的？）里面给出的答案非常不错，所以，我翻译转载过来。 顺便说一下，StackExchange真是非常好，大家可以对同一个答案做贡献和修订，看看这个问题的[修订过程](http://programmers.stackexchange.com/posts/46760/revisions)你就知道了——专业的问答网站应该怎么去做。这就是我在这篇文章中也说过[真正的用户体验是什么样的](https://coolshell.cn/articles/5901.html "腾讯，竞争力 和 用户体验")。

好了，下面是正文（我对原文做了一些批注，也许不对或有误导，请大家指正）

下面的这些东西可能对于大多数人并不陌生，但是可能会有些东西你以前并没有看过，或是没有完全搞懂，甚至都没有听说过。（陈皓注：我相信当你看完这个列表后，你会觉得对于我国的Web开发有点弱了，还是那句话，表面上的东西永远是肤浅的）

#### **接口和用户体验**

* 小心浏览器的实现标准上的不一致，确信让你的网站能够适当地跨浏览器。至少，你的网站需要测试一下下面的浏览器：
* 最新的 [Gecko](http://en.wikipedia.org/wiki/Gecko_%28layout_engine%29) 引擎 \([Firefox](http://firefox.com/)\)，
* 一个 Webkit 引擎 \([Safari](http://www.apple.com/safari/), [Chrome](http://www.google.com/chrome), 或是其它的移动设备上的浏览器\)
*  [IE 浏览器](http://en.wikipedia.org/wiki/Internet_Explorer) \(测试IE的兼容性你可以使用微软IE的 [Application Compatibility VPC Images](http://www.microsoft.com/Downloads/details.aspx?FamilyID=21eabb90-958f-4b64-b5f1-73d0a413c8ef&displaylang=en)\)
*  [Opera](http://www.opera.com/) 浏览器。

最后，你可以使用一下[这个工具](http://www.browsershots.org/) 来看看你的网页在不同的浏览器下是怎么被显示出来的（陈皓注：这个工具就是以前本站介绍过的[在不同浏览器和平台上检查你的网站的兼容性](https://coolshell.cn/articles/757.html "如何检查网页浏览器的兼容性")）

* 多考虑一下人们是怎么来访问你的网站而不是那些主流的浏览器：手机，读屏软件和搜索引擎，例如：一些Accessibility的东西： [WAI](http://www.w3.org/WAI/) 和  [Section508](http://www.section508.gov/), 移动设备开发：[MobiForge](http://mobiforge.com/).

* 部署Staging：怎么部署网站的更新而不会影响用户的访问。 [Ed Lucas的答案](http://programmers.stackexchange.com/questions/46716/what-should-a-developer-know-before-building-a-public-web-site/46738#46738) 可以让你了解一些（陈皓注：Ed说了一些如版本控制，自动化build，备份，回滚等机制）。

* 千万不要直接给用户显示不友好的错误信息。

* 千万不要把用户的邮件地址以明文显示出来，这样会被爬虫爬走并被让用户的邮箱被垃圾邮件搞死。

* 为用户的链接加上 `rel="nofollow"` 的属性以 [避免垃圾网站的干扰](http://en.wikipedia.org/wiki/Nofollow)。（陈皓注： **nofollow** 是HTML的一个属性，用于通知搜索引擎“这个链接所指向的网页非我所能控制，对其内容不予置评”，或者简单地说，该链接不是对目标网站或网页的“投票”，这样搜索引擎不会再访问这个链接。这个是用来减少一些特定垃圾页面对原网站的影响，从而可以改善搜索结果的质量，并且防止垃圾链接的蔓延。）

* [为网站建立一些的限制](http://www.codinghorror.com/blog/archives/001228.html) – 这个属于安全性的范畴。（陈皓注：比如你在Google注册邮箱时，你一口气注册超过两个以上的邮箱，gmail要求给你发短信或是给你打电话认证，比如Discuz论坛的会限制你发贴或是搜索的间隔时间等等，更多的网站会用CAPTCHA来确认是人为的操作。 这些限制都是为了防止垃圾和恶意攻击）

* 学习如何做 [Progressive Enhancement](http://en.wikipedia.org/wiki/Progressive_enhancement). （陈皓注：[Progressive Enhancement](http://en.wikipedia.org/wiki/Progressive_enhancement)是一个Web Design的理念，如：1）基础的内容和功能应该可以被所有的浏览器存取，2）页面布局的应该使用外部的CSS链接，3）Javascript也应该是外部链接还应该是 [unobtrusive](http://en.wikipedia.org/wiki/Unobtrusive_JavaScript "Unobtrusive JavaScript") 的，4）应该让用户可以设置他们的偏好）

* 如果POST成功，要[在POST方法后重定向网址](http://en.wikipedia.org/wiki/Post/Redirect/Get)，这样可以阻止用户通过刷新页面重复提交。

* 严重关注Accessibility。因为这是[法律上的需求](http://www.section508.gov/)（陈皓注：Section 508是美国的508法案，其是美国劳工复健法的改进，它是一部联邦法律，这个法律要求所有技术要考虑到残障人士的应用，如果某个大众信息传播网站，如果某些用户群体（如残疾人）浏览该网站获取信息时，如果他们无法正常获得所期望的信息（如无法正常浏览），那可以依据相关法规，可以对该网站依法起诉）。 [WAI-ARIA](http://www.w3.org/WAI/intro/aria) 为这方面的事提供很不错的资源.

#### **安全**

* 在网上有很多关于安全的文章，但是 [OWASP 开发指导](http://www.owasp.org/index.php/Category%3aOWASP_Guide_Project) 涵盖了几乎所有关于Web站点安全的东西。（陈皓注：OWASP\(开放Web应用安全项目- Open Web Application Security Project\)是一个开放的非营利性组织，目前全球有130个分会近万名会员，其主要目标是研议协助解决Web软体安全之标准、工具与技术文件，长期 致力于协助政府或企业了解并改善网页应用程式与网页服务的安全性。OWASP被视为Web应用安全领域的权威参考。2009年下列发布的美国国家和国际立法、标准、准则、委员会和行业实务守则参考引用了OWASP。美国联邦贸易委员会\(FTC\)强烈建议所有企业需遵循OWASP十大WEB弱点防护守则）

* 了解什么是 [SQL 注入攻击](http://en.wikipedia.org/wiki/SQL_injection) 并知道怎么阻止这种攻击。

* 永远不要相信用户的输入（包括Cookies，因为那也是用户的输入）

* 对用户的口令进行Hash，并使用salt，以防止Rainbow 攻击（陈皓注：Hash算法可用MD5或SHA1等，对口令使用salt的意思是，user 在设定密码时，system 产生另外一个random string\(salt\)。在datbase 存的​​是与salt + passwd 产的md5sum 及salt。 当要验证密码时就把user 输入的string 加上使用者的salt，产生md5s​​um 来比对。 理论上用salt 可以大幅度让密码更难破解，相同的密码除非刚好salt 相同，最后​​存在database 上的内容是不一样的。google一下md5+salt你可以看到很多文章。关于[Rainbow 攻击](http://en.wikipedia.org/wiki/Rainbow_table)，其意思是很像密码字典表，但不同的是，Rainbow Table存的是已经被Hash过的密码了，而且其查找密码的速度更快，这样可以让攻击非常快）。使用慢一点的Hash算法来保存口令，如 bcrypt \(被时间检证过了\) 或是 scrypt \(更强，但是也更新一些\) \([1](http://www.tarsnap.com/scrypt.html), [2](http://it.slashdot.org/comments.pl?sid=1987632&cid=35149842)\)。你可以阅读一下 [How To Safely Store A Password](http://codahale.com/how-to-safely-store-a-password/)（陈皓注：酷壳以前曾介绍过[bcrypt这个算法](https://coolshell.cn/articles/2078.html "如何防范密码被破解")，这里，我更建议我们应该让用户输入比较强的口令，比如Apple ID注册的过程需要用户输入超过8位，需要有大小写和数字的口令，或是做出类似于[这样的用户体验的东西](https://coolshell.cn/articles/3877.html "另类UX让你输入强口令")）。

* [不要试图自己去发明或创造一个自己的fancy的认证系统](http://stackoverflow.com/questions/1581610/how-can-i-store-my-users-passwords-safely/1581919#1581919)，你可能会忽略到一些不容易让你查觉的东西而导致你的站点被hack了。（陈皓注：我在[腾讯那坑爹的申诉系统](https://coolshell.cn/articles/5987.html "如何设计“找回用户帐号”功能")中说过这个事了，我说过这句话——“真正的安全系统是协同整个社会的安全系统做出来的一道安全长城，而不是什么都要自己搞”，当然，很遗憾不是所有的人都能看懂这个事，包括一些资深的人）

* 了解 [处理信用卡的一些规则 ](https://www.pcisecuritystandards.org/). \([这里也有一个问题你可以查看一下](http://stackoverflow.com/questions/51094/payment-processors-what-do-i-need-to-know-if-i-want-to-accept-credit-cards-on-m)\) （陈皓注：有两上vendor可以帮助你，一个是 [Authorize.Net](http://www.authorize.net/) 另一个是 [PayFlow Pro](https://www.paypal.com/cgi-bin/webscr?cmd=_payflow-pro-overview-outside)）

* 使用 [SSL](http://www.mozilla.org/projects/security/pki/nss/ssl/draft302.txt)/[HTTPS](http://en.wikipedia.org/wiki/Https) 来加密传输登录页面或是任可有敏感信息的页面，比如信用卡号等。

* 知道如何对付session 劫持。（陈皓注：请参看wikipedia的这[Session Hijacking](http://en.wikipedia.org/wiki/Session_hijacking)，）

* 避免 [跨站脚本攻击](http://en.wikipedia.org/wiki/Cross-site_scripting)\(XSS\)。（陈皓注：参看酷壳站前几天发的《[新浪微博的XSS攻击事件](https://coolshell.cn/articles/4914.html "新浪微博的XSS攻击")》）

* 避免 [跨站](http://en.wikipedia.org/wiki/Cross-site_request_forgery)[伪造](http://en.wikipedia.org/wiki/Cross-site_request_forgery)[请求攻击 cross site request forgeries](http://en.wikipedia.org/wiki/Cross-site_request_forgery) \(XSRF\).

* 保持你的系统里的所有软件更新到最新的patch。

* 确保你的数据库连接是安全的。

* 确保你能了解最新的攻击技术，以及你系统的脆弱处。

* 请读一下 [The Google Browser Security Handbook](http://code.google.com/p/browsersec/wiki/Main).

* 请读一下 [The Web Application Hacker’s Handbook](http://rads.stackoverflow.com/amzn/click/0470170778).

* （陈皓注：之前本站的“[一些资源](https://coolshell.cn/articles/5537.html "一些文章资源和趣闻")”提到过[Mozilla的安全编程规范](https://wiki.mozilla.org/WebAppSec/Secure_Coding_Guidelines)，还有Ruby on Rails的[Web安全的开发教程](http://guides.rubyonrails.org/security.html)）

#### **性能**

* 只要需要，请实现cache机制，了解并合理地使用 [HTTP caching](http://www.mnot.net/cache_docs/) 以及 [HTML5 Manifest](http://www.w3.org/TR/html5/offline.html).

* 优化页面 —— 不要使用20KB图片来平铺网页背景。（陈皓注：还有很多网页页面优化性的文章，你可以STFG – Search The Fucking Google一下。如果你要调试的话，你可以使用firebug或是chrome内置的开发人员的工具来查看网页装载的性能）
* 学习如何 [gzip/deflate 网页](http://developer.yahoo.com/performance/rules.html#gzip "gzip content") \([deflate 更好](http://stackoverflow.com/questions/1574168/gzip-vs-deflate-zlib-revisited)\).

* 把多个CSS文件和Javascript文件合并成一个，这样可以减少浏览器的网络连数，并且使用gzip压缩被反复用到的文件。

* 学习一下 [Yahoo Exceptional Performance](http://developer.yahoo.com/performance/) 这个网站上的东西，上面有很多非常不错的改善前端性能的指导，以及 [YSlow](http://developer.yahoo.com/yslow/) 这个工具。 [Google page speed](http://code.google.com/speed/page-speed/docs/rules_intro.html) 是另一个用来做性能采样的工具。这两个工具都需要安装 [Firebug](http://getfirebug.com/) 。

* 为那些小的图片使用 [CSS Image Sprites](http://alistapart.com/articles/sprites)，就像工具条一样。 \(参看 “最小化 HTTP 请求” \) （陈皓注：把所有的小图片合并成一个图片，然后用CSS把显示其中的一块，这样，这些小图片只用传输一次，酷壳的Wordpress样式的那个RSS订阅列表中的小图标就是这样做的）

* 繁忙的网络应该考虑[把网页的内容分开存放](http://developer.yahoo.com/performance/rules.html#split)在不同的域名下。（陈皓注：比如有专门的图片服务器——图片相当耗带宽，或是专门的Ajax服务器）

* 静态网页 \(如，图片，CSS，JavaScript，以及一些不需要访问cookies的网页\) 应该放在一个[不使用cookies](http://blog.stackoverflow.com/2009/08/a-few-speed-improvements/)的独立的域名下，因为所有在同一个域名或子域名下的cookie会被这个域名下的请求一同发送。另一个好的选择是使用 Content Delivery Network \(CDN\).

* 使用单个页面的HTTP请求数最小化。

* 为Javascript使用 [Google Closure Compiler](http://code.google.com/closure/compiler/) 或是 [其它压缩工具](http://developer.yahoo.com/yui/compressor/)（陈皓注：压缩Javascript代码可以让你的页面减少网络传输从而可以得到很快的喧染。注意，并不是所有的工具都可以正确压缩Javascript的，Google的这个工具甚至还可以帮你优化你的代码）

* 确认你的网站有一个 `favicon.ico` 文件放在网站的根下，如 `/favicon.ico`. [浏览器会自动请求这个文件](http://mathiasbynens.be/notes/rel-shortcut-icon)，就算这个图标文件没有在你的网页中明显说明，浏览器也会请求。如果你没有这个文件，就会出大量的404错误，这会消耗你的服务器带宽。（陈皓注：服务器返回404页面会比这个ico文件可能还大）

#### **SEO \(搜索引擎优化\)**

* 使用 “搜索引擎喜欢的” URL，如：使用 `example.com/pages/45-article-title` 而不是 `example.com/index.php?page=45 `\(陈皓注：这里的URL是说Wordpress的，后者是默认的\)

* 如果你的动态页面要使用 `#` ，那么请把其改成 `#!` ，而在服务端，你需要处理`$_REQUEST["_escaped_fragment_"]` 这是Google搜索引擎需要的。换句话说，`./#!page=1` 会被Google搜索引擎转成 `./?_escaped_fragments_=page=1。` （陈皓注：通常来说URL中的\#后的东西都不会被传到服务器上，所以，为了要让Google可以抓取AJAX的东西，你需要使用\#\!，而Google会把“\#\!”转成“\_escaped\_fragment\_”来向服务器发请求，Twitter的大量的链接者是\#\!的，比如：<https://twitter.com/#!/your_activity>）。另外，用户也许会使用Firefox 或 Chromium， `history.pushState({"foo":"bar"}, "About", "./?page=1");` 是一个很不错的命令。所以，就算是我们的地址栏上的地址改变了，页面也不会重新装载。这可以让你使用 `?` 而不是 `#!` 也能无刷地保住当前的动态的页面，这可以让AJAX的请求被浏览器记住。

* 别使用 “click here” 这样的链接。这样一来，无法SEO，而且对于一些需要使用读屏人来说很不友好（陈皓注：关于读屏软件，可参看本站的“[如果看不见你还能编程吗](https://coolshell.cn/articles/5514.html "如果你看不见你还能编程吗？")”）

* 做一个 [XML sitemap](http://www.sitemaps.org/)，并放在网端的根下 `/sitemap.xml`. （陈皓注：这个文件可以让搜索引擎了解你的网站图）
* 当你有多个URL指向同一个网页的使用，使用 [`<link rel="canonical" ... />`](http://googlewebmastercentral.blogspot.com/2009/02/specify-your-canonical.html) 你可以使用 [Google Webmaster Tools](http://www.google.com/webmasters/) 来查看相关的问题。

* 使用 [Google Webmaster Tools](http://www.google.com/webmasters/) 和 [Yahoo Site Explorer](http://siteexplorer.search.yahoo.com/).

* 安装 [Google Analytics](http://www.google.com/analytics/)  \(或是别的开源的网站分析工具，如： [Piwik](http://piwik.org/)\).

* 了解 [robots.txt](http://en.wikipedia.org/wiki/Robots_exclusion_standard) 和搜索引擎爬虫是如何工作的。

* 重定向请求 \(使用 `301 重定向网站`\) ，如果你要把 `www.example.com` 定向到 `example.com`\(或是其它的变更\) 这样可以防止Google的rank因为域名的变化发生改变。（陈皓注：301重定向一般用作域名变更）

* 知道并不是所有的爬虫都是好的，有些爬虫的行为并不好。（陈皓注：比如向你的网站发大量的请求导致服务器性能低下）

* 如果你有一些非文本的内容需要在 Google’s sitemap  中，比如视频什么的。[Tim Farley的答案](http://stackoverflow.com/questions/72394/what-should-a-developer-know-before-building-a-public-web-site#167608)，可以让你看到很多有价值的东西。

#### **技术**

* 理解什么是 [HTTP](http://www.ietf.org/rfc/rfc2616.txt) 比如 GET, POST, sessions, cookies等，了解什么是 “stateless” 无状态。

* 让你的 [XHTML](http://www.w3.org/TR/xhtml1/)/[HTML](http://www.w3.org/TR/REC-html40/) 和 [CSS](http://www.w3.org/TR/CSS2/) 符合 [W3C 规范](http://www.w3.org/TR/)，并确认他们都是 [合格的](http://validator.w3.org/)。我们的目标是避免浏览器的 “quirks mode”，并且可以让其更容易地能和非标准的浏览器工作，比如读屏器或移动设备。

* 理解浏览器是怎么处理 JavaScript 的。（陈皓：你会看到有些Javascript代码在页面上前面，有些则是在后面，所以你需要对其了解清楚为什么是这样）

* 了解浏览器是怎么装载 JavaScript，CSS和其它资源的，了解其对视觉上的影响。（陈皓注：10年前我做网页的时候因为HTML还很弱，所以只能使用table来布局，使用table布局的问题就是整个table读完后页面才会显示，用户的视觉体验并不好）。在某些情况下，你可能需要[把你的脚本放在页面的后面](http://developer.yahoo.net/blog/archives/2007/07/high_performanc_5.html)。

* 理解 JavaScript 的 sandbox 是怎么怎么工作的，尤其是你想使用iframes。

* 请注意 JavaScript 可能会被禁止，这样会让你的AJAX失效。就算是大多数用户都开启了Javascript功能，但是也可能在一些情况下脚本是不被运行的，比如移动终端上，搜索引擎抓网页的时候也并不会执行你的脚本。

* 学习 [301 和 302 转向的区别](http://www.bigoakinc.com/blog/when-to-use-a-301-vs-302-redirect/) \(这也是一个SEO的问题\).

* 尽可能多地学习你的部署平台。（比如：操作系统，Web Server：Apache/Nginx，防火墙，数据库，等等）

* 考虑使用一个 [Reset Style Sheet](http://stackoverflow.com/questions/167531/is-it-ok-to-use-a-css-reset-stylesheet).

* 考虑使用 JavaScript 框架\(如： [jQuery](http://jquery.com/), [MooTools](http://mootools.net/), [Prototype](http://www.prototypejs.org/), [Dojo](http://dojotoolkit.org/) 或 [YUI 3](http://developer.yahoo.com/yui/3/)\)，它们会很好的兼容于不同的浏览器。（陈皓注：强烈推荐你看一下本站的[开源中最好的WEB开发资源](https://coolshell.cn/articles/4795.html "开源中最好的Web开发的资源")一文）

* 把视觉效果和JS框架合在一起讨论，考虑使用一个Service，如：[Google Libraries API](http://code.google.com/apis/libraries/devguide.html) 来装载框架，这样可以让浏览器可能早就把这个JS框架已经cache了而不需要再从你的网站上下载了。

#### **Bug fixing**

* 明白你会花20%的时间写代码，而80%的时候在维护，所以你要小心编码。（陈皓注：参看本站的“[多些时间可以少些代码](https://coolshell.cn/articles/5686.html "多些时间能少写些代码")”一文）

* 设计一个好的错误报告机制。

* 设计一个入口可以让人们联系到你并给你建议和批评。

* 为你开发的东西形成文档，这样可以让后来的人容易维护你的软件和系统。

* 频繁备份（也可确保你的这些备份功能正常） [Ed Lucas 的回答](http://stackoverflow.com/questions/72394/what-should-a-developer-know-before-building-a-public-web-site#73970) 有一些忠告。你还需要有一个恢复策略，而不只是一个备份策略。

* 使用一个版本控制系统来保存你的代码，如： [Subversion](http://subversion.apache.org/) 或 [Git](http://git-scm.org/).

* 别忘了做Acceptance Testing，使用 [Selenium](http://seleniumhq.org/) 能帮到你。

* 确保你有足够的日志，你可以使用 log4j, log4n 或 log4r。如果出了问题，这是可以让你快速找到问题的方式。

* 当你写日志的时候，确保你记录了你捕获了处理和未处理异常。报告和分析日志可以让你知道你网站的问题。

这里有多的东西被省略了，并不是因为那些可能不是有帮助的答案，而是因为那些东西都太细节了，超出了这个问题的范围，因为这本来就是一个Web开发需要了解东西的Overview。我想你可以去看一下其它人的答案，我有时间，我也会补充别人的答案进来。请随意编辑这个答案，因为可能有些东西忘了，也有可能有些东西不对。

（全文完）

![image](images/1112-webkfzxyljddx-0.jpeg) 
![image](images/1112-webkfzxyljddx-1.jpeg)
关注CoolShell微信公众账号和微信小程序

**（转载本站文章请注明作者和出处[酷 壳 – CoolShell](https://coolshell.cn/) ，请勿用于任何商业用途）**

——=== **访问[酷壳404页面](http://coolshell.cn/404/) 寻找遗失儿童。** ===——

### 相关文章

* [
![image](https://coolshell.cn/articles/11021.html)
* [
![image](https://coolshell.cn/articles/17634.html)
* [
![image](https://coolshell.cn/articles/3684.html)
* [
![image](https://coolshell.cn/articles/9666.html)
* [
![image](https://coolshell.cn/articles/17066.html)
* [
![image](https://coolshell.cn/articles/12136.html)

![好烂啊](images/1112-webkfzxyljddx-8.gif)![有点差](images/1112-webkfzxyljddx-8.gif)![凑合看看](images/1112-webkfzxyljddx-8.gif)![还不错](images/1112-webkfzxyljddx-8.gif)
![image](images/1112-webkfzxyljddx-9.gif) \( **44** 人打了分，平均分： **4.70** \)

![image](images/1112-webkfzxyljddx-10.gif)
 Loading...
