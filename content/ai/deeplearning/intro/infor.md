---
title: "深度学习平台"
date: 2020-01-30T00:40:25+09:00
description: Test description
draft: false
enableToc: false
keyword: 深度学习, 山河, tensorflow, torch, caffe, keras
---

## 山河深度学习平台
深度学习平台基于 Docker 容器技术，将主流的深度学习框架做成 docker 镜像的形式，用户无需为环境进行繁琐的配置，直接运行容器化的深度学习应用，即可迅速开展训练和预测任务，提高了用户的开发和部署效率。
山河深度学习平台提供入门版、基础版和企业版三个版本，其中企业版搭载 NVIDIA Tesla P100 GPU，在 docker 宿主机中安装 NVIDIA Driver(387.26/418.87)，nvidia-docker2，Docker(18.09.6)，基础版搭载 AMD GPU，在 docker 宿主机中安装 ROCm 2.6.22，Docker(18.09.7)，入门版 docker 宿主机上安装 Docker(18.09.6)，宿主机上预置了一个 docker 镜像，镜像中均安装 Caffe(1.0，基础版硬件不支持未内置),  TensorFlow(1.12.0/1.14.0),  Keras(2.2.4/2.3.1),  PyTorch(1.1.0/1.2.0) 框架。

### <span id="gpu_support_table">深度学习系列、GPU型号和区域支持对应表</span>

|系列	|GPU型号	|支持区域  |
| :-------- | :--------:| :--: |
|企业版|NVIDIA Quadro RTX 6000|jn1a|
|基础版|AMD FirePro s7150*2|jn1a|
|入门版|-|全部区域|

- 内置镜像

|系列 |版本	|Python 版本	|加速库版本	|内置镜像	|描述  |
| :-------- | :--------:| :--: | :--|:--| :--|
|企业版|v2.0n-cuda9.1|2.7/3.6|CUDA 9.1|qingcloud/deeplearning:1.1-cu91-cudnn7.1|GPU 训练，CUDA 9.1 和 cuDNN 7.1 加速|
|企业版|v2.0n-cuda10.0|2.7/3.6|CUDA 10.0|qingcloud/deeplearning:1.1-cu10.0-cudnn7.6|GPU 训练，CUDA 10.0 和 cuDNN 7.6 加速|
|基础版|v2.0a|2.7/3.6|ROCm 2.6.22|qingcloud/deeplearning:1.1-rocm26|GPU 训练，ROCm 加速|
|入门版|v2.0c|2.7/3.6|MKLDNN 0.18.0|qingcloud/deeplearning:1.1-cpu-optimize|Intel CPU 优化，AVX/AVX2 指令集和 MKLDNN 库加速|

为满足用户对不同 Deep Learning 框架版本、Python 版本和 CUDA 版本的需求，山河深度学习平台提供了匹配不同版本的多个[docker image](https://hub.docker.com/u/qingcloud/)，用户可依据需要拉取，多个版本的 docker image 以及获取命令见[image 获取命令](#docker_images_pulls)

- 各深度学习框架的 Docker Hub Repository 地址

|深度学习框架	|Repository地址	|
| :-------- | :--|
|TensorFlow|https://hub.docker.com/r/qingcloud/tensorflow/|
|Keras|https://hub.docker.com/r/qingcloud/keras/|
|Pytorch|https://hub.docker.com/r/qingcloud/pytorch/|
|Caffe|https://hub.docker.com/r/qingcloud/caffe/|
|TensorFlow+Keras+Pytorch+Caffe|https://hub.docker.com/r/qingcloud/deeplearning/|