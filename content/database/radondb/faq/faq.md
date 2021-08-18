---
title: "性能测试"
description: Test description
draft: false
enableToc: false
---

## 硬件环境

```plain
云数据库RadonDB:
1 组 SQL 节点 (16C64G 超高性能云服务器)
4 组存储节点 (16C64G 超高性能云服务器)
sync_binlog=1
innodb_flush_log_at_trx_commit=1

RDB:
RDB (16C64G 超高性能云服务器)
sync_binlog=1
innodb_flush_log_at_trx_commit=1
```

## 测试模型

  sysbench: 16 表, 512 线程，随机写，5000 万条数据。

## 测试结果

| Item                       | Transaction Per Second (TPS) | Response Time(ms) |
| :------------------------- | ---------------------------: | :---------------: |
| 云数据库RadonDB (4 组存储节点)     |                        26589 |        20         |
| 单机 MySQL (shanhe RDB) |                         9346 |        73         |

可以看到 云数据库RadonDB 的延迟是单机 MySQL 的 1/3，但性能几乎是单机的 3 倍，这要得益于 云数据库RadonDB 对大表进行切分后，用户的写操作在这些小表上可并发式执行。

## 如何压测 云数据库RadonDB

云数据库RadonDB 支持 [sysbench](https://github.com/akopytov/sysbench) 和 [benchyou](http://github.com/XeLabs/benchyou) 性能压测软件。