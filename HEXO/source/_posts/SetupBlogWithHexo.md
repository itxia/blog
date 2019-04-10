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

注：想要搭建自己的博客的，请看详细版。简略版主要是用于快速搭建此博客，自己的博客还是全新搭建比较好。

## 简略版(快速搭建此itxia博客)

### 安装
1. 安装`` Git ``、`` node (npm) ``、`` Hexo ``。
   以下命令仅作示例（Ubuntu 18.04）：
   ```shell
   sudo apt install git nodejs
   # Maybe you need to install 'npm' separately
   # Strongly recommened in China:
   # sudo npm config set registry https://registry.npm.taobao.org
   sudo npm install --unsafe-perm --verbose -g hexo-cli
   # to verify installation
   hexo -v
   ```
1. 克隆该博客仓库及hexo相关操作
   ```shell
   git clone git@github.com:itxia/blog.git
   cd blog/HEXO
   # Ensure 'package.json' exists in this directory before doing the next
   npm install
   ```
   <!-- 1. `` npm ls --depth 0 ``，会提示缺少一大堆东西，用`` npm install --save xxx ``安装完成；不过似乎只要安装`` install.sh ``里的东西就够了，如果你的网速很快也可以一个个慢慢装。-->

### 用法
博客文章存放于`` /source/_post/ ``里面。(如果是要写自己的博客，你可以删掉里面的`` .md ``文件。)

1. 新建一篇文章。`` hexo new test ``。`` test ``是你的文章名字(不一定是标题)，最好不要有空格。
1. 编辑`` /source/_post/test.md ``文件，写你想写的。
1. 生成文件。`` hexo generate ``，等待。
1. 启动本地预览。`` hexo server ``，按提示在浏览器中打开`` http://localhost:4000 ``即可。可以使用`` hexo server --debug ``，这样修改md文件并保存后可以热更新。
1. 提交到GitHub。本地预览完毕，没有错误，可以提交。`` hexo deploy ``。

注：以上的几个hexo命令可以简写为首字母，如`` hexo n test ``、`` hexo g ``、`` hexo s --debug ``、`` hexo d ``。如果你对修改很有信心不要预览直接提交，可以`` hexo d -g ``。

## 详细版(用于一般性的搭建)
请查看[简书文章1(总体搭建)](https://www.jianshu.com/p/465830080ea9)、[简书文章2(关于NexT主题)](https://www.jianshu.com/p/5d5931289c09)，然后再看上面的简略版。
这里给出一个步骤：
1. 安装
   ```shell
   sudo apt install git nodejs
   # Maybe you need to install 'npm' separately
   # Strongly recommened in China:
   # sudo npm config set registry https://registry.npm.taobao.org
   sudo npm install --unsafe-perm --verbose -g hexo-cli
   # to verify installation
   hexo -v
   ```
1. hexo初始化及安装必要的包
   ```shell
   cd <your_blog_dir>
   hexo init
   # Ensure 'package.json' exists in this directory before doing the next
   npm install
   ```
1. 搭建自己的博客，需要配置一下`` /_config.yml ``文件，从上往下依次包括`` Site ``、`` URL ``、`` theme ``、`` Deployment ``。应该不难理解，如果不懂可以看上述两篇文章。
