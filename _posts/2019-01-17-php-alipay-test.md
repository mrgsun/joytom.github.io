---
layout: post
title:  "支付宝支付测试"
categories: Personal
tags:  Personal
author: mrgsev
---
## php实现支付宝接口：
如果你要进行操作，建议你首先去蚂蚁金服看一看开发文档，因为我们不是真正的商户，平台为我们提供了进行了测试的环境--------沙箱。像了解一下吗？快来测试吧
###准备工具
你要先有一个实名认证的支付宝账号
下载一个demo包  
编辑器
基本上就差不多了，
###一 [下载sdk开发工具包]( https://docs.open.alipay.com/270/106291/)
![](https://upload-images.jianshu.io/upload_images/15073013-778758a9c285a256.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
用什么语言进行测试下载相应的数据包就行了。（这里演示的只是模拟的环境 项目中需要你自己来写逻辑和调用接口）
![](https://upload-images.jianshu.io/upload_images/15073013-2986dfe6920df8b9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

下载好了之后   把他解压在项目里就可以了。大体结构就是这样的，标注的单个文件分别是配置文件（用来配置参数）、支付结果异步通知、支付结果同步通知（通知文件就是写业务逻辑）
![](https://upload-images.jianshu.io/upload_images/15073013-a9dfc350286fde91.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

config文件打开后你会看到这些东西，需要哦我们来填写的有 六类应用id  商户私钥   异步通知   同步跳转   支付宝网关  支付宝公钥   这些东不能弄错 否则就实现不了。我们看看怎么获取这下参数吧
![](https://upload-images.jianshu.io/upload_images/15073013-601046709ace2252.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

首先用你实名认证的支付宝登[陆蚂蚁金服 进入沙箱环境](https://openhome.alipay.com/platform/appDaily.htm)你就会看到他给你提供的信息了，
![](https://upload-images.jianshu.io/upload_images/15073013-1733073216f3e951.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
密钥需要你自己获取，windows可以下载[支付宝密钥生成器](https://docs.open.alipay.com/291/105971)来生成一对密钥（密钥都是成对存在的）

![](https://upload-images.jianshu.io/upload_images/15073013-a01705196c911dc8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/15073013-323da8134c454e75.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

生成的时候一定要看好 因为我们用的是php语言 不要生成java的密钥了，生成之后把私钥配置到配置文件中，把公钥放到沙箱中PAS2就会自动生成支付宝公钥之后把它放到配置文件中就可以了。

![](https://upload-images.jianshu.io/upload_images/15073013-c4f30034fc7ab9de.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

完成之后再修改config.php文件中的通知和跳转就可以实现测试的支付功能了
![](https://upload-images.jianshu.io/upload_images/15073013-f8fb1e2ceb4320ab.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![image.png](https://upload-images.jianshu.io/upload_images/15073013-0d6f6e595c32d939.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](https://upload-images.jianshu.io/upload_images/15073013-ae358481bd9970bb.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
