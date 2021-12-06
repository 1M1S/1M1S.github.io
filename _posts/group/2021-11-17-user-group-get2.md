---
title: "그룹 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-group GET
published: true

---

path로 전달된 그룹 읽어오기

`GET` `http://localhost:8080/api/user/{user_id}/group/{group_id}`

### URI Parameter

| Name     | In   | Required | Type | Description |
| -------- | ---- | -------- | ---- | ----------- |
| user_id  | path | true     | Long | 유저의 id   |
| group_id | path | true     | Long | 그룹의 id   |

### Response

| Status code | Type  | Description |
| ----------- | ----- | ----------- |
| 200 OK      | Party | 그룹        |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/user/1/group/2`

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
    "goal": "목표",
    "maximumNumberOfPeople": 10,
    "recruit": true
}
```

