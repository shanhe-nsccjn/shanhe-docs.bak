---
title: "系统盘的扩容"
date: 2021-07-07T00:38:25+09:00
description: Test description
draft: false
enableToc: false
keyword: 山河
---

# 云服务器系统盘扩容

一直以来，山河 shanhe 都秉承云计算的理念，云服务器的系统是临时的，随时可以关闭和销毁，而并不影响业务可用性的，所以并不建议用户将数据放在系统盘（即操作系统启动程序所在磁盘）。

但是，用户的需求总是各式各样的，作为综合平台服务商，山河需要支持各种场景。

于是，山河 shanhe 为云服务器增加了系统盘扩容的功能：

*   用户可以在创建云服务器时，自定义系统盘的大小。
*   用户可以在已有的云服务器进行扩容。

已知限制：

> 注解: 
>
> Linux 和 FreeBSD 操作系统支持的范围是 20 到300 GB，Windows 操作系统支持的范围是 50 到 300 GB。
>
> 为现有的云服务器进行扩容，必须在操作系统关闭的情形下进行。
>
> 扩容仅支持单向的增加，而不可以缩减。

>警告:在扩容前，请务必确认你所使用的操作系统以及文件系统是否支持，否则，有可能会出现系统无法启动，数据无法访问的情形！

>警告: 请务必做好备份工作。以防万一。

## 使用步骤：

### 一、新创建云服务器时指定系统盘大小

如下图所示：

![创建云服务器](/storage/disk/quickstart/_images/create_instance_custom_disk.png)

### 二、已有的云服务器扩容步骤

以一台安装有 CentOS7.3 操作系统的云服务器为例：

1、确认当前系统的大小

![确认系统盘大小](/storage/disk/quickstart/_images/system_disk.png)

2、关闭操作系统，选择要扩容系统盘的云服务器，在“更多操作”中选择“更改配置”，并按照下图所示，扩展系统磁盘：

![更改操作系统](/storage/disk/quickstart/_images/resize_system_instance.png)

3、启动云服务器，并查看更改后的结果：

![启动云服务器](/storage/disk/quickstart/_images/after_resize.png)

确认修改成功。

如有更多需求，请提交工单或联系我们。
