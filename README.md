KKDaemon - Very easy tool for automation
==========================================

KKDaemon是一个简单Windows托盘工具，帮助程序开发者方便地执行他们的自动化脚本。

![KKDaemon](https://raw.githubusercontent.com/mr-kelly/KKDaemon/master/screenshot.png)

起因
-------
作为一名开发者，每天工作一些频繁的动作是什么？ 

*编译* : 弱点的，打开IDE，点编译，然后等；强点的，打开浏览器，输入JIRA(或类似)网址，选择编译项目，编译。

*资源打包或压缩* : 弱点的，真实游戏开发团队个案，美术打包工程文件，压缩，然后发给策划，打开游戏编辑器，点击打包资源，然后svn上传，程序测试~~~我的妈呀。

*打开文件夹*：双击我的电脑，再n次双击找文件夹，层次很多啊；或者用TotalCommander, 寻找锁定的标签，双击打开，标签很多啊。别小看这类东西，我遇到不少美术人员会为这个搔爆头。

*等等....*

我比较偷懒，一直想找一种方法，以最少的行为动作就能实现我的目的。
从自然法则来说，最好的方法就是通过“脑电波”控制计算机了，可是时代还没进步到这个地步。

这让我萌生了，做一个小工具解决问题的想法。



功能
-----------------------

* 打开KKDaemon/bin/Debug/KKDaemon.exe执行程序后，右下角出现托盘图标。
* 按下快捷键Alt + ~ 或 Ctrl + ~，弹出脚本选择菜单。
* KKDaemon/bin/Debug/config.json是配置文件
* 可以配置时间和消息，间隔时间出现冒泡消息

目前支持自定义Python脚本，日后添加NodeJS脚本引擎，内置一个py.exe绿色python


开发平台
-----------------
Visual Studio 2012 + .Net Framework 3.0 WPF

老的Python版
-------------------------
原名KKScriptHelper， 使用Python + wxPython + py2exe开发。遇到一些兼容性问题，加之API有限，改用.net framework 3.0的WPF， Windows 7后免框架安装。

现状
-----------------------
目前游戏团队使用这个简单的工具，进行数据表编译、翻译字段搜寻和工程目录打开功能。
其中最常用的是数据表编译，我们使用Excel表编辑，通过KKDaemon快速执行Python脚本，把Excel表转换成Tab文本文件。

未来
--------
* 与服务器进行通讯，实现公司内部的基本信息广播
* 使用IronPython替代CPython