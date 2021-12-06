---
title: "유저가 속해있는 그룹들 목록 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-group GET
published: true
---

유저가 속해있는 그룹들 목록 읽어오기

`GET` `http://3.135.231.171/api/user/{user_id}/group`

### URI Parameter

| Name    | In   | Required | Type | Description |
| ------- | ---- | -------- | ---- | ----------- |
| user_id | path | true     | Long | 유저의 id   |

### Response

| Status code | Type             | Description                 |
| ----------- | ---------------- | --------------------------- |
| 200 OK      | Iterable\<Party> | 유저가 속해있는 그룹들 목록 |



### 예제

#### Sample Request

`GET` `http://3.135.231.171/api/user/1/group`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 2,
        "name": "new group",
        "interest":{
            "id": 1,
            "subject": "workout"
        },
        "goal": "목표",
        "maximumNumberOfPeople": 10,
        "recruit": true
    },
    {
        "id": 4,
        "name": "new group 2",
        "interest":{
            "id": 1,
            "subject": "workout"
        },
        "goal": "목표",
        "maximumNumberOfPeople": 10,
        "recruit": true
    }
]
```

