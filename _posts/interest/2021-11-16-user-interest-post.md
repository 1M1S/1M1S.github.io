---
title: "유저 관심분야 추가 [POST]"
date: 2021-11-15 22:21:00 +0900
categories: user-interest POST
published: true
---

path로 전달된 유저의 관심분야 추가

`POST` `http://3.135.231.171/api/user/interest`

### URI Parameter

### Request Body

DB `MemberInterest`

| Name        | Type          | Description               |
| ----------- | ------------- | ------------------------- |
| interest_id | Interest (DB) | 관심분야 id               |
| level       | String        | 해당 관심분야의 유저 수준 |

> 수준 : beginner / junior / expert

### Response

| Status code | Type           | Description          |
| ----------- | -------------- | -------------------- |
| 200 OK      | MemberInterest | 추가된 유저 관심분야 |



### 예제

#### Sample Request

`POST` `http://3.135.231.171/api/user/interest`

Request Body

```json
{
    "interest" : {
        "id" : 1
    },
    "level" : "beginner"
}
```

#### Sample Response

Status code: 200

```json
{
    "id": 1040,
    "member":{
        "id": 1030,
        "username": "test",
        "password": "$2a$10$7JpJLI4KUV82mMcmNMY2A.rptegu4WxvgtjYsONETJQNrpSR8rZa6"
    },
    "interest":{
        "id": 1,
        "subject": null
    },
    "level": "beginner"
}
```

