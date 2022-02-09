---
layout: wiki  # 使用wiki布局模板
wiki: le_more # 这是项目名
title: SSL证书申请与配置
order: 3
---
## SSL证书申请

SSL证书申请并不像申请备案那么麻烦

只需要简单的几步就可以快速上手（全过程最短2分钟，实际时间看自己的主机或服务器访问速度，一般20分钟里能完全解决）

{% mark SSL验证的种类 color:green %}

+ File文件型
+ DNS解析型

{% mark SSL证书的种类 color:green %}

+ RSA证书 基于RSA算法（国际标准算法），应用较早，最为普及，比ECC算法的适用范围更广，兼容性更好，一般采用 2048 位的加密长度，但是对服务端性能消耗高。
+ ECC证书 基于ECC算法（椭圆加密算法），新一代算法趋势主流，一般采用 256 位加密长度，加密速度快，效率更高，对服务器资源消耗低，而且最重要的是更安全，抗攻击型更强

{% mark 本文仅讲述File文件型配置方法，DNS型请自行百科 color:yellow %}

### 进入FreeSSL，注册登陆，然后来到控制台

![](https://doc.cnin.top//Public/Uploads/2022-02-08/6202642f3c008.png)
![](https://doc.cnin.top//Public/Uploads/2022-02-08/6202647c46aab.png)

### 填写要申请的域名

{% mark 免费里只有TrustAsia是支持File的 color:yellow %}

![](https://doc.cnin.top//Public/Uploads/2022-02-08/620267247538d.png)

### 勾选SSL类型，验证类型，CSR生成方式，然后点击生成

![](https://doc.cnin.top//server/index.php?s=/api/attachment/visitFile&sign=a46c40e02e00380b9efa00dfd35c998f)

{% mark 此时浏览器会自动下载一个CSR私钥，后面还会用到，不要弄丢！！！ color:red %}

### 点击下载文件，下载一个txt文件，在你域名的根目录下创建 .well-known/pki-validatio路径，在这个路径下上传刚刚下载txt文件

{% mark 然后复制验证文件路径，在浏览器中打开，看看是否有显示和验证文件值一样的值 color:yellow %}

![](https://doc.cnin.top//server/index.php?s=/api/attachment/visitFile&sign=ec09902d8f180cc09bac7e929eb229fc)
![](https://doc.cnin.top//server/index.php?s=/api/attachment/visitFile&sign=20dfc1872fc580c705877fff7e967825)
![](https://doc.cnin.top//server/index.php?s=/api/attachment/visitFile&sign=56e0afe8c55d3f9b03cc39b9c086d316)

如果能够访问，那么再进行第三步

![](https://doc.cnin.top//server/index.php?s=/api/attachment/visitFile&sign=d7ba0ee716213c3eea9913c192053945)
![](https://doc.cnin.top//server/index.php?s=/api/attachment/visitFile&sign=bad7128061cbbf681cc3467ccf8d6ff1)

下载一个zip的压缩包，解压里面两个文件，并用记事本打开
![](https://doc.cnin.top//server/index.php?s=/api/attachment/visitFile&sign=343e9aa944bdb318752dedc4908f60e1)
![](https://doc.cnin.top//server/index.php?s=/api/attachment/visitFile&sign=9d7e66b3a32ece806bee0e619d23c81b)

完成后可以打开http强制转https
到此为止SSL就是全部配置完成了

> 本教程与[此网站](https://doc.cnin.top/web/#/6/49)同步