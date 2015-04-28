Wiki in box
===

我觉得管理知识碎片的最好形式就是 Wiki，因为很多时候知识总是逃不出一个相互定义的圈子，因为这是知识的本质，这也是不懂英语的人拿到了一本英英词典却无法学会英文的原因。而 Wiki 中知识的相互链接恰好十分形象的表现了这一点。

扯远了哈，所以在经历过许多次的“查询 --> 忘记”的过程之后，我终于决定开始构建自己的知识体系了，那么如上所述， Wiki 便成了我的不二选择。

但是，自己搭建 Wiki 总是需要各种环境支持，这倒不不难，但是琢磨起备份的方法来总是觉得头晕。因为本人手残，在服务器上误删网站的事情也旅游发生，所以就希望一个简简单单，放在 Dropbox 里的 Wiki 系统。当然，其实这个已经有很多人在做了，但是也许是我笨，一个都没能试验成功，索性自己操刀了……

** Append: ** 我想我是被 Chrome 给坑了，他喵的不允许 Javascript 操作本地文件。所以如果你用的是 Chrome 浏览器，那么你必须搭建一个服务器。

不过好消息是：在 Windows 下搭建静态服务器的软件实在是多的一塌糊涂，且十分小巧方便，比打开一个记事本可能都要省资源，那么网盘里放一个也不算什么了。

Linux 下可能更简单一些，大部分系统都自带了 Python， 那么到 Wiki 根目录下运行 ```python -m SimpleHTTPServer 4000``` 然后访问 ```http://ocalhost:4000``` 即可。

Mac 系统我不了解，求赞助一个供我研究……

---

## 当前状态： ##

* 建立项目 ………… OK
* 文件体系 ………… OK
* 网页模板 ………… OK
* 代码转换 ………… OK
* 文件获取 ………… OK
* 命名空间 ………… OK
* 样式定义

## 使用说明： ##

我写完代码再告诉你

## 文件结构： ##

* /
	* 	|- files			全部引用文件
		* 	|- css			全部样式文件，包括 Bootscrap、Hightlight、自定义
		* 	|- fonts		全部字体文件，目前主要是 Bootscrap
		* 	|- js			全部脚本文件，包括 Bootscrap、Hightlight、自定义
	* 	|- files			全部引用文件
	* 	|- imgs				全部文章图片
	* 	|- data				全部文章源码
	* 	|- index.html		唯一的页面文件，负责解读一切内容


## 技术支持： ##

* [marked](https://github.com/chjj/marked) by [chjj](https://github.com/chjj) 这是一个很不错的 Markdown 转化 Html 的工具，JavaScript 书写， Node.js 和本地都可以使用.
* [highlight.js](https://github.com/isagalaev/highlight.js) by [isagalaev](https://github.com/isagalaev) 一个真心好用的代码高粱工具，支持 118 种代码高亮。爽得一塌糊涂，记得去他的管网下载，我就是傻乎乎的在 Github 下载的，然后被坑的好爽……
