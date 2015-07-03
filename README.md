Wiki in box
===

我觉得管理知识碎片的最好形式就是 Wiki，因为很多时候知识总是逃不出一个相互定义的圈子，因为这是知识的本质，这也是不懂英语的人拿到了一本英英词典却无法学会英文的原因。而 Wiki 中知识的相互链接恰好十分形象的表现了这一点。

扯远了哈，所以在经历过许多次的“查询 --> 忘记”的过程之后，我终于决定开始构建自己的知识体系了，那么如上所述， Wiki 便成了我的不二选择。

但是，自己搭建 Wiki 总是需要各种环境支持，这倒不不难，但是琢磨起备份的方法来总是觉得头晕。因为本人手残，在服务器上误删网站的事情也屡有发生，所以就希望一个简简单单，放在 Dropbox 里的 Wiki 系统。当然，其实这个已经有很多人在做了，但是也许是我笨，一个都没能试验成功，索性自己操刀了……

**Append:** 我想我是被 Chrome 给坑了，他喵的不允许 Javascript 操作本地文件。所以如果你用的是 Chrome 浏览器，那么你必须搭建一个服务器。

不过好消息是：在 Windows 下搭建静态服务器的软件实在是多的一塌糊涂，且十分小巧方便，比打开一个记事本可能都要省资源，那么网盘里放一个也不算什么了。

Linux 下可能更简单一些，大部分系统都自带了 Python， 那么到 Wiki 根目录下运行 ```python -m SimpleHTTPServer 4000``` 然后访问 ```http://localhost:4000``` 即可。

Mac 系统我不了解，求赞助一个供我研究……

**如果你使用 Sublime Text 作为编辑器，那么，只需要安装 SublimeServer 插件 [SublimeServer](https://github.com/learning/SublimeServer) 便可以轻松 High 翻天。本人目前的测试工作都是在这上面进行。**

---

## 当前状态： ##

* 建立项目 ………… OK
* 文件体系 ………… OK
* 网页模板 ………… OK
* 代码转换 ………… OK
* 文件获取 ………… OK
* 命名空间 ………… OK
* 样式定义 ………… OK
* 首页文档 ………… OK
* 内页链接 ………… OK
* 代码复制 ………… OK
* 页内索引 ………… **Beta**
* 数学公式 ………… OK
* 变量设置
* 内链优化

## 使用说明： ##

1. 如果你使用的是 Firefox 浏览器，那么可以把文件放在网盘，在本地使用，十分方便；
2. 如果你使用的是 Chrome 浏览器，你需要准备一个 Http 服务器，请不要找那些大型套件，一个很小很小的 Http 服务器即可，把文件放在网站根目录，在本地使用一样爽歪；
3. 如果你有需要，也可以以上传到网站进行展示，这不需要做任何修改，但是由于是异步读取文件内容，境外主机请慎选，否则可能页面加载时间过长；
4. 文件存放在 data 目录下，后缀为 md，因为本系统支持的是 Markdown 语法（[Markdown教程](http://wowubuntu.com/markdown/)）；
5. data 目录下支持子目录；
6. 命名空间深度无限，区分大小写，详细规则如下：

	http://yourname.com/?name=dir-a:dir-b:file-c
	
	对应读取文件为：

	/data/ dir-a/dir-b/file-c.md

7. 内部链接只需要链接到页面命名，比如：```[链接到一个页面](linux:vim)```；
8. imgs 文件夹可用来储存文章图片，目录结构自行安排；
9. 打开 latex.html 文件可以浏览相应加载 MathJax 的 md 文档；

## 文件结构： ##

* /
	* 	|- files			全部引用文件
		* 	|- css			全部样式文件，包括 Bootscrap、Hightlight、自定义
		* 	|- fonts		全部字体文件，目前主要是 Bootscrap
		* 	|- js			全部脚本文件，包括 Bootscrap、Hightlight、自定义
	* 	|- imgs				全部文章图片
	* 	|- data				全部文章源码
		*	|- index.md		默认显示文档，建议用作索引
	* 	|- index.html		唯一的页面文件，负责解读一切内容
	* 	|- latex.html		新增的页面文件，用于解读带LaTeX公式的内容


## 技术支持： ##

* [marked](https://github.com/chjj/marked) by [chjj](https://github.com/chjj) 这是一个很不错的 Markdown 转化 Html 的工具，JavaScript 书写， Node.js 和本地都可以使用.
* [highlight.js](https://github.com/isagalaev/highlight.js) by [isagalaev](https://github.com/isagalaev) 一个真心好用的代码高亮工具，支持 118 种代码高亮。爽得一塌糊涂，记得去他的管网下载，我就是傻乎乎的在 Github 下载的，然后被坑的好爽……
* [toc](https://github.com/jgallen23/toc) by [jgallen23](https://github.com/jgallen23) 这是一个业内索引 jQuery 插件. 不幸的是，此插件存在点击目录定位不准的问题。
