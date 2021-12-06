---
title: "유저 관심분야 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-interest GET
published: true
---

path로 전달된 유저의 관심분야 목록 반환

`GET` `http://localhost:8080//api/user/{user_id}/interest`

### URI Parameter

| Name    | In   | Required | Type | Description |
| ------- | ---- | -------- | ---- | ----------- |
| user_id | path | true     | Long | 유저의 id   |

### Response

| Status code | Type                      | Description        |
| ----------- | ------------------------- | ------------------ |
| 200 OK      | Iterable\<MemberInterest> | 유저 관심분야 목록 |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/user/1/interest`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1004,
        "member": {
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "interest": {
            "id": 2,
            "subject": "job"
        },
        "level": 7
    },
    {
        "id": 1026,
        "member": {
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "interest": {
            "id": 1,
            "subject": "workout"
        },
        "level": 7
    }
]
```

