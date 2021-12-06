---
title: "유저 정보 수정 [PUT]"
date: 2021-11-15 22:21:00 +0900
categories: user-information PUT
published: true
---

path로 전달된 유저의 개인정보 수정

`PUT` `http://3.135.231.171/api/user/information`

### URI Parameter

### Request Body

DB `MemberInformation`

> 수정할 항목들만 전달하면 된다. 나머지는 null로 전달됨.

| Name     | Type   | Description |
| -------- | ------ | ----------- |
| name     | String | 실명        |
| nickname | String | 닉네임      |
| gender   | String | 성별        |
| phone    | String | 전화번호    |
| email    | 이메일 | String      |

### Response

| Status code | Type              | Description            |
| ----------- | ----------------- | ---------------------- |
| 200 OK      | MemberInformation | 수정된 유저의 개인정보 |



### 예제

#### Sample Request

`PUT` `http://3.135.231.171/api/user/information`

Request Body

```json
{
  "email" : "edited@test.com"
}
```

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
    "email": "edited@test.com",
    "register_date": "2021-12-06T09:27:43.784559",
    "memberId": 1030
}
```

