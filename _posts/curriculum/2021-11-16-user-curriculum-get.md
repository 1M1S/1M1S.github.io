---
title: "유저의 커리큘럼 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-curriculum GET
published: true

---

path로 전달된 유저의 커리큘럼 목록 반환

`GET` `http://3.135.231.171/api/user/curriculum`

### URI Parameter

### Response

| Status code | Type                        | Description          |
| ----------- | --------------------------- | -------------------- |
| 200 OK      | Iterable\<MemberCurriculum> | 유저의 커리큘럼 목록 |



### 예제

#### Sample Request

`GET` `http://3.135.231.171/api/user/curriculum`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1,
        "member":{
            "id": 3,
            "username": "test",
            "password": "$2a$10$ox4kqouwAtL1Bi7grOEXROfsZfEvr1qR160Cggn17ugdoPbNjLqvO"
        },
        "curriculum":{
            "id": 0,
            "name": "운동 - 초급자",
            "interest":{
                "id": 1,
                "subject": "exercise"
            },
            "level": "beginner"
        },
        "memberId": 3
    },
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
]
```

