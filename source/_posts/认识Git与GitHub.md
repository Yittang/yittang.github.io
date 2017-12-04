---
title: 初识Git与GitHub
date: 2017-12-02 16:02:21
categories: GitHub系列
tags: [Git,GitHub,Node.js]
---
![](http://upload-images.jianshu.io/upload_images/5875188-15ad88a4b9c019ac.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
# 前言
&emsp;&emsp;GitHub 是一个面向开源及私有软件项目的托管平台，因为只支持Git作为唯一的版本库格式进行托管，故名 GitHub。
# Git的安装
1. 在使用GitHub之前首先要安装[Git](https://git-scm.com/)
2. 具体如何安装可以看[这篇](https://jingyan.baidu.com/article/90895e0fb3495f64ed6b0b50.html)

# GitHub初体验
在进入[GitHub](https://github.com)官网，你首先要注册一个账号(ps:这个就是你个人账户，牢记！)
![GitHub注册](http://upload-images.jianshu.io/upload_images/5875188-3f950b6801ca530a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

**既然我们都已经迈出了第一步，是不是该体验起飞的感觉了！**

# Github仓库的创建
不急，我们先进入主页我们会看到右边有这么一个大绿色按钮![](http://upload-images.jianshu.io/upload_images/5875188-d5eb719b1df0d063.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

毫不犹豫的按下它吧！！！这就是你以后经常需要触碰的仓库！![](http://upload-images.jianshu.io/upload_images/5875188-489861b0bb33638e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

因为我勾选了自动创建README，所以界面是这样的

![](http://upload-images.jianshu.io/upload_images/5875188-bea021cb4078c0d5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

**好了，到了这一步说明已经成功了一半，仓库建好了，那么我们怎么才能把这远程仓库能clone到我们本地呢？**
仔细的你一定看到了又出现了一个大绿色按钮，没错，这就是我们的主角！点开它，你会发现右上角有个**Use SSH**(这是个切换按钮，记得切换到SSH)

![](/images/GitHub/SSH.gif)

那么问题来了，[SSH](http://www.ruanyifeng.com/blog/2011/12/ssh_remote_login.html)是啥？我没有这玩意儿啊，该怎么办？不慌！这时候该我们的Git登场了！(blingbling滑稽)

# Git初体验
- 首先打开我们的Git Bash (安装成功)
- 因为Git是分布式版本控制系统，所以需要填写用户名和邮箱作为一个标识。

![](http://upload-images.jianshu.io/upload_images/5875188-cbcabe8f716ce752.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 然后我们可以查看我们电脑中是否已经存在过ssh，打下面两条命令就能看到，我已经安装过，所以显示存在，没有安装是显示不存在的。

![](http://upload-images.jianshu.io/upload_images/5875188-53df3ff31496f5ce.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 接下来我们[安装SSH](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/) `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`(**记得替换你自己的邮箱**),把这句代码输进Git中，它先要求你确认保存公钥的位置（.ssh/id_rsa），然后它会让你重复一个密码两次，如果不想在使用公钥的时候输入密码，可以留空，一直按回车结束，就成功了。

![](http://upload-images.jianshu.io/upload_images/5875188-65ae659d83cda2c9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 现在只需要我们去ssh目录下的id_rsa.pub中的钥匙给复制出来然后粘贴到GitHub的SSH中就行了

![](http://upload-images.jianshu.io/upload_images/5875188-317383ab7b5396a7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 回到GitHub中，点击我们的头像，然后下面会出现一个Settings。

![](http://upload-images.jianshu.io/upload_images/5875188-81559db0a745b145.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 如图点击New SSH key

![](http://upload-images.jianshu.io/upload_images/5875188-22764e975d7d473e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](http://upload-images.jianshu.io/upload_images/5875188-56190c8a443a6e19.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 好了，现在完成了我们的SSH创建，接下来我们就能clone我们的仓库到本地啦！

# Clone仓库到本地
- 回到我们的clone按钮，切换到SSH，并且复制这段地址

![](http://upload-images.jianshu.io/upload_images/5875188-4ad0fffb24619408.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 选好你想放仓库的文件夹位置，并且右键点git bash here，输入`git clone git@github.com:xxx/test.git`(后面改成你们的地址哦)

**然后静等仓库clone下来，然后就能愉快的玩耍GitHub啦！**
![](http://upload-images.jianshu.io/upload_images/5875188-14b8d5f3f434237c.gif?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

