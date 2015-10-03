# Update with GIT

我参考的这篇[Update your book using GIT](http://help.gitbook.com/build/push.html) 然后按照里面非方法 遇到坑了

- 第一没有在Gitbook上建立相应的书籍 gitbookguide
- 第二没有Git pull 直接就push了

		git remote add gitbook https://username:apitoken@git.gitbook.com/marshallshen/ruby-api-best-practices.git
		git push -u gitbook master
刚开始就是这样 不成功

纠正：

		git remote rm gitbook
		git remote add gitbook https://username:apitoken@git.gitbook.com/marshallshen/ruby-api-best-practices.git
		git branch --track gitbook master
		git pull gitbook master
在本地库中 稍作修改有些内容合并了   
然后再进行Push 就成功了 

使用gitbook editor的 [另外的参考文章](https://ilmvfx.wordpress.com/2015/09/30/gitbook-introduction-and-test-drive-maya-houdini-scripts-cookbook/)  
[Issues](https://github.com/GitbookIO/gitbook/issues/660)