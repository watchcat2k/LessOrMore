---
layout: post
title:  利用github page和jekyll搭建个人博客网站（二）：使用域名
date:   2019-03-02 00:00:00 +0800
categories: 个人静态博客网站建设
---

* content
{:toc}





本人参考了这篇博客[https://blog.csdn.net/yucicheung/article/details/79560027](https://blog.csdn.net/yucicheung/article/details/79560027)，成功地将自己申请的域名解析到自己之前创建了个人静态博客网站，现在总结一下步骤。

# 域名注册  {#domain-regist}
本人是在阿里云购买注册域名的，前往此处[https://wanwang.aliyun.com/?spm=5176.8142029.735711.62.7df46d3enEbCVs](https://wanwang.aliyun.com/?spm=5176.8142029.735711.62.7df46d3enEbCVs)，查询你想要的域名，如下图所示：

![在这里插入图片描述](https://img-blog.csdnimg.cn/201903021651427.PNG)

在输入栏输入你想要的域名，若该域名已被注册，则我们无法购买，如下图所示：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190302165431118.PNG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MjcyMjgy,size_16,color_FFFFFF,t_70)

挑选好自己想要的域名，然后点击“加入清单”，通常`.com`域名需要55元一年，而其它特殊域名价格很高。购买域名时还要实名认证什么的，这些可以自己完成。

购买了域名后，就可以在个人管理控制台的左侧栏中，点击`域名`一项，如下图：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190302170118399.PNG)

然后就可以看到自己的域名列表了，如下图：

![在这里插入图片描述](https://img-blog.csdnimg.cn/2019030217021286.PNG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MjcyMjgy,size_16,color_FFFFFF,t_70)

# 域名解析  {#domain-analysy}
首先获取我们之前建立的个人静态博客网站的`ip`地址，比如我的个人静态博客网站网站为[https://watchcat2k.github.io/](https://watchcat2k.github.io/)，那个打开命令行，在命令行中输入`ping watchcat2k.github.io `，如下图：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190302170807633.PNG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MjcyMjgy,size_16,color_FFFFFF,t_70)

那么，我的个人静态博客网站的`ip`地址为`185.199.110.153`，在阿里云的域名列表中，点击`管理`，如下图：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190302171048761.PNG)

然后，再点击左侧栏的`域名解析`一项，如下图：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190302171150300.PNG)

然后点击`新手引导`这一项，如下图：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190302171257564.PNG)

在弹出框中填入刚刚获取的个人静态博客网站的`IP`地址即可

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190302171429423.PNG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MjcyMjgy,size_16,color_FFFFFF,t_70)

# github page的配置  {#github-page-setting}
进入个人github账号中的`username.github.io`项目（username为个人github账号用户名），点击`setting`，如下图：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190302171636905.PNG)

然后找到`github page`这一项，在`Custom domain`里填入自己刚刚注册好的域名，并且把`Enforce HTTPS`这一项勾上如下图：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190302171915390.PNG?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzM2MjcyMjgy,size_16,color_FFFFFF,t_70)

勾上`Enforce HTTPS`，是为了使自己的网站能通过https（密文传输）访问，否则的话，一部分浏览器会提示该站点不安全。完成之后，在浏览器中输入你申请的域名，就可以访问了。

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190302172234224.PNG)
