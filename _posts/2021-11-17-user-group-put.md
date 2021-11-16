---
title: "그룹 수정 (그룹장) [PUT]"
date: 2021-11-15 22:21:00 +0900
categories: user-group PUT
published: true
---

유저가 그룹장일 경우, 해당 그룹 수정

`PUT` `http://localhost:8080/api/user/{user_id}/group/{group_id}`

### URI Parameter

| Name     | In   | Required | Type | Description      |
| -------- | ---- | -------- | ---- | ---------------- |
| user_id  | path | true     | Long | 유저의 id        |
| group_id | path | true     | Long | 수정할 그룹의 id |

### Request Body

DB `Group`

> 수정할 항목들의 값만 전달하면 된다. 나머진 null로 자동전달.

| Name                     | Type    | Description   |
| ------------------------ | ------- | ------------- |
| name                     | String  | 그룹명        |
| interest_id              | Long    | 그룹 관심분야 |
| goal                     | String  | 그룹 목표     |
| maximum_number_of_people | Integer | 그룹 최대인원 |
| recruit                  | Boolean | 그룹 모집여부 |

### Response

| Status code | Type  | Description                    |
| ----------- | ----- | ------------------------------ |
| 200 OK      | Party | 수정된 그룹                    |
| 400         |       | 해당 그룹의 그룹장이 아닐 경우 |



### 예제

#### Sample Request

`PUT` `http://localhost:8080/api/user/1/group/2`

Request Body

```json
{
    "goal": "수정된 목표",
    "recruit": false
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
        "subject": "workout"
    },
    "goal": "수정된 목표",
    "maximumNumberOfPeople": 10,
    "recruit": false
}
```

