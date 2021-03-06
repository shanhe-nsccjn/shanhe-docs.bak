---
title: "扩容集群"
description: 
date: 2021-04-19T00:39:25+09:00
draft: false
weight: 7
---

云数据库ClickHouse on shanhe 支持对一个运行中的数据库服务进行在线扩容，调整CPU、内存、磁盘空间大小。

本小节主要介绍如何扩容集群。

## 操作步骤

1. 登录 shanhe 管理控制台。
2. 选择**产品与服务** > **数据仓库与 BI** > **云数据库ClickHouse**，进入 云数据库ClickHouse 集群列表页。
3. 点击集群 ID，进入集群详情页面。
4. 在**基本属性**区域下拉窗口，点击**扩容集群**。
5. 选择扩容的目标规格和磁盘大小。
6. 点击**提交**，完成扩容。

   ![扩容集群](../_images/scale.png)

**注解**：扩容需要在开机状态下进行，扩容时链接会有短暂中断，请在业务低峰时进行。
