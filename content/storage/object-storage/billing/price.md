---
title: "消费说明"
date: 2020-11-23T10:08:56+09:00
description:
draft: false
weight: 21
---

对象存储的计费周期为月，每月初会根据用量自动扣除上个月费用。

## 资费标准

<table>
  <tr>
    <th rowspan="9">存储空间价格</th>
    <th>阶梯</th>
    <th>标准存储单价（元/GB/月）</th>
    <th>低频存储单价（元/GB/月）</th>
  </tr>
  <tr>
    <td>0GB-10GB</td>
    <td>免费</td>
    <td>免费</td>
  </tr>
  <tr>
    <td>10GB-1TB</td>
    <td>0.096</td>
    <td>0.064</td>
  </tr>
  <tr>
    <td>1TB-3TB</td>
    <td>0.094</td>
    <td>0.061</td>
  </tr>
  <tr>
    <td>3TB-10TB</td>
    <td>0.092</td>
    <td>0.058</td>
  </tr>
  <tr>
    <td>10TB-200TB</td>
    <td>0.088</td>
    <td>0.055</td>
  </tr>
  <tr>
    <td>200TB-500TB</td>
    <td>0.084</td>
    <td>0.052</td>
  </tr>
  <tr>
    <td>500TB-5000TB</td>
    <td>0.081</td>
    <td>0.049</td>
  </tr>
  <tr>
    <td>5000TB以上</td>
    <td>0.078</td>
    <td>请联系我们</td>
  </tr>
  <tr>
    <td rowspan="8">下载流量价格</td>
    <td>阶梯</td>
    <td>单价（元/GB）</td>
    <td>单价（元/GB）</td>
  </tr>
  <tr>
    <td>0 GB - 1 GB</td>
    <td>免费</td>
    <td>免费</td>
  </tr>
  <tr>
    <td>1GB-3TB</td>
    <td>0.4</td>
    <td>0.4</td>
  </tr>
  <tr>
    <td>3TB-10TB</td>
    <td>0.37</td>
    <td>0.37</td>
  </tr>
  <tr>
    <td>10TB-50TB</td>
    <td>0.34</td>
    <td>0.34</td>
  </tr>
  <tr>
    <td>50TB-100TB</td>
    <td>0.31</td>
    <td>0.31</td>
  </tr>
  <tr>
    <td>100TB-500TB</td>
    <td>0.29</td>
    <td>0.29</td>
  </tr>
  <tr>
    <td>500TB以上</td>
    <td>0.24</td>
    <td>0.24</td>
  </tr>
  <tr>
    <td>API 请求次数</td>
    <td></td>
    <td>0.008元/万次</td>
    <td>0.05元/万次</td>
  </tr>
  <tr>
    <td>数据取回</td>
    <td></td>
    <td>无</td>
    <td>0.025元/GB</td>
  </tr>
  <tr>
    <td>最小存储单元</td>
    <td></td>
    <td>无</td>
    <td>无</td>
  </tr>
  <tr>
    <td>最小存储天数</td>
    <td></td>
    <td>无</td>
    <td>30天</td>
  </tr>
</table>


## 免费额度

注册成功并完成认证的的 对象存储服务OIS用户，shanhe 为您提供一定额度的 OIS™ 对象存储免费使用套餐（雅加达区对象存储不在免费政策范围内）。 免费政策从用户创建的存储空间之日算起，在未来 12 个月免费赠送:

- 存储空间：30 GB （含10 GB 永久免费空间）
- 下载流量：11 GB（含1 GB 免费下载流量）
- 读请求 (GET/HEAD)：100 万次
- 写请求 (PUT/POST/DELETE)：10 万次

## 欠费说明

若当月费用扣除后余额不足，则用户的所有存储空间将会处于 `暂停` 状态，此时用户无法使用对象存储的任何功能。等到用户充值足够的金额后，用户的所有存储空间将会自动恢复。
