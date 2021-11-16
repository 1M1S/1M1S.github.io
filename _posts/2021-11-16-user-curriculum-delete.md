---
title: "유저의 커리큘럼 삭제 [DELETE]"
date: 2021-11-15 22:21:00 +0900
categories: user-curriculum DELETE
published: true
---

path로 전달된 유저의 커리큘럼 삭제

`DELETE` `http://localhost:8080/api/user/{user_id}/interest/{member_curriculum_id}`

### URI Parameter

| Name                 | In   | Required | Type | Description            |
| -------------------- | ---- | -------- | ---- | ---------------------- |
| user_id              | path | true     | Long | 유저의 id              |
| member_curriculum_id | path | true     | Long | 삭제할 유저커리큘럼 id |

### Response

| Status code | Type             | Description          |
| ----------- | ---------------- | -------------------- |
| 200 OK      | MemberCurriculum | 삭제된 유저 커리큘럼 |
| 500         |                  | 삭제 실패            |



### 예제

#### Sample Request

`DELETE` `http://localhost:8080/api/user/1/curriculum/1027`

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

