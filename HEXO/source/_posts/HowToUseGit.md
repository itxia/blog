---
title: 如何使用Git和GitHub
date: 2018-09-08 14:08:10
tags:
---

## 参考
《GitHub入门与实践》[日]大塚弘记

<!--more-->

## 安装Git
1. 到[Git官网](https://git-scm.com/downloads)下载与你正在使用的操作系统(本文以windows为例)相对应的文件。一般地，选择``64-bit Git for Windows Setup``。
2. 安装时注意：勾选添加git到环境变量；在``Windows Explorer Integration``中勾选``Git Bash Here``。其余配置默认即可。
3. 安装完成后(可能需要注销或重启)，在任意一个文件夹空白处右键，检查是否有``Git Bash Here``的选项。

## 注册GitHub
1. 到[GitHub官网](https://github.com)注册一个账号，为方便下文举例，我们取邮箱为`` test@smail.nju.edu.cn ``，用户名为`student`。

## 配置git与github关联
1. 设置邮箱和用户名
打开``Git Bash``(输入命令均在Git Bash中进行，以后不再声明)，分别输入下列命令(输入一行命令后需要回车，以后不再声明)：

```shell
git config --global user.name "student"
git config --global user.email "test@smail.nju.edu.cn"
```
下面这一行设置可以增强输出命令的可读性：

```shell
git config --global color.ui auto
```
2. 用ssh生成公钥
输入：

```shell
ssh-keygen -t rsa -C "test@smail.nju.edu.cn"
```

回车之后会出现如下所示的输出，直接按回车即可：

```shell
Generating public/private rsa key pair.
Enter file in which to save the key
(/Users/your_user_directory/.ssh/id_rsa): (按回车键)
Enter passphrase (empty for no passphrase): (按回车键)
Enter same passphrase again: (按回车键)
```

这样密钥文件就生成了，默认在用户目录下，如：``C:\User\xxx\.ssh\``这个文件夹中。其中的xxx是你的windows用户名。

3. 将公钥添加到github中
 (1). 在``C:\user\xxx\.ssh\``文件夹中找到``id_rsa.pub``这个文件，用文本编辑器(如记事本)打开，复制里面的所有内容。
 (2). 登陆github账号，点击头像旁的小三角展开，点击``settings``-``SSH and GPG keys``-``New SSH key``，在``Title``中取一个名字，``key``中粘贴你刚刚复制的内容。然后点击``Add SSH key``即可。

4. 测试是否关联成功
输入：

```shell
ssh -T git@github.com
```

出现以下结果即为成功：

```shell
Hi student! You've successfully authenticated, but GitHub does not provide shell access.
```

## 日常使用
常用命令

```shell
git status
git add xxx
git commit -m "xxxxxx"
git push -u origin mater
```
