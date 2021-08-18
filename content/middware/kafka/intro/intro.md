---
title: "什么是消息队列Kafka"
date: 2020-01-30T00:40:25+09:00
description: 
draft: false
enableToc: false
keyword: 
---

[消息队列Kafka](http://消息队列Kafka.apache.org/)是一种高吞吐量、低延迟、高可靠的分布式发布订阅消息系统。被广泛应用于网站活动追踪、日志监控、流式计算、事件采集、数据存储等应用场景。

`消息队列Kafka on shanhe AppCenter`将消息队列Kafka通过云应用的形式在shanhe AppCenter部署，具有如下特性:

- 开箱即用，支持横向与纵向在线伸缩
- 系统自动健康检查，系统自动运维，降低企业使用成本
- 提供了监控告警功能更好的管理集群
- 节点上安装了消息队列Kafka-manager，可以管理和监控多个消息队列Kafka集群
- 提供文件查看器方便排查问题（版本消息队列Kafka 1.1.1 - shanhe 1.5.0起）
- 提供第三方监控[zabbix](https://www.zabbix.com/)平台接口（版本消息队列Kafka 2.3.0 - shanhe 2.0.0起）

>**注意**：消息队列Kafka 1.0.0-shanhe1.1.6及后续新版本提供的消息队列Kafka-manager安装在客户端节点上。客户端节点用户名：ubuntu，密码：消息队列Kafka。消息队列Kafka-manager显示的版本并非实际消息队列Kafka版本，我们以创建消息队列Kafka实际版本为主，并不会影响到您使用消息队列Kafka和消息队列Kafka-manager。