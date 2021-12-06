---
title: "로그아웃 [POST]"
date: 2021-11-26 22:21:00 +0900
categories: auth
published: false
---

`POST ` `http://3.135.231.171/auth/logout`

### URI Parameter

### Request Body

### Response

| Status code | Type   | Description             |
| ----------- | ------ | ----------------------- |
| 200 OK      | String | 성공 여부 문자열로 반환 |
| 500         |        | 서버 오류               |



### 예제

#### Sample Request

`POST` `http://3.135.231.171/auth/logout`

#### Sample Response

Status code: 200

```json
true
```

