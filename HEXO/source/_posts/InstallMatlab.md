---
title: "安装Matlab R2018a"
date: 2018-09-10 08:00:00
categories: "软件教学系列"
tags: Matlab
author: "Chang Ma"
---

整个安装、测试过程约花费30\~60分钟，请合理安排时间。

<!--more-->

<center>\~~Author: Chang Ma~~</center>

# MathWoks MATLAB & Simulink 安装指南

**本指南仅用于学习交流，在[这里](https://ww2.mathworks.cn/store)可以购买正版的 MATLAB。**

## 概述

本指南需要最基本的计算机使用知识，如打开指定的文件夹、复制 & 粘贴、单击下一步等。同时需安装 [7-Zip](https://www.7-zip.org/)、[WinRAR](http://www.winrar.com.cn/)、[Bandizip](https://cn.bandisoft.com/bandizip/) 或 [PeaZip](http://www.peazip.org/) 等解压缩程序中的至少一个并懂得如何使用。本文选用 MATLAB R2018a 的 Windows 版本为示例。其他版本 MATLAB 的安装方式与此版本相似，可以参考安装包所附的 Readme 文档和本指南进行安装和破解。本指南只适用于 64 位的 Windows 系统，并已经在数十台装有 64 位版本 Windows 10 的计算机上得到了成功验证。**除非安装者知道自己在做什么或者有足够理由，否则不建议改变本文所述的安装破解步骤**。本指南仅用于学习交流，笔者原则上不鼓励使用盗版软件。在科研工作中如果需要使用 MATLAB 也必须购买正版。在[这里](https://ww2.mathworks.cn/store)可以买到正版的 MATLAB。

## 下载和解压

一份安装包可以在[这里](https://pan.baidu.com/s/1zRLrmkt3sp3ikqfCCtnX3w)下载，其他版本的安装包可以从[紫荆站](http://zijingbt.njuftp.org/stats.html?id=106787)、[52 破解](https://www.52pojie.cn/thread-713048-1-1.html)和[百度](https://www.baidu.com)等网站获取。在下载百度网盘中文件时推荐使用 [BaiduPCS-Go](https://github.com/iikira/BaiduPCS-Go)、[PanDownload](https://www.pandownload.com/) 或 [SpeedPan](https://www.speedpan.com/) 等第三方百度网盘下载软件或者[百度网盘客户端](https://pan.baidu.com/download)进行下载。
在校园网环境下安装的同学可以选择从校内 FTP 下载安装文件以获得更快的下载速度，目前已知可用的校内 FTP 包括[匡院团学联 FTP](ftp://ftp.diisquare.com/software_lecture/Matlab/)、[xy维护的 FTP1](ftp://114.212.170.211/software/study/Science/MATLAB/Matlab2018aWin64/) 和[不是xy维护的且容易gg的 FTP2](ftp://114.212.165.143/software/study/Science_soft/MATLAB/MATLAB2018a/win/)（截止2018/9/14，团学联 FTP 中的软件还是 2016b 版本，请酌情选择。xy维护的 FTP1 里有最新的版本。）

<!-- > 编者注：也可以连接校园网后从校内FTP下载，速率很快，目前可用的站点有(引自[TeXLive安装教程](/2018/09/09/InstallTeXLive/#more))：
   - [匡院团学联FTP](ftp://ftp.diisquare.com)(亲生的，稳)
   - [一个野生的匡院FTP](ftp://114.212.170.211)(地址可能会变但由我维护，软件较新)
   - [另一个野生的匡院FTP](ftp://114.212.165.143)(地址极易变且经常被管理阿姨关机)等。
-->

下载后，**请将 R2018a\_win64\_dvd1.iso 和 R2018a\_win64\_dvd2.iso 进行解压，并将内容拷贝至同一文件夹中**。不少安装教程中推荐使用虚拟光驱软件进行挂载，但是虚拟光驱的使用较为麻烦，且经常出错。拷贝后的结果如下图所示：

<!-- 编者注：``Windows 10``可以直接双击挂载iso文件。如果不想解压占用过多硬盘空间，可以双击``dvd1.iso``点击``setup.exe``安装，到提示弹出dvd1插入dvd2时，弹出``dvd1.iso``，双击``dvd2.iso``挂载后，继续安装。需要确保``dvd1.iso``和``dvd2.iso``挂载时的盘符是一样的。关于挂载和弹出，可以参考TeXLive安装教程。如果不会挂载和弹出或是觉得可能搞不定，就按照作者的方法吧。-->

![fig1](/figure/matlab/fig1.jpg)

**请确保 dvd1 和 dvd2 两个文件位于同一文件夹中。**别忘了解压 MATLAB R2018a Win64 Crack.zip。


## 安装

打开 setup.exe，在选择*允许此应用对系统进行修改* 后，会弹出以下窗口：

![Fig2](/figure/matlab/fig2.jpg)

选择*使用文件安装密钥*，点击下一步；

![fig3](/figure/matlab/fig3.jpg)

选择*是*，点击下一步；

![fig4](/figure/matlab/fig4.jpg)

选择*我已有我的许可证文件安装密钥*，在输入框中输入 `09806-07443-53955-64350-21751-41297` （如果你在安装其他版本，你往往可以在破解包中的 readme.txt 中找到对应版本的安装密钥），点击下一步；

![fig5](/figure/matlab/fig5.jpg)

点击*浏览* 并在弹出窗口中选择安装目录，或直接点击下一步；

![fig6](/figure/matlab/fig6.jpg)

选择要安装的组件。请确保你所需要的组件已被勾选，或者保险起见，勾选全部组件。点击下一步。

![fig7](/figure/matlab/fig7.jpg)

最后一次对要安装的部分进行确认。点击*安装* 开始安装。

![fig8](/figure/matlab/fig8.jpg)

请等待直到安装完成。这一过程可能会持续 10 分钟或者更久，视硬盘读写速度和安装组件大小而定。这段时间可以拿来干点别的，比如搓一局炉石。若过程中弹出显示着*弹出 dvd1 并插入 dvd2* 的窗口，请检查自己之前是否按照描述的步骤操作，并自行解决问题。
	
出现这样的窗口后，点击下一步。

![fig9](/figure/matlab/fig9.jpg)

至此，安装结束。

![fig10](/figure/matlab/fig10.jpg)

## 破解

安装完毕后，可以开始破解步骤。
	
找到 MATLAB 的启动程序 matlab.exe（一般在安装目录的 bin 文件夹下）并打开，在选择*允许此应用对系统进行修改* 后，会弹出以下窗口：

![fig11](/figure/matlab/fig11.jpg)

选择*在不使用 Internet 的情况下手动激活*，点击下一步；

![fig12](/figure/matlab/fig12.jpg)

选择*输入许可证文件的完整路径 (包括文件名)*，点击浏览，找到 MATLAB R2018a Win64 Crack 文件夹下的 license_standalone.lic，点击下一步，激活完成。
	
在激活后，将 MATLAB R2018a Win64 Crack 文件夹下的 bin 文件夹复制到安装路径，并覆盖安装路径下的 bin 文件夹，即可完成破解。之后，打开安装路径下 bin 文件夹中的 matlab.exe，即可开始使用 MATLAB。

## 常见问题

Q：出现以下报错怎么办？

![fig13](/figure/matlab/fig13.jpg)

A：执行破解的最后一步，即 “将 MATLAB R2018a Win64 Crack 文件夹下的 bin 文件夹复制到安装路径，并覆盖安装路径下的 bin 文件夹”。

Q：出现 “请弹出 dvd1 并插入 dvd2” 的窗口，我弹出了 dvd1，也挂载了 dvd2，也没用，怎么办？

A：玄学问题。请取消安装，按照本文方法（解压光盘映像文件）重新安装。

Q：我是 32 位系统。

A：MATLAB 早已停止了对 32 位系统的支持。如果实在是换不了 64 位系统，去安装 MATLAB R2015a 吧，那个有 32 位版本的。

Q：Linux 系统怎么安装？

A：既然选择了 Linux 系统，就要有折腾 Linux 系统的觉悟。在[这里](https://pan.baidu.com/s/1YmTuh7fD0XttDPCRxV1PGg)可以找到一份 Linux 系统下 MATLAB 的安装包，你可以自己摸索着安装（安装过程是类似的，也可以在网上找到教程）。安装之后 Matlab 2018a Linux64 Crack.tar.gz 文件中有破解相关的说明。不要高兴的太早，很多 Linux 系统的发行版都会出现库问题和 jre 字体问题，这些都可以在谷歌得到解决。我的 Manjaro 格式化之前装了一份 MATLAB，但是被我格了。不然我就截图晒你一脸了。

Q：Mac OS X 怎么安装？

A：我手（mai）头（bu）没（qi）有 Mac 电脑，欢迎 Mac 用（you）户（qian）增（ren）补（song）本（wo）指（yi）南（tai）。

Q：我装完了。但我一点都不会用。

A：你可以在命令行窗口（就是打开 MATLAB 最中间的那个）随便输点什么体验体验，比如 2\*5 之类的。如果时间允许，欢迎参加匡院学术部和开物社举办的软件学习讲座，加这个群 `674580668` 可以了解详情。MATLAB 的帮助文档很丰富，如果有什么不清楚可以直接查阅。各种 MATLAB 书籍（我推荐郑智波翻译，David McMahon 编著的《MATLAB 揭秘》和谢中华的《MATLAB 从零到进阶》）和网上教程也是不错的选择。

---
<center>\~~Editor: Yang Xu~~</center>
