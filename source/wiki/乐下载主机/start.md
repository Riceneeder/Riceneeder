---
layout: wiki  # 使用wiki布局模板
wiki: le # 这是项目名
title: 快速上手
order: 1
---

{% noteblock color:yellow 前提 %}
1.拥有基本的网络与电脑知识
2.拥有一个能够成功解析的域名（可使用UP所免费提供的二级域名）
{% endnoteblock %}

## 1.购买服务（免费）

首先进入UP的[官网](http://idc.letec.xyz/)（为缓解服务器压力和避免恶意购买，进入官网以及购买等操作的速度会明显缓慢）

![](https://gitee.com/MrVanme/photos/raw/master/202201242028299.jpeg)

点击右上角用户中心进行注册，注册成功后登录用户中心

![](https://gitee.com/MrVanme/photos/raw/master/202201242029849.jpeg)

进入用户中心后点击前往购买

![](https://gitee.com/MrVanme/photos/raw/master/202201242037473.png)

可选择的主机有很多，全部都是免费，如果本站显示缺货可以到[乐主机二站](http://idc1.letec.xyz/)或[乐科技](http://idc.zuizui.world/index.php/buy/index/)注册并购买

{% noteblock 提示 %}
购买时可能出现以下提示

```
提示信息：服务开通失败，但已扣除费用，请联系管理员处理
```
请勿慌张，重新或选择其他类型购买，如果反复购买失败请进入官方QQ群（950336404）进行反馈
{% endnoteblock %}


## 2.上传网站源码

购买成功后登录进入控制页面（不同站点不同主机可能控制面板不同，但操作是相通的）

![](https://gitee.com/MrVanme/photos/raw/master/202201242050410.jpeg)

点击```FTP/文件管理```里的在线文件管理器进入主机文件管理

![](https://gitee.com/MrVanme/photos/raw/master/202201242054039.jpeg)

进入```wwwroot```目录，如果没有请新建一个同名文件夹

![](https://gitee.com/MrVanme/photos/raw/master/202201242058895.jpeg)

点击上传文件，选择本教程提供的源码（[点击下载](https://oneindex-serverless-riceneeder.vercel.app/%E5%85%B6%E4%BB%96/game.7z
)，源码来自于[GitHub](https://github.com/yangyunhe369/h5-game-blockBreaker/)），然后上传

![](https://gitee.com/MrVanme/photos/raw/master/202201242101706.jpeg)

上传成功后点击文件旁的解压按钮进行解压，记住解压出来的文件夹名字，演示时解压出来的名字为```pacman-master```，请以实际解压出来的文件名为主，并且注意文件夹以及任何文件、文件路径不得为中文

{% noteblock color:red 提示 %}
请一定要查看文件夹内有没有index.htm或index.html或index.php文件，这个是一个网页的入口文件
{% endnoteblock %}

## 3.域名绑定

{% noteblock color:green 提示 %}
如果没有域名可以到[此处](http://yumingfenfa.xyz/)申请UP分发的免费二级域名
{% endnoteblock %}

回到控制面板，点击域名绑定进入绑定页面

![](https://gitee.com/MrVanme/photos/raw/master/202201242143750.jpeg)

在第一个``域名``框中填入你申请到的域名，在第二个``目录``框中填入``wwwroot/{此处填入你解压出来的文件名}/``，点击确定

![](https://gitee.com/MrVanme/photos/raw/master/202201242149651.jpeg)

然后回到你的域名提供商（或UP的免费域名分发站），进行域名解析，如下图（大部分解析界面都是相通的）

![](https://gitee.com/MrVanme/photos/raw/master/202201242151458.jpeg)

记录值填在主机域名绑定页面提示的IP

至此所有步骤结束，如果不出意外的话你将会看见一个打砖块游戏的页面

![](https://gitee.com/MrVanme/photos/raw/master/202201242154484.jpeg)

{% folding 域名解析提示 %}
设置 example.cn.ma 的域名解析，主机名填写：@

设置 www.example.cn.ma 的域名解析，主机名填写：www

设置 blog.example.cn.ma 的域名解析，主机名填写：blog 以此类推；

设置 _dnsauth.example.cn.ma SSL证书权限鉴定解析，主机名填写：_dnsauth

记录类型为 A ,记录值必须是一个ip地址;例如: 103.243.101.158

记录类型为 AAAA ,记录值必须是一个ipv6地址;例如: 1:2:3:4:5:6:7:8

记录类型为 CNAME ,记录值必须是其它有效域名,例如: www.nic.com.pk

记录类型为 MX ,记录值必须是其它有效域名,例如: mail.biz.tk ,MX优先级数字越小级别越高

记录类型为 TXT ,记录值是一段文本信息;

记录类型为 NS(子域授权,不常用也非必要,随意设置NS记录存在风险) ,记录值例如: tree.dnspod.net

网站需要的解析类型有：A、AAAA、CNAME; 邮箱需要的解析类型：MX；权限鉴定通常需要设置的解析类型：TXT
{% endfolding %}