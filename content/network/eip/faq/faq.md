---
title: "常见问题"
description: Test description
draft: false
enableToc: false
---

## 公网 IP 流量计费的具体统计方法是什么？ {#id23}

如果公网 IP 的计费模式是按流量计费，则除了固定的 IP 地址价格外， 流量数据会每小时自动统计一次，统计方法是： 在即将扣费的时间范围内，分别对进、出数据量求和，然后取其中较大的值作为扣费依据。

为了保持跟带宽计费一致的优惠策略（请见： [山河的公网带宽上下行速率是对称相等的吗](#id17) ) ，只有当下行速率超出 10Mbps 时才会对其扣费。例如：

一个按流量计费的、带宽上限是 20Mbps 的公网IP，在一个扣费周期内有 30 分钟其下行速率一直保持在 18Mbps ，有 10 分钟其上行速率一直保持在 10Mbps ， 则在即将扣费的时间范围内对进、出数据量求和结果如下（这里为了方便举例， 上下行速率假设一直稳定在一个固定值，而实际计算时使用的是采样间隔为1分钟的速率数据）：

>
>
>进数据量之和 ＝ 8Mbps（18 Mbps 减去优惠的 10 Mbps） * 1800（秒数） / 8 = 1800 MB (megabyte)
>
>出数据量之和 ＝ 10Mbps * 600（秒数） / 8 = 750 MB (megabyte)
>
>

因为进数据量之和大于出数据量之和，所以此1小时的实际扣费是 1800 MB / 1024 * 流量单价（每GB ** 元）

警告

公网 IP 计费模式不能频繁切换，24小时内只能改一次。

## 云服务器绑定了公网 IP 之后，为什么我无法通过 IP SSH 登录，也不能 ping 通该 IP？ {#ip-ip-ssh-ping-ip}

为了加强位于基础网络 vxnet-0 中的云服务器的安全性， 山河在云服务器之前放置了一个防火墙（Security Group）。 初始状态下，每个防火墙都不包含任何规则，即，全部端口都是封闭的， 您需要建立规则以打开相应的端口。

>注解
>如果你的云服务器使用的是默认防火墙，那么 ping 和 ssh 的端口都是默认打开的，你无需再进行操作。

例如您需要访问云服务器的22号端口，需要手动为云服务器的防火墙添加一条 接受 tcp 22 端口 的下行规则，然后再点击 更新规则 使其应用到云服务器。

同理，如果你想开启 ping 功能， 需要在防火墙里头添加 接受 ICMP echo request 的下行规则。

## 欠费后的公网 IP 会被如何处理？ {#id22}

对于通过山河备案信息验证的公网 IP，我们会在欠费之后为用户保留 10 天， 并发出欠费提醒的邮件；对于不需要备案或备案信息没有通过验证的公网 IP， 一旦欠费就会被系统释放回资源池。

## 如果我有多台云服务器需要访问外网，是不是每台云服务器都需要绑定一个公网 IP？ {#ip}

当然不是这样。您可以将需要访问外网的云服务器加入到您的某个受管私有网络中， 再将该受管私有网络连接到您创建的路由器上， 然后再给路由器上绑定一个公网 IP。这样， 位于受管私有网络中的所有云服务器都可以连接互联网了，既节省钱，也节约 IP 地址。