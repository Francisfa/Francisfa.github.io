---
layout:     post
title:      Mac终端(zsh)下用sublimetext编辑器打开文件

subtitle:   转载自http://qiubaiying.top/
date:       2018-07-01
author:     WF
header-img: img/post-wf-mac.jpg
catalog: true
tags:
    - Mac
    - terminal
    - zsh
---

# 说明
 
 在前面 [blog](http://qiubaiying.top/2017/06/19/%E5%BF%AB%E9%80%9F%E9%85%8D%E7%BD%AEzsh/) 的学习中，学习了如果快速在终端用代码编辑器中打开文件的位置和目录，这是一个很高效率的小技巧，所以学习后记录一下。
 
# 正文

#### 查看自己的shell类型

打开mac终端，输入：

	$ cat /etc/shells
	
#### 安装 oh my zsh

	$ git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh  #克隆该软件
	$ cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc  #拷贝并且设置直接启动

重新打开终端，输入：
	
	$ zsh

可以切换终端。

#### 修改主题

	$ open ~/.zshrc 
<br>
	修改 `ZSH_THEME="robbyrussell"`，主题在 ~/.oh-my-zsh/themes 目录下。

可以[参照主题](https://github.com/robbyrussell/oh-my-zsh/wiki/themes)进行选择.

#### 设置为默认shell（`如果不设置也可以，每次都需要在终端再次输入zsh切换`）

	$ chsh -s /bin/zsh

#### 修改 `zsh` 配置文件

	$ open ~/.zshrc
	
在文件末尾加上这几行代码

	alias subl='/Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl'

#### 测试
使用 sublimetext 打开
	
	$ subl .

#### 补充
如果要用atom或者vcCode打开，则需要在配置文件中加入：

	alias atom='/Applications/Atom.app/Contents/MacOS/Atom'
	alias code='/Applications/Visual\ Studio\ Code.app/Contents/Resources/app/bin/code'

> 本文首次发布于 [BY Blog](http://qiubaiying.github.io), 作者 [@柏荧(BY)](http://github.com/qiubaiying) ,转载自 [BY Blog](http://qiubaiying.top/).