# 图书章节

每一本图书都有章节 那么如何设置呢？该在哪里设置呢？

在之前建立的SUMMARY.md文档中进行设置  
内容如下：



> # Summary   
* [Intro] (README.md)
* [安装内容] (setup/README.md)
	* [Node.js安装] (setup/nodejsinstall.md)
	* [gitbook安装] (setup/gitbookinstall.md)
	* [gitbook command] (setup/gitbookci.md)
* [图书格式] (booksetup/README.md)
	* [关于README] (booksetup/AboutREADME.md)
	* [图书章节] (booksetup/AboutSummary.md)

以上是我一部分的文件章节内容 注:真正编写SUMMARY的时候 []与()之间没有空格

## 目录初始化 ##

之后我需要进行 **目录初始化**

- $ gitbook init

初始化后 在我的GitbookGuide中 自动创建相关文件夹 如

- setup
- booksetup

以上两个文件夹包含了我命名的.md文档 如上面括号中的文档  
在setup中有4个文档

- README.md
- nodejsinstall.md
- setup/gitbookinstall.md
- setup/gitbookci.md

各个文档中的一级标题就是章节名称

参考[章节设定](https://wastemobile.gitbooks.io/gitbook-chinese/content/format/chapters.html)