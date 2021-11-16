---
title: "그룹 생성 [POST]"
date: 2021-11-15 22:21:00 +0900
categories: user-group POST
published: true
---

path로 전달된 유저를 그룹장으로 그룹 생성.

`POST` `http://localhost:8080/api/user/{user_id}/group`

### URI Parameter

| Name    | In   | Required | Type | Description |
| ------- | ---- | -------- | ---- | ----------- |
| user_id | path | true     | Long | 유저의 id   |

### Request Body

DB `Group`

| Name                     | Type    | Description   |
| ------------------------ | ------- | ------------- |
| name                     | String  | 그룹명        |
| interest_id              | Long    | 그룹 관심분야 |
| goal                     | String  | 그룹 목표     |
| maximum_number_of_people | Integer | 그룹 최대인원 |
| recruit                  | Boolean | 그룹 모집여부 |

### Response

| Status code | Type  | Description |
| ----------- | ----- | ----------- |
| 200 OK      | Party | 생성된 그룹 |



### 예제

#### Sample Request

`POST` `http://localhost:8080/api/user/1/group`

Request Body

```json
{
    "name": "new group",
    "interest": {
        "id": 1
    },
    "goal": "목표",
    "maximumNumberOfPeople": 10,
    "recruit": true
}
```

#### Sample Response

Status code: 200

```json
{
    "id": 2,
    "name": "new group",
    "interest":{
        "id": 1,
        "subject": null
    },
    "goal": "목표",
    "maximumNumberOfPeople": 10,
    "recruit": true
}
```

