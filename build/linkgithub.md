# Link Github

- 目标
	- 直接在Github的repo中进行修改 然后直接同步到Gitbook  
- 发现 [Link a book and a GitHub repository](http://help.gitbook.com/github/index.html)
	- **同步**从 Github-》》》 Gitbook 可直接在Github修改repo内容 编辑gitbook
	- **同步不可逆 **以上不可逆 在gitbook的builds不会改变Github远程库repo的内容
> **Caution:** When you specify a GitHub repository in your book's settings, it will take priority over GitBook's git repository, this means that the editor will directly edit content on GitHub.  
> 
**The sync is unidirectional,** only changes made on GitHub will trigger builds on GitBook, GitBook will not update your GitHub repository with any content written before.

- 执行 参考[Transferring content to GitHub](http://help.gitbook.com/github/transferring_to_github.html)
	- 进入Gitbook网站 gitbook与github帐号连接
	- 选择书籍 进入 setting --》》 Github --》》 Export to Github 
		- 因为我现在Gitbook编辑了 所以Export to Github
		- 如果先在Github上有书籍Repo 可以直接 Link
			- 我可以将本地book的working dir与Github中repo连接 然后直接选择此处的 Link
	- 进入 Github Importer --》》 check url 
	- 因为之前我已经Pull了Gitbook的repo then 我直接push到上面所建立的Github Repo 但是发现不可行

			git remote add gbhub git@github.com:<...>.git
			git branch --track gbhub master
			git pull gbhub master 

		> fatal: 'gthub' does not appear to be a git repository
		fatal: Could not read from remote repository.
		
		- 出错 我也明白 我之间就将本地repo与gitbook 进行关联了 
		- 所以尝试另外建立一个文件夹 git pull 这个文件夹 但是我想直接在gitbook本地repo进行修改 不想再建 那么我就尝试 去掉本地repo与gitbook的关联 直接让本地repo与书籍github库进行关联 因上面也提到改变github repo可以直接改变gitbook 【这个想法我没有去尝试】
		- 我将github repo clone到本地 
			- 本地新建文件目录（文件夹）
			- $ git init
			- $ git clone https://github.com/JeremiahZhang/gitbookguide.git
			- $ git remote add 
			- $ git push 这里只推到了github repo
		- 经历以上折腾后 不成功 哪里不成功
			- 1 push 到github后 gitbook 无反应
			- 这时候想到可能要双推 gitbook要推 github也要推
		-  这时候突然想起了 OMOOC.py的[double push](https://openmindclub.gitbooks.io/omooc-py/content/support/dpush.html)
- 嗯 走了这么多弯路 最后发现

> - 我已经有了local repo 因为我之前就是在本地local repo 编辑图书 之后push 到gitbook的   
> - 那么我在gitbook网页用GithubImporter与Github连接之后 
> - 我可以直接将local repo 推送到 Github repo 之前不用进行Pull了
> - 只要进行双推就OK了   
> 因为相信Gitbookhelp文档说的 只要github repo更新 Gitbook自动同步 嗯 我试过了 不行

- 结果
	- 用double push解决了问题 现在理解了为什么double push Gitbook help中说的github同步gitbook 是个坑啊