---
layout: post
title: Windows可以上网但Ubuntu上不了
date:   2014-08-27 15:32:24
categories: Ubuntu
---

同样一根网线，没有插拔，在win7下面可以正常使用，但是在Ubuntu下面就没法使用了（灯都不亮）。

首先排除连接的问题，因为win7下面是可以正常上网的。所以不妨尝试一下重设端口。

    sudo ifconfig eth0 down
    sudo ifconfig eth0 up
    sudo mii-tool -F 10baseT-HD eth0

正常情况下在执行第一句后灯会亮起，执行第二句后灯会熄灭，执行第三句后会重新亮起，然后就可以正常使用了。

但是这种方法每一次重启都需要重新打这三行，如果觉得麻烦可以把它写入开机脚本，这里不详述。
