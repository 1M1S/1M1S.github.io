---
title: "유저 정보 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-information GET
published: true
---

path로 전달된 유저의 개인정보 반환

`GET` `http://3.135.231.171/auth/me`

### URI Parameter

### Response

| Status code | Type              | Description     |
| ----------- | ----------------- | --------------- |
| 200 OK      | MemberInformation | 유저의 개인정보 |



### 예제

#### Sample Request

`GET` `http://3.135.231.171/auth/me`

#### Sample Response

Status code: 200

```json
{
    "id": 1031,
    "member":{
        "id": 1030,
        "username": "test",
        "password": "$2a$10$7JpJLI4KUV82mMcmNMY2A.rptegu4WxvgtjYsONETJQNrpSR8rZa6"
    },
    "name": "안치산",
    "nickname": "테스트",
    "gender": "male",
    "phone": null,
    "email": "chisan@test.com",
    "register_date": "2021-12-06T09:27:43.784559",
    "memberId": 1030
}
```

