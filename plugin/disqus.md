# Disqus

作为一个非常流行的为网站集成评论系统的工具，Gitbook可以集成Disqus 便于和读者进行交流 好形成反馈

- 1 首先注册Disqus 参考[配置 Disqus](https://openmindclub.gitbooks.io/omooc-py/content/support/Disqus_Setup.html) 发现出错 出现
> We were unable to load Disqus. If you are a moderator please see our troubleshooting guide. 

- 2 去了 [troubleshooting guide](https://help.disqus.com/customer/portal/articles/472007-i-m-receiving-the-message-%22we-were-unable-to-load-disqus-%22)
- 3 排除解决方案 第一反应 book.json的问题 google search Gitbook disqus then 参考[GitbookIO/plugin-disqus](https://github.com/GitbookIO/plugin-disqus) 
	- install disqus 插件 $ npm install gitbook-plugin-disqus -g 但是为修改 book.json 还是用的1 连接中的设置
	- 然后 双推 
	- 还是出现1的结果
	- 修改book.json 按照3中的参考链接
	- 此次Gitbook中成功加载Disqus评论

更正：

- 在OMOOC的[配置 Disqus](https://openmindclub.gitbooks.io/omooc-py/content/support/Disqus_Setup.html) 中有错
	- 得 install disqus plugin 
	`$ npm install gitbook-plugin-disqus -g`
	- 再得 book.json文件 代码如下
 
		    {
			"plugins": ["disqus"],  
			"pluginsConfig": {  
			"disqus": {  
				"shortName": "XXXXXXX"  
					}
				}  
			}

你也可以参考这篇较好的[Gitbook教程](http://www.chengweiyang.cn/gitbook/plugins/functional/disqus.html)


