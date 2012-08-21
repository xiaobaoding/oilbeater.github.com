---
---
layout: post
title: "VS2008编译Qtwebkit"
description: "为了证明自己这一个月没有打酱油，不过一个月写出这么个环境搭建的东西也只能证明我打酱油了，也为了回去能把环境搭起来，还是写那么两笔吧。"
category:
tagline: "Hack the life"
tags: [webkit]
img: "http://lh6.googleusercontent.com/-Z7ZgfMMC0ug/UDLqG1HYL_I/AAAAAAAAAVk/0BlqB3-i35Q/s215/webkit.png"
---

published: false
---

 为了证明自己这一个月没有打酱油，不过一个月写出这么个环境搭建的东西也只能证明我打酱油了，也为了回去能把环境搭起来，还是写那么两笔吧。官方的安装指导在[这里](http://trac.webkit.org/wiki/BuildingQtOnWindows)但是按照这个指导是肯定编译不过去的，所以还是看我的吧。安装环境的过程其实一点也不麻烦
### 安装VS2008
 官方链接在[这里](http://www.microsoft.com/zh-cn/download/details.aspx?id=3713)第一次找的时候不知道为什么脑抽筋直接下了一个MSDN，装完后还傻傻的找启动程序在那里？在哪里？
### 安装Qt for VS2008
 网上很多教程都说要自己从编译Qt，实践证明直接用安装包就好了，链接在[这里](http://qt.nokia.com/downloads/windows-cpp-vs2008)安装好后记得要在环境变量PATH里把qt安装目录下面的bin路径加入到PATH中，因为vs编译的时候需要找到qmake的路径。
### 下载pthread
 不知道为什么里面会用到pthread这种和平台相关的库，不过好在pthread现在也有windows平台的了，链接在[这里](ftp://sourceware.org/pub/pthreads-win32/pthreads-w32-2-9-1-release.zip)
将 pthreadVC2.lib  pthreadVC2.lib 和pthread.h （看一下是x86版还是x64版）扔到qt安装目录下的lib中
### 安装GUN 工具包
**记住安装路径中不能有空格** 
由于某些众所周知的原因下面的链接可能打不开

* [Bison](http://gnuwin32.sourceforge.net/downlinks/bison.php)
* [GPerf](http://gnuwin32.sourceforge.net/downlinks/gperf.php)
* [Grep](http://gnuwin32.sourceforge.net/downlinks/grep.php)
* [Flex](http://gnuwin32.sourceforge.net/downlinks/flex.php)
* [Libiconv](http://gnuwin32.sourceforge.net/downlinks/libiconv.php)

然后记得在PATH中加入他们的bin文件夹路径
###安装Python 和 Perl
由于编译的时候要执行许多脚本生成代码，又由于他们不是用一个语言写的所以这两个都要装。
Perl在[这里](http://www.activestate.com/activeperl/downloads)
Python 需要2.x版，链接在[这里](http://www.python.org/download/)由于某些众所周知的原因你可能打不开。然后再把python的安装路径和perl的bin路径加到PATH中就不需要再安装别的东西了。需要安装的东西一点也不多。
