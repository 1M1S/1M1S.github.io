---
title: "[예제]일정 수정"
date: 2021-11-7 12:21:00 +0900
categories: tutorial
---
수정할 일정의 id, 시간, 내용을 전달받아 일정을 수정하고 수정된 일정을 반환한다.

`PUT` `http://3.135.231.171/{id}`

### URI Parameter

| Name | In   | Required | Type | Description      |
| ---- | ---- | -------- | ---- | ---------------- |
| id   | path | true     | int  | 수정할 일정의 id |

### Request Body

time이나 content 중 한가지만 수정하려면 수정하지 않을 항목의 값은 ""로 보내면 된다.

| Name    | Type   | Description |
| ------- | ------ | ----------- |
| time    | string | 시간        |
| content | string | 내용        |

### Response

| Status code | Type     | Description |
| ----------- | -------- | ----------- |
| 200 OK      | TodoList | 수정한 일정 |

### 예제

#### Sample Request

`PUT` `http://3.135.231.171/34`

Request Body

```json
{
  "time":"6:30PM",
  "content" : ""
}
```

#### Sample Response

Status code: 200

```json
{
    "id": 34,
    "time": "6:30PM",
    "content": "dinner"
}
```
