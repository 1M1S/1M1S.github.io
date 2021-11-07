---
title: "[예제]일정 삭제"
date: 2021-11-7 12:21:00 +0900
categories: tutorial
---
삭제할 일정의 id를 전달받아 해당 일정을 삭제하고 삭제한 일정을 반환한다.

`DELETE` `http://localhost:8080/{id}`

### URI Parameter

| Name | In   | Required | Type | Description      |
| ---- | ---- | -------- | ---- | ---------------- |
| id   | path | true     | int  | 삭제할 일정의 id |

### Response

| Status code | Type     | Description |
| ----------- | -------- | ----------- |
| 200 OK      | TodoList | 삭제한 일정 |

### 예제

#### Sample Request

`DELETE` `http://localhost:8080/34`

#### Sample Response

Status code: 200

```json
{
    "id": 34,
    "time": "6:30PM",
    "content": "dinner"
}
```