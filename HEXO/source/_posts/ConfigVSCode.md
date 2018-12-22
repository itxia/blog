---
title: 配置VSCode
date: 2018-09-10 12:35:42
categories: "软件教学系列"
tags: vscode
author: Yang Xu
---

超简短一键式配置

<!--more-->

# VSCode的安装与配置

## 概述
VSCode，全称``Microsoft Visual Studio Code``，下文径称vscode(因为懒得打大写字母)，是一款微软公司出品的开源编辑器。它比IDE轻量，功能又比普通的文本编辑器强大，依赖丰富的插件实现足够胜任日常所需的功能。

## 下载
到[vscode官网](https://code.visualstudio.com/Download)下载对应你使用的系统的版本。下面我们以``Windows 10 64 bit``的``User Installer``为例。

## 安装
双击下载得到的``VSCodeUsrSetup-xxx-xxx.exe``文件，一直点击下一步即可。安装完成后打开vscode。如图所示。
![fig1](/figure/vscode/1_init.png)

## 配置
为了方便广大同学，避免繁琐的手动配置，我将借助``syncing``插件自动化完成配置过程。

1. 先点击左侧``Extensions``按钮，在搜索框中输入``syncing``，点击出现的第一个插件，确认与图中无误后，点击``Install``，等待插件安装完成。如下图所示。
![fig2](/figure/vscode/2_inst_syncing.png)

2. 此插件安装完成后，点击图中所示的``Reload``，等待vscode重新加载。
![fig3](/figure/vscode/3_reload_syncing.png)

3. Reload完成后，按快捷键：``Ctrl+Shift+P``，出现一个悬浮的命令窗口，输入``syncing``，选择出现的``Syncing: Download Settings``。如下图所示。
![fig4](/figure/vscode/4_syncing_dl.png)

4. 出现如图所示的``Enter GitHub Personal Access Token ... ``时直接按回车：
![fig5](/figure/vscode/5_syncing_token.png)

5. 出现如图所示的``Enter Gist ID``时，将这一串字符``9a5d7c4bd7242257bab8a3e6554989f1``复制粘贴进去，回车：
![fig6](/figure/vscode/6_syncing_gist.png)

6. 回车之后，界面右下角可能会出现如图所示的确认信息，只要点击``Confirm to download``即可。界面左下角可以看到``syncing``插件已经在工作了，会有下载的进度提示。
![fig7](/figure/vscode/7_syncing_confirm.png)

7. 当进度提示下载完成，界面右下角会弹出如图所示的提示，点击``Reload Now``，等待vscode重新加载即可。
![fig8](/figure/vscode/8_syncing_reload.png)

8. 重新加载完成后，vscode的界面就大概是这样，熟悉的中文界面！如果没有变成中文界面，请**退出**vscode再打开。
![fig9](/figure/vscode/9_final.png)

9. 还有一件事(不是必须的，如果你电脑上没有python那就不用进行这一步了)，我的配置文件里的python路径是我自己的电脑上的，如果你的电脑上的python路径与我的不同(~~嘤~~该是显然的)，那还需要单独修改一下python的路径。步骤如下：
   (1) 按快捷键``Ctrl+Shift+P``，输入``settings``，点击出现的``首选项：打开设置(JSON)``。如图所示。
   (2) 在右半边``用户设置``里面找到如图所示的python路径，把红框里的路径修改为你电脑上``python.exe``的路径。如果是``Windows``用户，记得把``\``改成``\\``。
![fig10](/figure/vscode/10_modify_PythonPath.png)

至此就配置完成啦。

vscode有很多快捷键，你可以在``文件(F)`` - ``首选项(P)`` - ``键盘快捷方式``中查看。编译LaTeX的快捷键是``Ctrl+B``。

---

可以与[TeXLive安装教程](/2018/09/09/InstallTeXLive/)配合，写一个测试LaTeX文档，按``Ctrl+B``编译。正常的工作状态如图，vscode和sumatra各占一半。
![fig11](/figure/vscode/WritingTeX.png)

---

<center>\~~Author: Yang Xu~~</center>
