---
title: "StopMongos"
description: 
draft: false
---



关闭指定的 Mongo 集群。

**Request Parameters**

| Parameter name | Type | Description | Required |
| --- | --- | --- | --- |
| mongos.n | String | Mongo ID | Yes |
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
https://api.shanhe.com/iaas/?action=StopMongos
&mongos.1=mongo-9ues6uda
&zone=jn1a
&COMMON_PARAMS
```

_Example Response_:

```
{
  "action":"StopMongosResponse",
  "ret_code":0,
  "mongos":[
    "mongo-9ues6uda"
  ],
  "job_id":"j-isgtvl1j"
}
```
