---
title: "常见问题"
date: 2021-07-07T00:38:25+09:00
description: Test description
draft: false
enableToc: false
---

## CPU 占用率过高怎么办？

首先通过监控项（当前线程连接数、活跃线程连接数）或 show processlist 确认并发情况。如果并发较高，CPU 占用率高就是并发太多引起的，建议扩容 CPU。

如果并发并不是很多，那很有可能是复杂的查询造成的，建议下载分析慢日志，如果涉及聚合(count,sum,avg,max,min), 分组(group by), 排序(sort)等运算，是很消耗 CPU 资源的。

> 建议：如果用户 SQL 不好优化，可以建议他扩容CPU。

## MySQL 查询很慢是什么原因?

建议您先分析慢日志：

连接到 MySQL 里面执行`show engine innodb status\G`，查看下数据库读写状态，重点关注最后的每秒读写情况。

下载慢日志文件`mysql-slow.log`。

分析下慢日志里面运行很慢的 SQL，看是否能创建索引来优化, 减少全表扫描。

## 业务压力大，内存占用率100%怎么办？

建议下载、分析慢日志，优化比较耗时的 SQL。

若 SQL 无需优化，建议您扩容。

## MySQL 高可用读 IP、高可用写 IP、高可用Proxy IP、主节点 IP、从节点 IP 的作用分别是什么？

**主节点**可读可写，**从节点**只可读。

**高可用读IP**可将请求在多个从节点和主节点（可配置是否分发给主节点）之间进行负载分发，以提高数据库的查询性能；发生从节点故障, 会自动从高可用读IP列表里面摘掉故障节点IP, 不影响业务查询。

**高可用写IP**可以在主节点发生故障时自动切换到新的主节点上，提供高可用机制, 以减少故障时间。

建议写业务连接高可用写IP, 读业务连接高可用读IP。

**高可用Proxy IP**必须有Proxy节点才能使用，Proxy会根据读写、只读请求将负载分别分发到主、从节点。