---
title: "StopCaches"
description: 
draft: false
---



关闭一台或多台缓存服务。该操作将关闭缓存服务的所有缓存节点。

**Request Parameters**

| Parameter name | Type | Description | Required |
| --- | --- | --- | --- |
| caches.n | String | 缓存服务ID | Yes |
| zone | String | 区域 ID，注意要小写 | Yes |

[_公共参数_](../../../parameters/)

**Response Elements**

| Name | Type | Description |
| --- | --- | --- |
| action | String | 响应动作 |
| job_id | String | 执行任务的 Job ID |
| ret_code | Integer | 执行成功与否，0 表示成功，其他值则为错误代码 |

**Example**

_Example Request_:

```
https://api.shanhe.com/iaas/?action=StopCaches
&caches.1=c-55dwkqew
&zone=jn1a
&COMMON_PARAMS
```

_Example Response_:

```
{
  "action":"StopCachesResponse",
  "job_id":"j-1234abcd",
  "ret_code":0
}
```
