---
title: "概述"
date: 2020-02-28T10:08:56+09:00
description:
draft: false
weight: 1
---

山河对象存储服务(shanhe Object Storage Service，亦称对象存储服务OIS)旨在为用户提供 稳定可靠，安全易用，空间无限的云存储服务。可存储任意类型，任意数量，任意大小 (单个对象最大至50T)的非结构化数据。本指南将介绍如何使用山河对象存储服务的API。

## 总览
山河对象存储服务的 API 符合 REST (Representational State Transfer) 风格所定义的 语义，通过 URL 指定想要访问的资源，使用标准的 HTTP 方法(GET, PUT, DELETE, HEAD, POST, OPTIONS)定义对资源的操作方式。

## 基本概念

### Location (or Zone)
区域。和山河shanhe一样，山河对象存储服务支持多区域部署。您可以在不同区域创建 存储空间(Bucket)。

### Service
对象存储服务的顶层命名空间，在该命名空间下，每一个用户可以创建多个存储空间 (Bucket)。存储空间名称在该命名空间下全局唯一。

### Bucket

用户申请的存储空间。创建存储空间时须选择区域。
Bucket 命名规范:

- 遵守 DNS 命名规则。
- 长度在 6 ~ 63 之间。
- 只能包含 小写字母，数字和连接字符 -。
- 开头和结尾只能是小写字母或数字。
- 不能是有效 IP 地址。

### Object

用户操作的基本数据单元。PUT方法上传的 Object 允许最大 5GB; 分段(Multipart) 上传的 Object 最大可达 50TB。
Object 命名规范:

- 长度须在 1-1023 字节之间
- 须用 UTF-8 编码
- 不能以 '/' 开头

### 地址构成

每个 Object 的访问地址有如下两种风格:

- Virtual-host Style - `http://<bucket_name>.<zone_id>.is.shanhe.com/`
- Path Style - `http://<zone_id>.is.shanhe.com/<bucket_name>/`

其中 `<zone_id>` 代表存储空间创建时选择的区域，目前对象存储开放的区域有：

|Name|Zone ID|URL Example|
|-|-|-|
|济南1区-A|jn1a|`http://mybucket1.jn1a.is.shanhe.com/myobject`|
|           |         |                                                |
|           |         |                                                |
|           |         |                                                |
|           |         |                                                |
