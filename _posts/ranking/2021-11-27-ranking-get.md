---
title: "관심분야별 상위 3명 랭커 출력 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: ranking GET
published: true

---

query로 전달된 관심분야에서 1등, 2등, 3등 순으로 Ranking 반환

`GET` `http://3.135.231.171/api/ranking`

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

`GET` `http://3.135.231.171/api/ranking/top3?interest_id=1`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1034,
        "member":{
            "id": 1030,
            "username": "test",
            "password": "$2a$10$7JpJLI4KUV82mMcmNMY2A.rptegu4WxvgtjYsONETJQNrpSR8rZa6"
        },
        "interest":{
            "id": 1,
            "subject": "exercise"
        },
        "score": 118
    },
    {
        "id": 4,
        "member":{
            "id": 1,
            "username": "vcho1958",
            "password": "$2a$10$jI1tgF/qoAB6PEN.NUroOOoVfbVQaasSdMNPkvFR/15R3a0QQFuQi"
        },
        "interest":{
            "id": 1,
            "subject": "exercise"
        },
        "score": 0
    },
    {
        "id": 1004,
        "member":{
            "id": 1001,
            "username": "jjj",
            "password": "$2a$10$nl1du0FdjzK9HQmWw1eT0eXJtuO3g.9aL22JbXSHymW7gQ1XhCOJe"
        },
        "interest":{
            "id": 1,
            "subject": "exercise"
        },
        "score": 0
    }
]
```

