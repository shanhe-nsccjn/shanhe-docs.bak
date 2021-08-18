---
title: "云数据库PolonDB 架构"
description: Test description
draft: false
weight: 5
enableToc: false
keyword: 云数据库PolonDB, shanhe, 数据库
---



![image-GaoKeYongJiaGou](../../_images/image-GaoKeYongJiaGou.png)


- 协调器和 Worker 节点均通过 云数据库PostgreSQL 流复制做了高可用

- 高可用管理节点负责高可用的管理和故障转移等功能

- 协调器将 `tab` 表进行分片，表的实际数据存储在 `tab_x` 中， `tab` 表不存储任何数据

