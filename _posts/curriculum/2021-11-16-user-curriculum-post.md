---
title: "유저 커리큘럼 추가 [POST]"
date: 2021-11-15 22:21:00 +0900
categories: user-curriculum POST
published: true

---

path로 전달된 유저의 커리큘럼 추가

`POST` `http://3.135.231.171/api/user/curriculum`

### URI Parameter

| Name          | In    | Required | Type | Description        |
| ------------- | ----- | -------- | ---- | ------------------ |
| curriculum_id | query | true     | Long | 추가할 커리큘럼 id |

### Response

| Status code | Type             | Description            |
| ----------- | ---------------- | ---------------------- |
| 200 OK      | MemberCurriculum | 유저에 추가된 커리큘럼 |



### 예제

#### Sample Request

`POST` `http://3.135.231.171/api/user/curriculum?curriculum_id=2`

#### Sample Response

Status code: 200

```json
{
    "id": 14,
    "member":{
        "id": 3,
        "username": "test",
        "password": "$2a$10$ox4kqouwAtL1Bi7grOEXROfsZfEvr1qR160Cggn17ugdoPbNjLqvO"
    },
    "curriculum":{
        "id": 2,
        "name": "프로그래밍 - 초급자",
        "interest":{
            "id": 2,
            "subject": "programming"
        },
        "level": "beginner"
    },
    "memberId": 3
}
```

