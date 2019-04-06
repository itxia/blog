---
title: 安装TeXLive
date: 2018-09-09 18:05:03
categories: 软件教学系列
tags: TeX
author: "Yang Xu"
---

整个安装、测试过程约花费1小时，请合理安排时间。

<!--more-->
# TeXLive安装及配置指南

## 下载
提供几个备选方案：

1. [官网](https://tug.org/texlive/)。
2. [清华大学镜像站](https://mirrors.tuna.tsinghua.edu.cn/)。
按如图所示的步骤下载iso文件。(最推荐。使用校园网，并接上网线速度更快)
![TUNA TeXLive](/figure/TeX/tuna_TeXLive.png)
3. 校内FTP。
使用校内FTP是最快的下载方式，但是可能存在版本老旧和地址易变的缺点，当然必须使用校园网才能连接。
请看[这里](/2018/09/17/UseFTP/#FTP%E7%AB%99%E7%82%B9%E5%9C%B0%E5%9D%80)。

下载后得到一个类似``texlive2018-20180414.iso``这个名字的文件就对了，叫做“光盘镜像文件”，以下简称``iso文件``。

## 安装
1. 如果你是``Windows 10``系统，那请直接双击这个``iso文件``打开它。如下图所示：
![Mount TeXLive](/figure/TeX/mount_TeXLive.png)
如果不是``Windows 10``系统，或是不能双击直接打开，也可以用解压软件将其解压后进行后续操作。此教程只针对``Windows``用户，``Mac OS``和``Linux``用户有更简单的命令行安装方法，请自行搜索。

2. 双击``install-tl-windows.bat``，稍等片刻会出现一个窗口，基本上只需要一路点击“下一步(Next)”即可。其中安装目录可以自选，为方便下文叙述，以默认安装目录``C:\TeXlive\``为例。

3. 等等等。安装过程十分漫长，你甚至可以去吃个晚饭或洗个澡。

4. 安装完成后，别忘了弹出这个``iso``镜像。
``打开此电脑`` - ``右键DVD驱动器: X (DVD Drive: X)`` - ``点击弹出(Eject)``。

## 配置
1. 配置TeXLive的二进制文件们。
   ``添加 C:\TeXlive\2018\bin 到 Path`` (方法见附录)
2. 安装SumatraPDF阅读器。(非必须，sumatra的优点是可以实时刷新pdf。)
   到[SumatraPDF官网](https://www.sumatrapdfreader.org/download-free-pdf-viewer.html)下载对应你电脑系统的安装包，如``SumatraPDF-x.x.x-64-install.exe``的这个文件。下载后，双击安装即可。
<!--   (2) 解压压缩包，将里面的``SumatraPDF.exe``复制粘贴到一个你记得的地方，你可以选择重命名以方便命令行使用。比如``C:\D\study\SumatraPDF\sumatra.exe``
   (3) ``添加 C:\D\study\SumatraPDF\sumatra.exe 到 Path``
-->

## 测试
新建一个TeX文件，随意写入内容。如``test.tex``：
```LaTeX
% !Mode:: "TeX:UTF-8"
% !TEX program  = xelatex %这两行不是必须的，但是建议加上
\documentclass{article}
\begin{document}
Hello, \LaTeX !
\end{document}
```

然后，在``test.tex``所在文件夹的空白处，``按住Shift``+``鼠标右键``，选择``在此处打开PowerShell窗口(Open PowerShell window here)``，输入``xelatex test.tex``并回车。运行完成后，若文件夹内出现``test.pdf``且用sumatra打开查看没问题，则说明TeXLive安装和配置均已成功！

在[另一篇文章](/2018/09/10/ConfigVSCode/)中会介绍配合``VScode``和``SumatraPDF``写LaTeX文档的方法。

## 附录(Appendix)
1. **定义函数** ``添加 ... 到 Path(Add ... to Path)`` ：
   (1) ``右键此电脑(This PC)`` - ``属性(Properties)`` - ``高级系统设置(Advanced System Settings)`` - ``环境变量(Environment Variables)``。
   (2) 选中``系统变量(System variables)``中的``Path``，点击``编辑(Edit)``
   (3) 点击``浏览(Browse)``，找到`` ... ``并选中它，点击``确定(OK)``。
   (4) 逐层点击``确定(OK)``返回。

2. **更新TeXLive** (建议做)
   引自[这里](https://mirror.tuna.tsinghua.edu.cn/help/CTAN/)。
   打开命令行(按``Windows + R``，输入cmd并回车)，逐行执行以下命令即可。如果提示权限问题，使用管理员权限运行命令行。(但是我的电脑上不需要管理员权限)
   ```shell
   tlmgr option repository https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/tlnet
   tlmgr update --self
   tlmgr update --all
   ```

3. FAQ
   1. 报错(最后是`` Goodbye ``，开头有`` spawn: cmd ``)
      - 原因：CTeX卸载不完全导致的
      - 解决：在环境变量里添加`` C:\Windows\System32 ``

---
<center>\~~Author: Yang Xu~~</center>
