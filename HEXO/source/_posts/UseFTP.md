---
title: FTP使用教程(及其它零碎问题解答?)
date: 2018-09-17 14:06:27
categories: 软件教学系列
tags: FTP
top: true
author: "Yang Xu"
---

建议先看这一篇再去下~~崽~~载。

<!--more-->
# FTP使用教程

## 简介
FTP是File Transfer Protocol (文件传输协议) 的首字母缩写。顾名思义，它可以用来传输文件。本文所说的FTP特指校园网下的FTP。原因见下。
相比其它的下载方式，校内FTP的最大优点就是一个字：**快**！这是因为使用了内网。亲测**使用网线**下载文件可以获得10Mb/s的起步价。历史上最快观察到80Mb/s的峰值速率。
相比于紫荆需要分享率达标才能下载部分资源；相比与网盘的龟速，FTP的优点是显而易见的。当然，FTP也有其缺点，由于缺少专人维护，FTP上的资源可能很久不能更新，FTP服务器处于野生状态，地址可能会变化等等。~~但是这并不能影响我用FTP啊。~~

## FTP站点地址
> - [diisquare](ftp://ftp.diisquare.com) (匡院学术部维护，有一段时间未更新) ``ftp://ftp.diisquare.com``
- [zzrserver](ftp://114.212.170.211) (xy维护，内容**相对**最全最新) ``ftp://114.212.170.211``
- [kymCR](ftp://114.212.165.143) (匡院院楼机房，不稳定，内容较全较新) ``ftp://114.212.165.143``

## 使用方法

### 方法一：用 Windows 资源管理器
你可以通过打开``此电脑``或任意一个文件夹来开启 Windows 资源管理器 (快捷键 ``Windows + E``)。如图所示，(首先接上校园网，最好是网线) 在文件夹的地址栏输入FTP的地址，比如``ftp://114.212.170.211``，回车即可打开。
![fig1:connect](/figure/ftp/InputAddress.png)
找到你想要下载的资源，比如图中的这个``KerbalSpaceProgram 文件夹``，复制；
![fig2:copy and download](/figure/ftp/copy.png)
然后粘贴到自己的电脑里，等待下载即可。
![fig2:copy and download](/figure/ftp/paste.png)

### 方法二：用浏览器
大多数浏览器都可以打开FTP站点，以Chrome为例，在地址栏输入FTP的地址，回车打开，找到你想要下载的**文件**，右键下载即可。注意这个方法的缺点是不能下载一整个文件夹。
![fig3:download](/figure/ftp/download.png)

### 方法三：用下载工具
学校的基础计算机课程有个课程FTP站点用于下载课程资料和上传作业。老师让我们使用一些FTP工具，如``FlashFXP``来连接到FTP站点，由于~~没有安装~~年代久远，我就没截图。如果想用，下载安装即可，具体可以百度/谷歌。
