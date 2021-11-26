---
title: "유저별 상담결과 추가 [POST]"
date: 2021-11-15 22:21:00 +0900
categories: user-counsel-result POST
published: true

---

유저별 시간관리 상담 후 결과 저장.

`POST` `http://localhost:8080/api/user/{user_id}/counsel-result`

### URI Parameter

| Name    | In   | Required | Type | Description |
| ------- | ---- | -------- | ---- | ----------- |
| user_id | path | true     | Long | 유저의 id   |

### Request Body

| Name   | Type   | Description |
| ------ | ------ | ----------- |
| result | String | 상담 결과   |

### Response

| Status code | Type                | Description           |
| ----------- | ------------------- | --------------------- |
| 200 OK      | MemberCounselResult | 추가된 유저 상담 결과 |



### 예제

#### Sample Request

`POST` `http://localhost:8080/api/user/1/counsel-result`

Request Body

```json
{
  "result" : "솔루션1
  솔루션2
  솔루션3"
}
```

#### Sample Response

Status code: 200

```json
{
    "id": 1,
    "member":{
        "id": 1,
        "username": "user1",
        "password": "1234"
    },
    "counselSolution": "{\n  \"result\" : \"솔루션1\n  솔루션2\n  솔루션3\"\n}",
    "counselTime": "2021-11-27T02:17:38.0625466"
}
```

