# webhooks setup

上一节在于Github整合的时候 发现更新Github repo不会造成 Gitbook书籍更新 原以为Webhooks出错 嗯 webhook不是自动添加的 需要认为添加 步骤如下

- 将要gitbook中的书籍 Link Github 进入我的gitbook图书 Github设置

<center>
![webhooks1](https://raw.githubusercontent.com/JeremiahZhang/gitbookguide/master/_images/webhooks1.JPG)
</center>  

原来这里有link mybook to Github repo 当初做的时候就在头上也没有在意 直接Export To Github是没有用的 还要link Github 嗯 这样才能增加 webhooks 然后只要Push 到 Github repo 就可以直接更新书籍 不用先前的 double push 了

- 将Github 对应gitbook书籍的 repo 填上 然后点击 add webhook就ok了

<center>
![webhooks2](https://raw.githubusercontent.com/JeremiahZhang/gitbookguide/master/_images/webhooks2.JPG)
</center>  