---
title: "深度学习基础服务"
date: 2021-07-07T00:40:25+09:00
description: Test description
draft: false
enableToc: false
keyword: 深度学习, 山河, tensorflow, torch, caffe, keras
---

## 山河深度学习平台
深度学习平台使用miniconda进行框架的版本管理，用户可直接使用预置的框架版本，也可创建自己的虚拟环境，安装其他版本。

山河深度学习平台提供入门版、企业版二个版本，其中企业版搭载 NVIDIA RTX 6000 GPU，在 docker 宿主机中安装 NVIDIA Driver(460.84)。

### <span id="gpu_support_table">深度学习系列、GPU型号和区域支持对应表</span>

|系列	|GPU型号	|支持区域  |
| :-------- | :--------:| :--: |
|企业版|NVIDIA Quadro RTX 6000|jn1a|
|入门版|-|jn1a|

- 内置深度学习框架

| Python 版本	|加速库版本	|内置框架版本	|描述  |
| :-------- | :--------:| :--: | :--|
| 3.9 |CUDA 10.1|tensorflow-gpu_2.4.1-keras_2.4.3|GPU 训练，CUDA 10.1 和 cuDNN 7.6.5 加速|
| 3.6 |CUDA 10.0|tensorflow-gpu_2.0.0-keras_2.3.1|GPU 训练，CUDA 10.0 和 cuDNN 7.6.5 加速|
| 3.6 |CUDA 10.0|tensorflow-gpu_1.15.0-keras_2.3.1|GPU 训练，CUDA 10.0 和 cuDNN 7.6.5 加速|
| 3.9 |CUDA 11.1|pytorch-1.9.0|GPU 训练，CUDA 11.1|
| 3.6 |CUDA 10.1|pytorch-1.6.0|GPU 训练，CUDA 10.1|
| 3.6 |CUDA 10.0|pytorch-1.2.0|GPU 训练，CUDA 10.0|
| 3.6 |CUDA 10.1|caffe-gpu-1.0|GPU 训练，CUDA 10.1|
