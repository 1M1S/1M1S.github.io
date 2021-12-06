---
title: "[예제]일정 생성"
date: 2021-11-7 12:21:00 +0900
categories: tutorial
---
시간, 내용을 전달받아 일정을 생성하고, 생성된 일정을 반환한다.

`POST` `http://3.135.231.171`

### URI Parameter

| Name    | In    | Required | Type   | Description |
| ------- | ----- | -------- | ------ | ----------- |
| time    | query | true     | string | 시간        |
| content | query | true     | string | 내용        |

### Response

| Status Code | Type     | Description      |
| ----------- | -------- | ---------------- |
| 200 OK      | TodoList | 새로 생성한 일정 |

### 예제

#### Sample Request

`POST` `http://3.135.231.171?time=6:00PM&content=dinner`

#### Sample Response

Status code: 200

```json
{
    "id": 34,
    "time": "6:00PM",
    "content": "dinner"
}
```