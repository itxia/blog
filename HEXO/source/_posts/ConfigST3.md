---
title: 配置Sublime Text 3
date: 2018-09-12 08:00:00
categories: 软件教学系列
tags: Sublime
---

好像这里必须放一句话才能出现“阅读全文”…

<!--more-->

<center>\~~Author: Song Gao~~</center>

## 概述

[Sublime Text 3](https://www.sublimetext.com/)是一款强大的**收费版**轻量级纯文本编辑器（即便如此，用户依旧可以无限期地免费试用，软件只会以一个非常低的频率提醒你购买），其**启动速度快**，**代码高亮效果好**，配合插件[LaTeXTools](https://github.com/SublimeText/LaTeXTools)以及PDF预览器[Sumatra PDF](https://www.sumatrapdfreader.org/free-pdf-reader.html)可以高效而方便地满足LaTeX的日常使用需求。在经过配置后，可实现**反向搜索**、**公式预览**等方便快捷的功能。

为表述方便，以下Sublime Text 3均简称ST3。

## 下载与安装

[点此](https://www.sublimetext.com/3)可选择ST3下载版本，我们以`Windows 64 bit`的安装版为例，下载后直接安装即可。其界面如图：

![Figure 1](/figure/st3/1.png)

[点此](https://www.sumatrapdfreader.org/download-free-pdf-viewer.html)可选择Sumatra PDF下载版本，同样以`64-bit`的安装版为例，下载后直接安装即可。其界面如图：

![Figure 2](/figure/st3/2.png)

当然，也可以选择便携版，下载后直接解压即可使用。

## 配置

### 安装Package Control

[Package Control](https://packagecontrol.io/installation)可用来为ST3安装各类功能强大的插件，通过<code>Ctrl + `</code> 打开控制台，复制以下命令并回车，即可自动完成安装。

```
import urllib.request,os,hashlib; h = '6f4c264a24d933ce70df5dedcf1dcaee' + 'ebe013ee18cced0ef93d5f746d80ef60'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

在`Preference`菜单栏里，我们可以看到多出了`Package Settings`和`Package Control`两项，说明安装已完成。

![Figure 3](/figure/st3/3.png)

### 安装LaTeXTools

使用快捷键`Ctrl+Shift+P`调出，输入`install`并回车，待加载完毕后查找`LaTeXTools`并回车即可开始安装，安装完毕会弹出消息框。

![Figure 4](/figure/st3/4.png)
![Figure 5](/figure/st3/5.png)
![Figure 6](/figure/st3/6.png)

选择`Preference->Package Settings->LaTeXTools->Settings-User`，若出现提示框则点击确定。

![Figure 7](/figure/st3/7.png)
![Figure 8](/figure/st3/8.png)

打开后使用`Ctrl+F`查找`Windows`，根据注释的提示修改`209-225`行的内容。

`texpath`填写`(texlive所在位置)\\bin\\win32;$PATH`；`distro`填写`texlive`；`sumatra`填写SumatraPDF的安装位置，然后保存。（注意`\`应该使用转义符`\\`）

![Figure 9](/figure/st3/9.png)

到了这一步，就可以使用ST3编辑tex文档并编译了，并且编译的结果会用SumatraPDF自动打开。首次编译时`Tools->Build System`选择`LaTeX`或`Automatic`，并且`Build With`选择`LaTeX - XeLaTeX`，以后只需使用`Ctrl+B`的快捷键。使用SumatraPDF打开的文档依旧可以进行写入，并且会更新编译的结果。ST3与SumatraPDF配合使用的界面如下。

![Figure 10](/figure/st3/10.png)

### 反向搜索

反向搜索是SumatraPDF自带的一项功能，在pdf文档内双击我们需要修改的内容，在编辑器内插入符就会跳到内容所在的段落，十分方便。

点击SumatraPDF左上角按键，选择`设置->选项`，反向搜索命令行内填入`"(ST3所在位置如C:\Program Files\Sublime Text 3\sublime_text.exe)""%f:%l"`，如果使用的是其他编辑器，也可以同理进行修改。

![Figure 11](/figure/st3/11.png)

### 公式预览

`LaTeXTools`是自带公式预览的，但在实际使用中我们往往会遇到图中的问题。

![Figure 12](/figure/st3/12.png)

解决方法是添加名为`GS_LIB`的环境变量，打开环境变量编辑的最方便的方法是直接搜索“环境变量”等字眼，点击右下角的`环境变量…`，在下半栏系统变量中点击新建，变量名填`GS_LIB`，变量值为`...\tlpkg\tlgs\Resource\Init;...\tlpkg\tlgs\kanji`，其中`...`表示`texlive`的实际安装位置。可以先通过资源管理器找到这两个目录然后将它们复制过来，中间用分号隔开。

之后重启ST3，问题得以解决。

![Figure 13](/figure/st3/13.png)

### 自动补全

使用`Package Control`搜索安装`LaTeX-cwl`，重启后就能实现自动补全功能，下面是效果图。

![Figure 14](/figure/st3/14.gif)

## 其他的LaTeX编辑器

除了VS Code、ST3这两款及其他相近的功能强大的编辑器外，也有一些仅适用于LaTeX的类似IDE的编辑器，它们通常安装之后即可使用，无需繁琐的配置。其中比较著名的有WinEdt、TeXstudio、TeXworks、LyX等。

##### WinEdt

在过去数年里，TeX发行版的安装并没有现在这么容易，有人将其打包封装并取名[CTEX](http://www.ctex.org/HomePage)，并附带了一些使用说明文档，为众多入门者所使用（由于长久未更新，现已不推荐安装）。[WinEdt](http://www.winedt.com/)作为其中最主要的编辑器，也获得了许多受众。这款编辑器是面向新人的，因为它有大量的功能按键以辅助对命令尚不熟悉的新人，而使用熟练后，这些按键反而成了累赘，毕竟纯键盘操作的效率比之更高。

事实上，WinEdt是一款**收费**编辑器，如果你使用的是最新版本且不曾购买的话，会很恶心地发现每次打开都会跳出来提示你购买软件，使用中途同样也会跳出来打算你的思路。因此它被笔者卸载了。（此处并无诋毁收费软件之意。）

##### TeXstudio

[TeXstudio](https://www.texstudio.org/)是一款跨平台的免费开源软件，其自带预览功能，使用起来比较方便。

##### TeXworks

[TeXworks](http://www.tug.org/texworks/)是`texlive`自带可选择安装的轻量级编辑器，界面非常简洁，功能相对简陋。

##### LyX

这里特意提到[LyX](https://www.lyx.org/)是因为它是一款WYSIWYG（What You See Is What You Get，所见即所得）的编辑器，使用方法与word相近。

更多的编辑器的对比可以参考[维基百科](https://en.wikipedia.org/wiki/Comparison_of_TeX_editors)。

## 参考

1. https://www.jianshu.com/p/72fe0ec0ab4e
2. https://www.jianshu.com/p/fee3fa234626
3. https://blog.csdn.net/enjoyyl/article/details/50057491
4. https://www.zhihu.com/question/19954023

