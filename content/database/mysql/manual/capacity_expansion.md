---
title: "扩容集群"
description: test
weight: 3
draft: false
---


shanhe 云数据库MySQL Plus 云数据库支持对运行中的数据库服务进行在线扩容，调整CPU/内存/磁盘空间大小。

## 创建扩容

1. 选择目标集群，点击**扩容集群**。
2. 配置需要扩容的角色以及扩容后的规格。
3. 点击提交即可完成扩容。
   
> **注意**
> - 扩容需要在开机状态下进行，扩容时链接会有短暂中断，请在业务低峰时进行。
> 不支持资源降配。

![](../../_images/scale.png)

## 自动扩容

通过控制台的**运维与管理** > **自动伸缩**，可创建自动扩容。

![](../../_images/auto_scale.png)
