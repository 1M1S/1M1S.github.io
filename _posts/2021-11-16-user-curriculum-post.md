---
title: "유저 커리큘럼 추가 [POST]"
date: 2021-11-15 22:21:00 +0900
categories: user curriculum post
published: true

---

path로 전달된 유저의 커리큘럼 추가

`POST` `http://localhost:8080/api/user/{user_id}/curriculum`

### URI Parameter

| Name          | In    | Required | Type | Description        |
| ------------- | ----- | -------- | ---- | ------------------ |
| user_id       | path  | true     | long | 유저의 id          |
| curriculum_id | query | true     | long | 추가할 커리큘럼 id |

### Response

| Status code | Type             | Description            |
| ----------- | ---------------- | ---------------------- |
| 200 OK      | MemberCurriculum | 유저에 추가된 커리큘럼 |



### 예제

#### Sample Request

`POST` `http://localhost:8080/api/user/1/curriculum?curriculum_id=2`

#### Sample Response

Status code: 200

```json
{
    "id": 1027,
    "member":{
        "id": 1,
        "username": "user1",
        "password": "1234"
    },
    "curriculum":{
        "id": 2,
        "name": "beginner",
        "interest":{
            "id": 2,
            "subject": "job"
        },
        "level": 3
    }
}
```

