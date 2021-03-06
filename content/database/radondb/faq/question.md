---
title: "常见问题"
date: 2021-07-07T00:38:25+09:00
description: Test description
draft: false
enableToc: false
---

**CPU占用率过高:**

首先通过监控项（当前线程连接数、活跃线程连接数）或show processlist确认并发情况。如果并发较高，CPU占用率高就是并发太多引起的，建议扩容CPU。

如果并发并不是很多，那很有可能是复杂的查询造成的，建议下载分析慢日志, 如果涉及聚合(count,sum,avg,max,min), 分组(group by), 排序(sort)等运算,是很消耗CPU资源的。

建议： 如果用户SQL不好优化，可以建议他扩容CPU。

**MySQL查询很慢是什么原因:**

建议您分析下慢日志：

连接到mysql里面执行show engine innodb status\G查看下数据库读写状态，重点关注最后的每秒读写情况。

下载慢日志文件mysql-slow.log。

分析下慢日志里面运行很慢的SQL，看是否能创建索引来优化, 减少全表扫描。

**业务压力大，内存占用率100%？:**

建议下载、分析慢日志，优化一些比较耗时的SQL。

如果SQL没什么好优化的，建议您扩容。

**MySQL 高可用读IP、高可用写IP、高可用Proxy IP、主节点IP、从节点IP的作用分别是什么？:**

主节点可读可写，从节点只读。

高可用读IP可将请求在多个从节点和主节点（可配置是否分发给主节点）之间进行负载分发，以提高数据库的查询性能；发生从节点故障, 会自动从高可用读IP列表里面摘掉故障节点IP, 不影响业务查询。

高可用写IP可以在主节点发生故障时自动切换到新的主节点上，提供高可用机制, 以减少故障时间。

建议写业务连接高可用写IP, 读业务连接高可用读IP。

高可用Proxy IP必须有Proxy节点才能使用，Proxy会根据读写、只读请求将负载分别分发到主、从节点。