---
title: "유저 관심분야 수준 변경 [PUT]"
date: 2021-11-15 22:21:00 +0900
categories: user interest put
published: true

---

path로 전달된 유저의 관심분야 수준 변경

`PUT` `http://localhost:8080/api/user/{user_id}/interest/{member_interest_id}`

### URI Parameter

| Name               | In    | Required | Type    | Description               |
| ------------------ | ----- | -------- | ------- | ------------------------- |
| user_id            | path  | true     | long    | 유저의 id                 |
| member_interest_id | path  | true     | long    | 수정할 유저의 관심분야 id |
| level              | query | true     | Integer | 유저의 수준으로 사용할 값 |

### Response

| Status code | Type           | Description          |
| ----------- | -------------- | -------------------- |
| 200 OK      | MemberInterest | 수정된 유저 관심분야 |



### 예제

#### Sample Request

`PUT` `http://localhost:8080/api/user/1/interest/1026?level=5`

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
    "level": 5
}
```

