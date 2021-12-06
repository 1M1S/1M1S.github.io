---
title: "유저 정보 수정 [PUT]"
date: 2021-11-15 22:21:00 +0900
categories: user-information PUT
published: true
---

path로 전달된 유저의 개인정보 수정

`PUT` `http://localhost:8080/api/user/{user_id}/information`

### URI Parameter

| Name    | In   | Required | Type | Description |
| ------- | ---- | -------- | ---- | ----------- |
| user_id | path | true     | Long | 유저의 id   |

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

`PUT` `http://localhost:8080/api/user/1/information`

Request Body

```json
{
    "nickname": "changed",
    "email": "test@gmail.com"
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
    "name": "chisan",
    "nickname": "changed",
    "gender": "male",
    "phone": "010-1234-5678",
    "email": "test@gmail.com",
    "registerDate": "2021-11-14T00:00:00"
}
```

