---
title: "软件安装"
linkTitle: "软件安装"
date: 2020-02-28T10:08:56+09:00
description:
weight: 2
---

## 使用spack安装软件

### 1、在加目录下创建.spack目录

![](../_images/spack-root.png)

### 2、拷贝公共软件的配置文件到.spack目录

![](../_images/spack-config.png)


### 3、查找可安装的软件

![](../_images/spack-find-soft.png)

### 4、安装软件

![](../_images/spack-install-soft.png)

### 5、查找、加载本地软件

    spack find

    spack load software@version

### 6、查找加载公共软件

    spack-pub find

    spack-pub load software@version


