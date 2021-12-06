---
title: "유저 관심분야 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-interest GET
published: true
---

path로 전달된 유저의 관심분야 목록 반환

`GET` `http://3.135.231.171//api/user/interest`

### URI Parameter

### Response

| Status code | Type                      | Description        |
| ----------- | ------------------------- | ------------------ |
| 200 OK      | Iterable\<MemberInterest> | 유저 관심분야 목록 |



### 예제

#### Sample Request

`GET` `http://3.135.231.171/api/user/interest`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1040,
        "member":{
            "id": 1030,
            "username": "test",
            "password": "$2a$10$7JpJLI4KUV82mMcmNMY2A.rptegu4WxvgtjYsONETJQNrpSR8rZa6"
        },
        "interest":{
            "id": 1,
            "subject": "exercise"
        },
        "level": "beginner"
    },
    {
        "id": 1041,
        "member":{
            "id": 1030,
            "username": "test",
            "password": "$2a$10$7JpJLI4KUV82mMcmNMY2A.rptegu4WxvgtjYsONETJQNrpSR8rZa6"
        },
        "interest":{
            "id": 3,
            "subject": "employ"
        },
        "level": "expert"
    }
]
```

