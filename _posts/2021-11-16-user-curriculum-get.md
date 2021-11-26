---
title: "유저의 커리큘럼 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-curriculum GET
published: true

---

path로 전달된 유저의 커리큘럼 목록 반환

`GET` `http://localhost:8080/api/user/{user_id}/curriculum`

### URI Parameter

| Name    | In   | Required | Type | Description |
| ------- | ---- | -------- | ---- | ----------- |
| user_id | path | true     | Long | 유저의 id   |

### Response

| Status code | Type                        | Description          |
| ----------- | --------------------------- | -------------------- |
| 200 OK      | Iterable\<MemberCurriculum> | 유저의 커리큘럼 목록 |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/user/1/curriculum`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1027,
        "member": {
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "curriculum": {
            "id": 2,
            "name": "beginner",
            "interest": {
                "id": 2,
                "subject": "job"
            },
            "level": "beginner"
        }
    },
    {
        "id": 1028,
        "member": {
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "curriculum": {
            "id": 1,
            "name": "sample_curriculum",
            "interest": {
                "id": 1,
                "subject": "workout"
            },
            "level": "expert"
        }
    }
]
```

