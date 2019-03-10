---
title: 配置VSCode
date: 2018-09-10 12:35:42
categories: "软件教学系列"
tags: vscode
author: Yang Xu
---

超简短一键式配置(那是以前的版本...)

<!--more-->

# VSCode的安装与配置

## 概述
VSCode，全称``Microsoft Visual Studio Code``，下文径称vscode(因为懒得打大写字母)，是一款微软公司出品的开源编辑器。它比IDE轻量，功能又比普通的文本编辑器强大，依赖丰富的插件实现足够胜任日常所需的功能。

## 下载
到[vscode官网](https://code.visualstudio.com/Download)下载对应你使用的系统的版本。下面我们以``Windows 10 64 bit``的``User Installer``为例。

## 安装
双击下载得到的``VSCodeUsrSetup-xxx-xxx.exe``文件，一直点击下一步即可。安装完成后打开vscode。如图所示。
![fig1](/figure/vscode/1.png)

## 配置（仅以LaTeX为例）
### 设置中文界面（非必须）
1. 点击上图左侧红框处的按钮(或者按快捷键：``Ctrl+Shift+X``)，打开扩展页面。在搜索框里输入``Chinese``，找到如图所示的中文语言包，选择``Install``等待安装。

   ![fig_zh1](/figure/vscode/zh1.png)

1. 安装完毕会出现如下图的提示，点击``Restart Now``即可。如果发现界面还是英文，那么就参照上图中红框里的``使用方法``进行设置。

   ![fig_zh2](/figure/vscode/zh2.png)

1. 其中文界面如下图所示：

   ![fig_zh3](/figure/vscode/zh3.png)

### 安装配置``LaTeX Workshop``插件
1. 再次点击``扩展``按钮，在搜索框中输入``LaTeX Workshop``，选择如图所示的插件，点击安装。(请无视这里的界面语言，因为截屏的顺序不同)。

   ![fig3](/figure/vscode/3.png)

1. 安装完毕，出现提示``Reload/重新加载``，点击即可。

   ![fig4](/figure/vscode/4.png)

1. 按快捷键``Ctrl+Shift+P``，打开命令面板(这也以后极为常用的快捷键，要记住)。输入``settings``，在出现的候选列表里点击``首选项：打开设置 (JSON)``或``Preferences: Open Settings (JSON)``，如图所示：

   ![fig5](/figure/vscode/5.png)

1. 在出现的``用户设置``这个文件里，把以下内容复制粘贴进去，并保存：
   ```json
   "latex-workshop.latex.magic.args": [
     "-synctex=1",
     "-interaction=nonstopmode",
     "-file-line-error",
     "-shell-escape",
     "%DOCFILE%"
   ],
   "latex-workshop.latex.recipes": [
     {
       "name": "xelatex",
       "tools": [
         "xelatex"
       ]
     },
     {
       "name": "xelatex -> bibtex -> xelatex*2",
       "tools": [
         "xelatex",
         "bibtex",
         "xelatex",
         "xelatex"
       ]
     }
   ],
   "latex-workshop.latex.tools": [
     {
       "name": "latexmk",
       "command": "latexmk",
       "args": [
         "-synctex=1",
         "-interaction=nonstopmode",
         "-file-line-error",
         "-shell-escape",
         "-pdf",
         "%DOCFILE%"
       ]
     },
     {
       "name": "xelatex",
       "command": "xelatex",
       "args": [
         "-synctex=1",
         "-interaction=nonstopmode",
         "-file-line-error",
         "-shell-escape",
         "-pdf",
         "%DOCFILE%"
       ]
     },
     {
       "name": "bibtex",
       "command": "bibtex",
       "args": [
         "%DOCFILE%"
       ]
     }
   ],
   ```
   ![fig6](/figure/vscode/6.png)

<!--
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
-->

至此就配置完成啦。

## 测试
1. 在Vscode里打开一个文件夹(快捷键：``Ctrl+k``再按``Ctrl+o``)，如图所示：
   ![fig7](/figure/vscode/7.png)

1. 新建一个tex文件或者打开你已有的tex文件，写一些内容。你会发现，当检测到编辑的是tex文件时，vscode的左侧出现了一个``TEX``的按钮，点击它就会出现一些tex工具，方便编译、查看pdf等操作。

   ![fig9](/figure/vscode/9.png)

1. 不过，通常来讲，我更喜欢把左侧的这些栏隐藏。在如图所示的菜单里可以设置隐藏和显示。

   ![fig10](/figure/vscode/10.png)

1. 我正常使用的时候，喜欢分屏，vscode和SumatraPDF各占一半。使用``Ctrl+Shift+P``输入``LaTeX Workshop``可以查看各个命令及快捷键，如图所示。编译的快捷键是``Ctrl+L Alt+B``，``L Alt``表示左侧的``Alt``键。

   ![fig11](/figure/vscode/11.png)

vscode有很多快捷键，你可以在``文件(F)`` - ``首选项(P)`` - ``键盘快捷方式``中查看。

<center>\~~Author: Yang Xu~~</center>
