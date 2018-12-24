---
title: 搭建GitHub+Hexo博客
date: 2018-12-24 21:32:58
tags: tech
category: 人生经验
top: true
author: "Yang Xu"
---

把搭建本博客的过程和坑记录一下，方便以后维护。也可以用于搭建自己的博客。

<!--more-->

## 简略版

### 安装
1. 安装``Git``、``node``、``Hexo``。
<!--Linux/MacOS用户就不用说了，有方便的命令行方式；Windows用户可以去对应的官网下载安装包，或者使用scoop/chocolatey这样的包管理器。-->
1. ``git clone ``blog这个repo。(如果是搭建自己的博客，可以先fork再clone。)
1. ``cd blog/HEXO``
1. ``npm ls --depth 0``，会提示缺少一些东西，用``npm install --save xxx``安装完成。
1. (如果是搭建自己的博客，需要配置一下``/_config.yml``文件，从上往下依次包括``Site``、``URL``、``theme``、``Deployment``。应该不难理解，如果不懂可以看下面详细版的两篇文章。)

### 用法
博客文章存放于``/source/_post/``里面。(如果是要写自己的博客，你可以删掉里面的``.md``文件。)

1. 新建一篇文章。``hexo new test``。``test``是你的文章名字(不一定是标题)，最好不要有空格。
1. 编辑``/source/_post/test.md``文件，写你想写的。
1. 生成文件。``hexo generate``，等待。
1. 启动本地预览。``hexo server``，按提示在浏览器中打开``http://localhost:4000``即可。可以使用``hexo server --debug``，这样修改md文件并保存后可以热更新。
1. 提交到GitHub。本地预览完毕，没有错误，可以提交。``hexo deploy``。

注：以上的几个hexo命令可以简写为首字母，如``hexo n test``、``hexo g``、``hexo s --debug``、``hexo d``。如果你对修改很有信心不要预览直接提交，可以``hexo d -g``。

## 详细版
请查看[简书文章1(总体搭建)](https://www.jianshu.com/p/465830080ea9)、[简书文章2(关于NexT主题)](https://www.jianshu.com/p/5d5931289c09)，然后再看上面的简略版。
