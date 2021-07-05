---
title: "HPC 快速入门"
linkTitle: "HPC 快速入门"
date: 2020-02-28T10:08:56+09:00
description:
weight: 1
---



## 总览

本指南旨在介绍 HPC 集群的主要属性、以及如何创建和几个主要管理功能入口等基本操作。

## 集群列表

登录到管理控制台，点击HPC服务，转到HPC控制台，点击集群，将展示下图内容

![](../_images/hpc_cluster1.png)

图中的界面主要包括以下几部分信息：

**集群状态**

* 创建中/安装中/初始化中：HPC集群创建期间的状态，对应ECS实例创建/安装软件/初始化HPC管控等阶段。无需用户干预。
* 运行中：HPC集群创建完毕处于可用状态。注意：这是集群 唯一可以正常使用的状态 。
* 异常：请提交工单，我们会协助处理。
* 释放中：集群在停机释放过程中。

**基本信息**

* 集群ID ：ID是山河平台自动分配的 HPC 唯一标识，
* 公网IP ：该IP可定位到的 公网IP 界面，可以在公网IP详情页面查看流量的监控及计费情况等。
* 可用区 ：关于可用区的说明，请参考地域和可用区。
* 创建时间 ：集群创建开始安装时间。
* 集群描述 ：在这里可以修改集群名称和对该集群的描述信息。集群名称 是用户在创建集群时赋予的名称，以明确区分集群，方便管理。

**应用信息**

* 操作系统：目前支持CentOS_7.2，操作系统会安装在所有节点中
* 调度器：目前支持slurm调度器，如需其他调度器，请通过工单或者您的客户经理提需求
* 软件管理：一键安装用户需要的软件系统
* 域账号服务：目前支持ldap，域账户服务会为所有的节点配置同样用户。

**资源监控**

* 计算节点：展示集群计算节点的总数，和当前处于不同状态的节点数
* CPU：展示集群计算节点的CPU总量，和当前计算节点的CPU使用量
* 内存：展示集群计算节点的内存总量，和当前计算节点的内存使用量

## 集群详情

集群详情页提供沉浸式的集群使用体验，所有的集群操作都可以在集群详情页完成。

集群详情页左侧包含集群的详细信息，包括`基本信息`，`应用信息`，`存储信息`，`扣费信息`。

### 节点管理

用户可以在节点管理页查看到集群的所有节点，节点的基本信息，状态，及监控

![](../_images/hpc_cluster2.png)

### 作业列表

在集群中，可以直接提交作业，并查看历史的作业列表，及作业详情

![](../_images/hpc_cluster3.png)

### 队列管理

队列是计算节点的集合，作业的运行需要选择队列。用户可以使用共享队列，或者申请专属队列，专属队列的节点仅供所属的用户占用。

![](../_images/hpc_cluster4.png)

### 用户管理

用户管理可以查看当前集群中的所有用户

![](../_images/hpc_cluster5.png)

### 租赁信息

租赁信息统计集群中所有的收费资源，及各自的价格

![](../_images/hpc_cluster6.png)

### 扣费信息

扣费信息统计集群的历史扣费

![](../_images/hpc_cluster7.png)

