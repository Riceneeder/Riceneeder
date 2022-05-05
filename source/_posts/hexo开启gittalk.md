---
title: hexo开启gittalk
tags:
  - hexo
  - gittalk
abbrlink: 2c6e892
date: 2021-06-28 23:15:44
headimg: https://i.gyazo.com/90d0fad5395539dfbdc0f25e27bfa885.png
---


## 如何在hexo中开启gittalk

我在搭建博客的时候想要有一个评论区，然后发现了gittalk这个神器，然后踩坑踩了一晚上，现在终于成功，写个博客记录分享一下

<!--more-->

> 本文章为原Github博客文章

## 步骤

### 1.首先在github上注册一个应用

链接：https://github.com/settings/applications/new

+ 在 Appliction name 填上自己以后看到知道这是什么的名字，如“博客评论用”

+ 在 Homepage URL 填上自己博客主页链接，比如我的：https://my-blog-eight-dun.vercel.app/

+ 在 Authonrization callback URL 也填上自己的博客链接

+ **点击注册后记下页面上的`Client ID`和`Client Secret`，必须现在记下，不然等会儿可能就看不到secret了**

### 2.修改`\themes\Your_themes\_config.yml`(我用的主题叫~~Ocean~~Butterfly~~，已经集成了gittalk，没有集成的同学可能要自己想想办法~~)

```yml
# Gitalk
gitalk:
  enable: true # 开启gittalk
  clientID: ××××××× # 申请的 Client ID
  clientSecret: ×××××× # 对应的 Client Secret
  repo: Riceneeder # 用于存放评论的仓库名，例如我的就是Riceneeder
  owner: Riceneeder # GitHub ID 
  admin: Riceneeder # GitHub ID
```

然后记得在相对应的仓库开启Issues

### 3.然后愉快地部署就可以了

> 参考资料：https://www.jianshu.com/p/02fc71f3633f

