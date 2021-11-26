---
title: "관심분야별 상위 3명 랭커 출력 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-ranking GET
published: true

---

query로 전달된 관심분야에서 1등, 2등, 3등 순으로 Ranking 반환

`GET` `http://localhost:8080/api/ranking`

### URI Parameter

| Name        | In    | Required | Type | Description |
| ----------- | ----- | -------- | ---- | ----------- |
| interest_id | query | true     | Long | 관심분야 id |

### Response

| Status code | Type               | Description                     |
| ----------- | ------------------ | ------------------------------- |
| 200 OK      | Iterable\<Ranking> | 관심분야에서 상위 유저 3명 반환 |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/ranking/top3?interest_id=0`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1,
        "member": {
            "id": 2,
            "username": "user2",
            "password": "2345"
        },
        "interest": {
            "id": 0,
            "subject": "general"
        },
        "score": 100
    },
    {
        "id": 5,
        "member": {
            "id": 4,
            "username": "user4",
            "password": "4567"
        },
        "interest": {
            "id": 0,
            "subject": "general"
        },
        "score": 99
    },
    {
        "id": 3,
        "member": {
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "interest": {
            "id": 0,
            "subject": "general"
        },
        "score": 90
    }
]
```

