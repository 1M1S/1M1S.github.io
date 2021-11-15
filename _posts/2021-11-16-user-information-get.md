---
title: "유저 정보 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user information get
published: true
---

path로 전달된 유저의 개인정보 반환

`GET` `http://localhost:8080/api/user/{user_id}/information`

### URI Parameter

| Name    | In   | Required | Type | Description |
| ------- | ---- | -------- | ---- | ----------- |
| user_id | path | true     | long | 유저의 id   |

### Response

| Status code | Type              | Description     |
| ----------- | ----------------- | --------------- |
| 200 OK      | MemberInformation | 유저의 개인정보 |

### 예제

#### Sample Request

`GET` `http://localhost:8080/api/user/1/information`

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
    "name": "c",
    "nickname": "test",
    "gender": "male",
    "phone": "010-1234-5678",
    "email": "none@gmail.com",
    "registerDate": "2021-11-14T00:00:00"
}
```

