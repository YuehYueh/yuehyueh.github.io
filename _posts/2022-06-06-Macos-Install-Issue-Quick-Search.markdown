---
layout:     post
title:      "Macos Install Issue Quick Search"
subtitle:   " \"Insatll software\""
date:       2022-06-06 12:00:00 +0800
author:     "Yueh"
#header-img: "img/.jpg"
tags:
    - Macos
---
## Steps
1. Press Command+Space, type “Terminal”, and press Enter to launch one. Or, you can open a Finder window and head to Applications > Utilities > Terminal.
2. Run the following command in the Terminal window and provide your password:
   >sudo spctl --master-disable           
3. After you do, head to System Preferences > Security & Privacy. You'll find that the old “Anywhere” option has returned and is enabled.

---
### 一、允许“任何来源”开启**
苹果从macOS Sierra 10.12 开始，已经去除了允许“任何来源”的选项，如果不开启“任何来源”的选项，会直接影响到无法运行的第三方应用。

所以开启“任何来源”的方法如下：
打开【启动台】，选择【终端】，输入：
>sudo spctl  --master-disable

然后回车，继续输入密码（密码输入时是不可见的），回车。
接着打开【系统偏好设置】，选择【安全性与隐私】，选择【通用】，可以看到【任何来源】已经选定。
接着打开文件进行安装



### 二、发现还是显示“已损坏，无法打开。 您应该将它移到废纸篓”，不急，接下来用这种方法：**
在终端粘贴复制输入命令（注意最后有一个空格）：

>sudo xattr -r -d com.apple.quarantine   

先不要按回车，先不要按回车，先不要按回车，先不要按回车！
然后打开访达进入 “应用程序” 目录，找到该软件图标，将图标拖到刚才的终端窗口里面，会得到如下组合(如图所示)：

>sudo xattr -r -d com.apple.quarantine /Applications/WebStrom.app

回到终端窗口按回车，输入系统密码回车即可。
接着重新打开安装软件，就可以正常安装了


---

## End
-Yueh 6,June,2022 In Kuala Lumpur