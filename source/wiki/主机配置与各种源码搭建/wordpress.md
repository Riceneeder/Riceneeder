---
layout: wiki  # 使用wiki布局模板
wiki: le_more # 这是项目名
title: wordpress开源博客的搭建
order: 1
---

{% noteblock color:yellow 前提 %}
在阅读此文章前默认您已经阅读过[快速上手](/wiki/乐下载主机/start.html)这篇文章
{% endnoteblock %}

> WordPress是一款能让您建立出色网站、博客或应用程序的开源软件

## 上传源码

[点击此处](https://cn.wordpress.org/latest-zh_CN.zip)获取源码或前往[官网](https://cn.wordpress.org/)下载源码,将源码压缩包上传到你网站的```wwwroot```目录或根目录```/```下，解压

解压后你的文件目录应该是与下列类似的结构

```
- wwwroot     // 或者为 '/'  
   |- web1     // 其他网站源码文件夹（如果你有）
   |- wordpress
      |- wp-admin
      |- wp-content
      |- index.php  // 必须要有，此为网页入口文件
      |- 等等其他文件及文件夹
```

## 绑定域名

绑定方法不再过多阐述

需要注意的是如果你的文件结构和上面是一样的话，你填写的绑定目录应当为

```
wwwroot/wordpress/
```

如果不同请以实际文件结构为准

## 安装wordpress

访问你绑定的域名，不出意外你应该会见到wordpress选择语言的界面

请选择中文，~~当然也不限制你想用什么语言~~，进入安装界面进行账号绑定与数据库绑定

数据库的名称与地址在控制面板页面可以获取，数据库密码和你当时申请主机时填入的密码相同，然后进行安装

到此，不出意外的话在安装结束后你就可以访问你的博客了，尽情享用吧！！