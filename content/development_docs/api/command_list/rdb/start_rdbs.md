---
title: "StartRDBs"
description: 
draft: false
---



启动指定的数据库集群。

**Request Parameters**

| Parameter name | Type | Description | Required |
| --- | --- | --- | --- |
| rdbs.n | String | 数据库集群 ID | Yes |
| zone | String | 区域 ID，注意要小写 | Yes |

[_公共参数_](../../../parameters/)

**Response Elements**

| Name | Type | Description |
| --- | --- | --- |
| action | String | 响应动作 |
| job_id | String | 执行任务的 Job ID |
| ret_code | Integer | 执行成功与否，0 表示成功，其他值则为错误代码 |

**Example**

_Example Request_

```
https://api.shanhe.com/iaas/?action=StartRDBs
&rdbs.1=rdb-y76ik96v
&zone=jn1a
&COMMON_PARAMS
```

_Example Response_:

```
{
  "action":"StartRDBsResponse",
  "rdbs":[
    "rdb-y76ik96v"
  ],
  "job_id":"j-epc5mlzz",
  "ret_code":0
}
```
