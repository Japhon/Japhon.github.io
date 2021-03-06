---
layout: post
title: Ubuntu开Wifi给Android手机用
date:   2014-08-28 15:12:55
categories: blog
dsid: 0003
tags: ["Ubuntu", "Android"]
abstract: 之前在使用Ubuntu的时候总是有一个问题，就是我开的Wifi（参照网上参考的教程）我自己的Android手机没办法用，但是舍友的苹果手机就可以用。但是我自己的Android手机却不能用了。google了一下，发现Android的手机是不支持Ad-hoc架构的。下面就来解决这个问题。
---

之前在使用Ubuntu的时候总是有一个问题，就是我开的Wifi（参照网上参考的教程）我自己的Android手机没办法用，但是舍友的苹果手机就可以用。但是我自己的Android手机却不能用了。google了一下，发现Android的手机是不支持Ad-hoc架构的。下面就来解决这个问题。

下面这个方法也适用于校园网用户（好吧，反正我也不知道其他校园网能不能用），我是使用yah3c上网的，这个方法是可行的。然后在实验室直接IP地址上网也是可以的。其他的大家自己试试看咯。

注意：你的电脑的无线网卡必须支持Access Point (AP) mode，如果不支持的话一切都白搭。下面默认你是支持的，如果不支持的话请寻找有没有其他的解决方法。

#### <b>第1步</b>

点击下载安装

请点这里→[kde-nm-connection-editor](apt://plasma-nm).

#### <b>第2步</b>

在终端中输入

    kde-nm-connection-editor

或在Alt+F2中搜索kde-nm-connection-editor并打开它

![kde-connect-manager](/photo/Build-Wifi-For-Andoid/kde-connect-manager.png)

#### <b>第3步</b>

点击“添加”（Add）按钮，然后选择“Wireless (shared)”

![create-wireless-point](/photo/Build-Wifi-For-Andoid/create-wireless-point.png)

#### <b>第4步</b>

输入“链接名”（connection name）和 “ssid”, 然后“模式”（mode）选择“Access Point”。 然后可以在“Wireless Security”这个选项卡中设置你的密码（可选）。最后点击“OK”.完成设置。

![create-wireless-point1](/photo/Build-Wifi-For-Andoid/create-wireless-point1.png)

#### <b>第5步</b>

在已经有线连接上网的情况下，点击“链接到隐藏的Wi-Fi网络” （Connect to Hidden Wi-Fi network）， 选择你之前设置的“链接名”。

![connect-to-wireless](/photo/Build-Wifi-For-Andoid/connect-to-wireless.png)

#### <b>第6步</b>

最后，你的链接菜单应该就像下图这样。

![wifi-hotspot-connected](/photo/Build-Wifi-For-Andoid/wifi-hotspot-connected.png)

这时所有的步骤都完成了，用你的Android手机链接你的Wifi试一试吧！

参考的地址[Share Internet Connection With Android in Ubuntu 14.04](http://ubuntuhandbook.org/index.php/2014/06/share-internet-with-android-ubuntu-1404/)我只是把网页中大概介绍的步骤提取出来，顺便翻译成中文，供大家参考。
