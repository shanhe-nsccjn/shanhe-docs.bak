---
title: "企业级分布式 SAN (NeonSAN)"
date: 2021-07-07T00:38:25+09:00
description: Test description
draft: false
enableToc: false
keyword: 山河
---

# 简介

企业级分布式 SAN (NeonSAN) 是基于全闪存架构提供的分布式 SAN 服务，单块硬盘容量最高 20TB， I/O 吞吐性能最高可达 350 MB/s， IOPS 最高 50000，适用于对 IOPS、吞吐、容量和稳定性要求很高的业务，例如：企业核心数据库 Oracle RAC 及 SQL Server 故障转移集群、企业级云数据库云数据库RadonDB、弹性裸金属服务器高可用架构、大数据分析与计算、以及高可用容器集群等。


## 创建

### 第一步：创建企业级分布式 SAN (NeonSAN)

进在控制台导航中点击『产品与服务』-『存储服务』-『硬盘 』进入如下界面。

![企业级分布式NeonSAN](/storage/disk/manual/_images/create_NeonSAN_1.png)

点击 **创建** 进入如下界面

![创建NeonSAN](/storage/disk/manual/_images/create_NeonSAN_2.png)

在名称框里输入创建的硬盘名称，在数量框里输入需要创建的硬盘数量，在类型中选择企业级分布式 SAN (NeonSAN), 拖动滑动按钮选择容量大小，或者在右边的输入框中输入容量大小，点击 **提交** ，进入如下界面

![完成NeonSAN创建](/storage/disk/manual/_images/create_NeonSAN_3.png)

当状态显示为“可用”时，表示创建成功。

> 注解：
>
> 单块最小容量 100 GB、最大容量 20 TB，容量可选最小粒度为 100 GB 
>
> IOPS 参考范围：2000-50000
>
> 单盘 IOPS 计算公式： min{2000 + 50 * 容量， 50000 }
>
> 吞吐： 128 MB/s - 350MB/s ; 
>
> 单盘IO吞吐计算公式： min{128 + 0.5 * 容量， 350} MBps


### 第二步：配置服务

鼠标右键点击硬盘条目，或选中硬盘条目鼠标左键点击更多操作，进入如下界面

![备份NeonSAN](/storage/disk/manual/_images/create_NeonSAN_4.png)

![备份NeonSAN](/storage/disk/manual/_images/create_NeonSAN_5.png)

**加载企业级分布式 SAN (NeonSAN) 到云服务器**

点击 **加载硬盘到云服务器** ，进入如下界面

![加载neonSAN到云服务器](/storage/disk/manual/_images/create_NeonSAN_6.png)

选择需要加载该企业级分布式 SAN (NeonSAN) 的云服务器，点击 **提交**，即可挂载到指定云服务器。

> 注解：企业级分布式 SAN(NeonSAN) 支持被挂载至基础型、企业型 e2 和 GPU 云服务器上，且一块 NeonSAN 硬盘可以同时挂载到多台云服务器。如果您将一块 NeonSAN 硬盘绑定到多个云服务器上， 请确保使用集群文件系统，例如 OCFS2, 否则磁盘可能会损坏

还可以从 **计算-云服务器** 页面，鼠标右键点击云服务器条目，来选择 **硬盘**，进行硬盘加载，界面如下

![从云服务器加载NeonSAN](/storage/disk/manual/_images/create_NeonSAN_7.png)

**修改企业级分布式 SAN (NeonSAN) 名称或属性**

点击 **修改**，进入如下界面

![修改NeonSAN](/storage/disk/manual/_images/create_NeonSAN_8.png)

可以修改企业级分布式 SAN (NeonSAN) 的属性，包括名称和描述，然后点击 **修改** 。

**克隆企业级分布式 SAN (NeonSAN)**

点击 **克隆硬盘** ，进入如下界面

![克隆NeonSAN](/storage/disk/manual/_images/create_NeonSAN_9.png)

在名称框填入名称，写入拷贝数量，类型选择企业级分布式 SAN (NeonSAN) ，点击 **提交** ，进入如下界面

![完成NeonSAN克隆](/storage/disk/manual/_images/create_NeonSAN_10.png)

当状态显示为“可用”时，表示克隆成功。

**扩容**

点击 **扩容** ，进入如下界面

