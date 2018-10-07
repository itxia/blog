---
title: COMSOL Multiphysics 5.3a 安装教程
date: 2018-09-19 22:54:33
categories: 软件教学系列
tags: COMSOL
author: Yang Xu
---

个人感觉是史上最简单的安装教程了。

<!--more-->

## 下载
推荐使用校内FTP，详见[这里](/2018/09/17/UseFTP/#FTP%E7%AB%99%E7%82%B9%E5%9C%B0%E5%9D%80)。

## 安装

1. 双击下载得到的``COMSOL53_dvd.iso``挂载，点击``Setup.exe``，若弹出类似“是否允许此应用对你的计算机进行修改”这样的提示，选择``确定``即可。如图所示。
![fig1: setup](/figure/comsol/setup.png)

2. 待COMSOL安装程序打开后，选择``简体中文``并点击``下一步``(下文不再强调点击下一步这个动作)。点击``新安装COMSOL 5.3``。如图所示。
![fig2:new](/figure/comsol/new_inst.png)

3. 出现如下图所示的画面时：
![fig3.1:lic](/figure/comsol/select_lic1.png)
   - 第一步：点击``我接受 ... ``
   - 第二步：点击``许可证格式``后的下拉菜单，选择``许可证文件``。
   - 第三部：点击下一行的``浏览``，找到一同下载的文件夹中的``LMCOMSOL_Multiphysics_SSQ.lic``文件并确定。如下图所示。
![fig3.2:lic2](/figure/comsol/select_lic2.png)

4. 在这一步选择你需要安装的组件，一般地，全部勾选即可。在右侧可以选择安装的位置，你可以根据喜好修改。
![fig4:inst_path](/figure/comsol/set_inst_path.png)

5. 在这一步，需要确保``安装完成后检查更新``和``启用自动检测更新``前面的复选框**不被勾选**。其余选项可以根据个人喜好设置。
![fig5:update](/figure/comsol/disable_auto_update.png)

6. 在这一步设置``LiveLink``，这是COMSOL与其它软件，如``MATLAB``，进行协同工作的功能。如果已经安装了那些软件，你可以设置一下；没有安装也可以以后设置。因此如果不懂可以选择都不设置。
![fig6:livelink](/figure/comsol/livelink.png)

7. 检查无误即可开始安装，等待时间可以洗几件衣服。
![fig7:inst](/figure/comsol/inst.png)

8. 安装完成后，点击``关闭``即可。
![fig8:exit](/figure/comsol/finish.png)

9. 最后，不要忘了将挂载的iso文件弹出。在``此电脑``中``右键`` - ``弹出``即可，如图所示。
![fig9:eject](/figure/comsol/eject.png)

至此安装完成。
