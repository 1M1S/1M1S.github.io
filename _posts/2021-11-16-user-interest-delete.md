---
title: "유저 관심분야 삭제 [DELETE]"
date: 2021-11-15 22:21:00 +0900
categories: user-interest DELETE
published: true


---

path로 전달된 유저의 관심분야 삭제

`DELETE` `http://localhost:8080/api/user/{user_id}/interest/{member_interest_id}`

### URI Parameter

| Name               | In   | Required | Type | Description               |
| ------------------ | ---- | -------- | ---- | ------------------------- |
| user_id            | path | true     | Long | 유저의 id                 |
| member_interest_id | path | true     | Long | 삭제할 유저의 관심분야 id |

### Response

| Status code | Type           | Description          |
| ----------- | -------------- | -------------------- |
| 200 OK      | MemberInterest | 삭제된 유저 관심분야 |
| 500         |                | 삭제 실패            |



### 예제

#### Sample Request

`DELETE` `http://localhost:8080/api/user/1/interest/1026`

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

