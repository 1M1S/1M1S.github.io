---
title: "유저 관심분야 추가 [POST]"
date: 2021-11-15 22:21:00 +0900
categories: user interest post
published: true
---

path로 전달된 유저의 관심분야 추가

`POST` `http://localhost:8080/api/user/{user_id}/interest`

### URI Parameter

| Name        | In    | Required | Type    | Description               |
| ----------- | ----- | -------- | ------- | ------------------------- |
| user_id     | path  | true     | Long    | 유저의 id                 |
| interest_id | query | true     | Long    | 관심분야 id               |
| level       | query | true     | Integer | 해당 관심분야의 유저 수준 |

### Response

| Status code | Type           | Description          |
| ----------- | -------------- | -------------------- |
| 200 OK      | MemberInterest | 추가된 유저 관심분야 |



### 예제

#### Sample Request

`POST` `http://localhost:8080/api/user/1/interest?interest_id=1&level=7`

#### Sample Response

Status code: 200

```json
{
    "id": 1026,
    "member":{
        "id": 1,
        "username": "user1",
        "password": "1234"
    },
    "interest":{
        "id": 1,
        "subject": "workout"
    },
    "level": 7
}
```

