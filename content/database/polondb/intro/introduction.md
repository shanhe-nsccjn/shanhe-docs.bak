---
title: "什么是 云数据库PolonDB"
description: Test description
draft: false
weight: 3
enableToc: false
keyword: 云数据库PolonDB, shanhe, 数据库
---

云数据库PolonDB 是基于 云数据库PostgreSQL 和 Citus 构建的一款 HTAP 分布式关系型数据库。

Citus 是 云数据库PostgreSQL 的扩展（not a fork），采用 shared nothing 架构，节点之间无共享数据，由协调器节点和 Work 节点构成一个数据库集群。相比单机 云数据库PostgreSQL，Citus 可以使用更多的 CPU 核心，更多的内存数量，保存更多的数据。通过向集群添加节点，可以轻松的扩展数据库。

Citus 支持新版本 云数据库PostgreSQL 的特性，并保持与现有工具的兼容。Citus 使用分片技术在多台机器上横向扩展 云数据库PostgreSQL。Citus 的查询引擎在这些服务器上采用并行化查询，以便在大型数据集上实现实时的响应。

![image-PolonDBJieMian](../../_images/image-PolonDBJieMian.png)