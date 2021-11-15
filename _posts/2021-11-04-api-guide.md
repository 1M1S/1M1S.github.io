---
title: "제목"
date: 2021-11-4 12:21:00 +0900
categories: tutorial
published: false

---

API 설명

`GET|POST|PUT|DELETE` `http://example.com/api/test`

### URI Parameter

| Name | In         | Required   | Type   | Description |
| ---- | ---------- | ---------- | ------ | ----------- |
| 이름 | path/query | true/false | 자료형 | 설명        |
| ...  |            |            |        |             |

### Request Body

| Name | Type   | Description |
| ---- | ------ | ----------- |
| 이름 | 자료형 | 설명        |
| ...  |        |             |

### Response

| Status code | Type   | Description |
| ----------- | ------ | ----------- |
| ex) 200 OK  | 자료형 | 설명        |
| ...         |        |             |

### 예제

#### Sample Request

`POST` `http://example.com/api/test`

Request Body

```json
{
    "name" : "Mr.Kim"
}
```

#### Sample Response

Status code: 200

```json
{
    "id" : 1,
    "name" : "Mr.Kim"
}
```

