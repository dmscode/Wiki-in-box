说明文档
===

一个可以放在各种网盘，各种空间的，Markdown 语法支持的 Wiki 系统，可以用来方便的管理自己的知识碎片，也可以用来搭建自己的静态博客（http://zji.me/ ）。欢迎各种支持～

[主页 / 发布页](http://dmscode.github.io/Wiki-in-box/) | [Github 项目页](https://github.com/dmscode/Wiki-in-box)

## 请支持一下 ##

如果您觉得这个小程序对你有所帮助，希望您请我喝杯咖啡，让我在这寒冷的冬日里感受到一份温暖，谢谢~

本人支付宝账号：**alay9999@163.com**

## 使用说明 ##

* 页面内容文件存放在 data 目录下，后缀为 md，因为本系统支持的是 Markdown 语法（[Markdown教程](http://wowubuntu.com/markdown/)）；
* data 目录下支持子目录；
* 内部链接只需要链接到页面命名，比如：`[链接到一个页面](linux:software:vim)`；
* 命名空间深度无限，详细规则如下：

> linux:software:vim

对应读取文件为：

> /data/linux/software/vim.md

* imgs 文件夹可用来储存文章图片，也可自行安排使用其他位置；

### 本地使用 ###

* 站点文件可以存放在任意喜欢的位置，就如同您期望的，存放在网盘中是一个十分不错的选择。你唯一需要注意的只是保持这些文件的相对位置不变而已；
* 如果你使用的是 Firefox 浏览器，那么直接访问 `index.html` 文件即可，十分方便；
* 如果你使用的是 Chrome 浏览器，你需要准备一个 Http 服务器，请不要找那些大型套件，一个很小很小的 Http 服务器即可，把服务器的根目录设置到 `index.html` 文件所在目录即可，在本地使用一样爽歪；
* 如果你使用 Sublime Text 作为编辑器，那么，只需要安装 [SublimeServer](https://github.com/learning/SublimeServer) 插件便可以轻松 High 翻天；

### 在线使用 ###

* 如果你有需要，也可以以上传到您的网站空间上进行展示，这不需要做任何修改，但是由于是异步读取文件内容，境外主机请慎选，否则可能页面加载时间过长；

### 添加页内目录 ###

因为 Wiki 单页面很容易有大量的内容，这时候就需要有页内导航，本系统支持页内目录功能。使用方法：

> 在文档内任意位置的单独一个段落使用标签 `[TOC]` 即可，每页只可使用一次，效果如本页。

[TOC]

### 关于语法 ###

较基本语法略有增强，额外支持表格和注释[注释]。其他需求请自行使用 HTML 代码解决。

[注释]: 这是一个注释

## 文件结构： ##

* /
	* 	|- files			全部引用文件
		* 	|- css			全部样式文件，包括 Bootscrap、Hightlight、自定义
		* 	|- fonts		全部字体文件，目前主要是 Bootscrap
		* 	|- js			全部脚本文件，包括 Bootscrap、Marked、Hightlight、toc、自定义
	* 	|- imgs				全部文章图片
	* 	|- data				全部文章源码
		*	|- index.md		默认显示文档，建议用作索引
	* 	|- index.html		唯一的页面文件，负责解读一切内容

## 技术支持： ##

* [marked.js](https://github.com/chjj/marked) by [Christopher Jeffrey (JJ)](https://github.com/chjj) 这是一个很不错的 Markdown 转化 Html 的工具，JavaScript 书写， Node.js 和本地都可以使用.
* [highlight.js](https://github.com/isagalaev/highlight.js) by [Ivan Sagalaev](https://github.com/isagalaev) 一个真心好用的代码高亮工具，支持 118 种代码高亮。爽得一塌糊涂，记得去他的官网下载，我就是傻乎乎的在 Github 下载的，然后被坑的好爽……
* [TOC.js](https://github.com/jgallen23/toc) by [Greg Allen](https://github.com/jgallen23) 生成页内标题目录的工具，自定义性很好，只是默认设置对中文……很不友好。不过改个设置就好。