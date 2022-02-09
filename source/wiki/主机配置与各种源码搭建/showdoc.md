---
layout: wiki  # 使用wiki布局模板
wiki: le_more # 这是项目名
title: showdoc开源文档系统的搭建
order: 2
---

{% noteblock color:yellow 前提 %}
在阅读此文章前默认您已经阅读过[快速上手](/wiki/乐下载主机/start.html)这篇文章
{% endnoteblock %}

ShowDoc官网：[showdoc](https://www.showdoc.com.cn/)

ShowDoc是一个适合IT团队的在线API(接口)文档、技术文档的编辑工具，通过showdoc你可以方便地使用Markdown语法来书写出美观的API文档、数据字典文档、技术文档、在线excel文档等等

[演示网站](https://doc.cnin.top/web/#/1/3)

## 源码下载并上传服务器

从Github自动获取```git clone https://github.com/star7th/showdoc.git```

或手动下载[showdoc](https://www.showdoc.com.cn/)

或[点击此处](https://doc.cnin.top//server/index.php?s=/api/attachment/visitFile&sign=bd10097a856df15abe334302dbf4c941)直接下载

然后上传服务器并解压，将showdoc文件夹下的所有文件放置在根目录下或进行重定向

## 安装

进入自己的域名，然后选择语言（English/简体中文）

![](https://doc.cnin.top//server/index.php?s=/api/attachment/visitFile&sign=7dacabe485e866e71119d972f906ed6d)

默认账号 用户名：showdoc 密码：123456

再次刷新页面，选择我的项目，进入设置

![](https://doc.cnin.top//server/index.php?s=/api/attachment/visitFile&sign=cefa9929f59cea77ca68762ac6bc0fc9)
![](https://doc.cnin.top//server/index.php?s=/api/attachment/visitFile&sign=253d7aa1b349921ef8fd2943692eb934)

对管理员账户进行设置

![](https://doc.cnin.top//server/index.php?s=/api/attachment/visitFile&sign=9061b1bd23a6771685998d7d0914ae47)

再到站点设置中

网站外部访问url需要进行填写

![](https://doc.cnin.top//server/index.php?s=/api/attachment/visitFile&sign=dfbca5384412142db1145eb129097a96)

**安装就到此结束了，你可以回到“我的项目”中创建项目并开始你的编写**

> 本教程与[此站点](https://doc.cnin.top/web/#/1/2)同步更新