![扩容NeonSAN](/storage/disk/manual/_images/create_NeonSAN_11.png)

**备份**

点击 **创建备份** ，进入如下界面

![备份NeonSAN](/storage/disk/manual/_images/create_NeonSAN_12.png)

点击 **继续** ，进入如下界面

![完成创建NeonSAN](/storage/disk/manual/_images/create_NeonSAN_13.png)

在名称框里填入名称，有需要的选择创建新备份链，点击 **提交** 。可以左键点击企业级分布式 SAN (NeonSAN) 条目，进入如下界面

![完成NeonSAN备份链创建](/storage/disk/manual/_images/create_NeonSAN_14.png)

可以看到状态显示为“可用”，表示备份已经创建成功。

**标签**

点击 **标签** ，为已经创建的企业级分布式 SAN (NeonSAN) 绑定标签，进入如下界面

![为NeonSAN绑定标签](/storage/disk/manual/_images/create_NeonSAN_15.png)

如果没有标签或已有标签不适用，可以选择 **创建标签** ，或者进行 **标签管理** 。选择标签，点击 **提交** ，进入如下界面

![创建标签](/storage/disk/manual/_images/create_NeonSAN_16.png)

**添加到项目**

点击 **项目-加入**，进入如下界面

![将NeonSAN加入到项目](/storage/disk/manual/_images/create_NeonSAN_project.png)

选择需要添加到的项目，点击 **提交** 将硬盘添加到项目，回到硬盘列表可以查看硬盘所属的项目，如下图

![查看NeonSAN已加入的项目](/storage/disk/manual/_images/create_NeonSAN_project2.png)

## 备份配置

左键点击企业级分布式 SAN (NeonSAN) 条目，进入如下界面

![NeonSAN备份配置](/storage/disk/manual/_images/create_NeonSAN_17.png)

鼠标右键点击备份链ID，进入如下界面

![NeonSAN备份链修改](/storage/disk/manual/_images/create_NeonSAN_18.png)

**修改备份名称或描述**

点击 **修改** ，进入如下界面

![修改备份链](/storage/disk/manual/_images/create_NeonSAN_19.png)

在名称填入要修改成的名称，在描述框里输入新的描述，点击 **提交** 。

**基于备份新建硬盘**

点击 **创建硬盘** ，进入如下界面

![基于备份创建硬盘](/storage/disk/manual/_images/create_NeonSAN_20.png)

在名称框里填入新硬盘的名称，点击 **提交** ，可以硬盘首页看到

![完成备份硬盘创建](/storage/disk/manual/_images/create_NeonSAN_21.png)

当新建硬盘的状态显示为“可用”时，表示新硬盘已经创建成功。

**共享备份**

点击 **共享备份** ，进入如下界面

![共享NeonSAN备份](/storage/disk/manual/_images/create_NeonSAN_22.png)

可以选择共享给子账号还是共享给其他账号，选择要共享给的子账号或填写要给共享的其他用户 ID/ 注册邮箱地址，点击 **提交** 。鼠标右键双击备份链接入备份属性修改界面，可以看到共享列表，里面有已经添加成功的共享账号列表。

**跨区复制备份**

点击 **跨区复制备份** ，进入如下界面

![快去复制NeonSAN备份](/storage/disk/manual/_images/create_NeonSAN_23.png)

选择要复制到区域，点击 **提交** 。

## 备份属性修改

鼠标左键双击备份链条目，或者在备份链条目下面，可以看到备份链结构示意图，假如双击备份链条目，进入如下界面

![备份属性修改](/storage/disk/manual/_images/create_NeonSAN_24.png)

鼠标左键点击备份链右侧的 **...** ，可以选择对备份链的修改、创建硬盘、回滚和删除，界面如下

![修改备份链](/storage/disk/manual/_images/create_NeonSAN_25.png)

## 监控

在企业级分布式 SAN (NeonSAN) 挂载到云服务器时，可以点击条目，查看监控情况，界面如下

![NeonSAN监控](/storage/disk/manual/_images/create_NeonSAN_26.png)

在硬盘 IOPS 和硬盘吞吐量打开时，可以看到硬盘 IOPS 和硬盘吞吐量数据展示。还可以点击硬盘使用率右侧的 **查看监控图** 来查看硬盘使用率。


