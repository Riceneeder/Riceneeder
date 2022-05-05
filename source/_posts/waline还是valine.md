---
title: waline还是valine?
tags:
  - hexo
  - waline
  - valine
abbrlink: '56244039'
date: 2021-07-05 16:01:56
headimg: https://p5.ssl.qhimg.com/t01ec54674f5912eea9.png
---

[Valine](https://link.zhihu.com/?target=https%3A//valine.js.org/) 是一款样式精美,部署简单的评论系统,第一次接触便被它精美的样式,无服务端的特性给吸引了.它最大的特色是基于 [LeanCloud](https://link.zhihu.com/?target=https%3A//leancloud.app/) 直接在前端进行数据库操作而无需服务端,极大的缩减了部署流程,仅需要在静态页引入 Valine SDK 即可

<!--more-->

## Valine

Valine 诞生于2017年8月7日,是一款快速、简洁且高效的无后端评论系统,理论上支持但不限于静态博客,目前已有[Hexo](https://valine.js.org/hexo.html)、[Jekyll](https://valine.js.org/jekyll.html)、[Typecho](http://typecho.org/)、[Hugo](https://gohugo.io/)、[Ghost](https://ghost.org) 等博客程序在使用Valine

但是由于`appID`和`appKey`全部暴露在前端,这就会涉及到LeanCloud的数据安全问题,具体分析可以看看知乎上的这篇文章:[基于 Serverless 的 Valine 可能并没有那么香 - 怡红公子的文章 - 知乎]( https://zhuanlan.zhihu.com/p/295264916)

## Waline

基于以上原因，我们发现只有增加一层服务端中间层才能很好的解决 Valine 的安全问题，所以 [Waline](https://link.zhihu.com/?target=https%3A//waline.js.org/) 横空出世了！Waline 与 Valine 最大的不同就是增加了服务端中间层，解决 Valine 暴露出来的安全问题。同时基于服务端的特性，提供了**邮件通知**、**微信通知**、**评论后台管理**、LeanCloud, MySQL, MongoDB, SQLite, PostgreSQL **多存储服务支持**等诸多特性。

而且Waline同时也支持Github登录,并且Github的应用密钥会保存在搭建Waline的服务器上从而避免了隐私泄露

不仅如此，Waline 默认使用 [Vercel](https://link.zhihu.com/?target=https%3A//vercel.com/) 部署，实现完全免费部署！

本博客在此片文章前使用过基于github issue 的[Gittalk](https://gitalk.github.io/)和[Vssue](https://vssue.js.org/zh/),体验都不是很好,又碍于Valine的隐私泄露问题,所以最终选择了Waline,欢迎大家在下面留言评论