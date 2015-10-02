# gitbook安装

在gitbook安装中 因为我不熟悉命令行的使用 遇到了很多坑 也尝试了许多方法 现在一一道来

- [gitbook安装](http://tonydeng.github.io/gitbook-zh/gitbook-howtouse/howtouse/gitbookinstall.html)在cmd中直接npm install gitbook -g 出错 用git bash 也是出错 初步断定
	- **纠错中** 文件路径 姿势不对
		- change workdir in nodejs file 还是错误
		- 嗯 version 陈旧 2.14.4 OK 更新 [github issue](https://github.com/npm/npm/pull/9743) 失败
		- 继续执行 cmd 下 [Gitbook Library and cmd utility to generate GitBooks](https://www.npmjs.com/package/gitbook)
			> npm install gitbook-cli -g  
			> 依然 failure 文件夹不在node.js所在的文件
		- D:
		- CD <node.js所在文件名>
		- 执行 npm install gitbook-cli -g 
			- this time it is OK 
			- gitbook -V 版本为 0.3.6
	- 参考[简明教程](http://colobu.com/2014/10/09/gitbook-quickstart/) gitbook serve ./repository
		- cmd 将 一个 repo作为一本书 failure
	- 嗯 新建一文件夹 npm install gitbook -g 成功
	- 但是 gitbook 之后 出现要我 npm uninstall -g gitbook 然后 npm install -g gitbook-cli
	- ok 按照上面的完成
	- 执行 gitbook 显示OK
	- 之后按照[gitbook 2.0](http://samwhelp.github.io/blog/read/platform/gitbook2/diff/) 成功安装 Gitbook2.4.3
	- [建立.gitignore](http://samwhelp.github.io/blog/read/platform/gitbook/start/)
	- 再按上文的流程来 建立 README.md SUMMARY.md
		> touch README.md SUMMARY.md  


挖了这么多坑 gitbook升级为2.0了 关键部分参考了 [gitbook2.0](http://samwhelp.github.io/blog/read/platform/gitbook2/diff/)成功进行了安装

#### 安装gitbook ####

- 在所<node.js所在文件名> cmd 执行 npm install gitbook-cli -g
- $ gitbook 查看安装是否成功
- $ gitbook -V 查看version
- $ gitbook versions:install lastest 安装最新版本的 gitbook

### 我的新书 ###

这部因为安装好Babun 所以直接用Babun来进行操作

-  建立「.gitignore」 [参考folder](https://github.com/GitbookIO/gitbook#ignoring-files--folders) 非必要 可以不建立

		wget -c https://raw.githubusercontent.com/github/gitignore/master/GitBook.gitignore -O .gitignore
	上面这段代码 直接在win cmd中是无效的 用babun直接就解决了
- 建立「README.md」，「SUMMARY.md」 文档  
	- $ touch README.md  SUMMARY.md
- $ gitbook serve 可以查看书籍网址http://localhost:4000/ 在浏览器中键入 就可以查看了 当退出该 serving 的时候 图书网址没有用 
- $ echo "# bookname" > README.md 修改书名 这个也可以直接在README.md中进行修改

主要参考文章[buntu環境下，快速開始使用gitbook](http://samwhelp.github.io/blog/read/platform/gitbook/start/)