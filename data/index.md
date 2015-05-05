示例文档
===

一个可以放在各种网盘，各种空间的，Markdown 语法支持的 Wiki 系统，可以用来方便的管理自己的知识碎片。欢迎各种支持～

[Github 项目页](https://github.com/dmscode/Wiki-in-box)

## 使用说明： ##

1. 如果你使用的是 Firefox 浏览器，那么可以把文件放在网盘，在本地使用，十分方便；
2. 如果你使用的是 Chrome 浏览器，你需要准备一个 Http 服务器，请不要找那些大型套件，一个很小很小的 Http 服务器即可，把文件放在网站根目录，在本地使用一样爽歪；
3. 如果你使用 Sublime Text 作为编辑器，那么，只需要安装 SublimeServer 插件 [SublimeServer](https://github.com/learning/SublimeServer) 便可以轻松 High 翻天
4. 如果你有需要，也可以以上传到网站进行展示，这不需要做任何修改，但是由于是异步读取文件内容，境外主机请慎选，否则可能也面颊在时间过长；
5. 文件存放在 data 目录下，后缀为 md，因为本系统支持的是 Markdown 语法（[Markdown教程](http://wowubuntu.com/markdown/)）；
6. data 目录下支持子目录；
7. 命名空间深度无限，详细规则如下：

	http://yourname.com/?name=dir-a:dir-b:file-c

	对应读取文件为：

	/data/ dir-a/dir-b/file-c.md

8. 内部链接只需要链接到页面命名，比如：```[链接到一个页面](linux:vim)```；
9. imgs 文件夹可用来储存文章图片，目录结构自行安排

## 文件结构： ##

* /
	* 	|- files			全部引用文件
		* 	|- css			全部样式文件，包括 Bootscrap、Hightlight、自定义
		* 	|- fonts		全部字体文件，目前主要是 Bootscrap
		* 	|- js			全部脚本文件，包括 Bootscrap、Hightlight、自定义
	* 	|- files			全部引用文件
	* 	|- imgs				全部文章图片
	* 	|- data				全部文章源码
		*	|- index.md		默认显示文档，建议用作索引
	* 	|- index.html		唯一的页面文件，负责解读一切内容

## 代码高亮： ##

	<script>
		alert('Hello, World!')
	</script>

## 图片效果： ##

![Bridge](imgs/bridge.jpg)