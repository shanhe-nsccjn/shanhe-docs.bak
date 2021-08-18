---
title: "推理基础服务"
date: 2020-01-30T00:40:25+09:00
description: Test description
draft: false
enableToc: false
keyword: 推理引擎, 山河, tensorflow, torch, caffe, keras
---


## 简介

训练和推理是机器/深度学习的两个重要组成部分。用户利用加速器 ( CPU/GPU/FPGA) 通过各种深度学习框架如 Tensorflow, PyTorch 等训练好模型后，将模型部署到生产环境、管理模型版本并提供 API 用于推理，是机器/深度学习产生价值的不可或缺的环节。



一个成熟的推理产品除了要支持多种推理框架、多种加速器（CPU/GPU）之外，还需要支持诸如推理 API (HTTP/GPRC) 负载均衡、模型上传、模型存储、模型部署、水平/垂直伸缩、推理引擎日志/推理 API 访问日志查看等诸多功能。



Inference Engine 旨在解决上述问题，给用户提供一站式的模型部署与推理方案，并为以后模型市场的推出打下坚实的基础，具体来讲包括：

- 一键部署、灵活易用。用户仅需要上传模型，设置模型名称即可快速拥有生产环境可用的 AI 推理引擎。

- 支持目前比较主流的推理框架: Tensorflow Serving / ONNX Runtime / OpenVINO 

  > v1.0 版仅支持 针对 Intel CPU 优化过的 CPU 版的 Tensorflow Serving , 陆续会推出更多推理框架的支持

- 支持多种加速器 CPU、GPU 等。值得一提的是当前 Inference Engine 用到的 CPU 是第二代 Intel 至强可扩展处理器 ( CascadeLake ) ，因其采用了 Intel DeepLearning Boost VNNI 技术，AI 推理性能和较老型号的 CPU  相比有接近 100% 的提升 (详见性能测试部分)。不同于训练阶段，配合针对 CPU 优化过的框架，CPU 可以在推理环节发挥更重要的作用，与 GPU 相比可以给用户提供更低成本的选择。

- 支持通过云原生技术 Envoy 进行高效的 HTTP 和 GRPC 推理 API 的负载均衡，用户只需配置好需要暴露的 HTTP/GRPC 端口即可。

- 支持多种模型存储方式包括：本地磁盘存储、S3 对象存储、兼容 S3 协议的 MinIO 私有对象存储

- 支持多种部署方式：试验性单节点部署（利用本地磁盘作为模型库）、私有云多节点部署（利用 MinIO 作为模型库）、公有云多节点部署（利用 对象存储服务OIS作为模型库）

- 支持水平/垂直扩容和缩容

- 支持引擎运行日志查看和推理 API 访问日志查看