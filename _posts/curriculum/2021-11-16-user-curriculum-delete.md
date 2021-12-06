---
title: "유저의 커리큘럼 삭제 [DELETE]"
date: 2021-11-15 22:21:00 +0900
categories: user-curriculum DELETE
published: true
---

path로 전달된 유저의 커리큘럼 삭제

`DELETE` `http://3.135.231.171/api/user/{user_id}/curriculum`

### URI Parameter

| Name          | In    | Required | Type | Description        |
| ------------- | ----- | -------- | ---- | ------------------ |
| user_id       | path  | true     | Long | 유저의 id          |
| curriculum_id | query | true     | Long | 삭제할 커리큘럼 id |

### Response

| Status code | Type             | Description          |
| ----------- | ---------------- | -------------------- |
| 200 OK      | MemberCurriculum | 삭제된 유저 커리큘럼 |
| 500         |                  | 삭제 실패            |



### 예제

#### Sample Request

`DELETE` `http://3.135.231.171/api/user/1/curriculum?curriculum_id=2`

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
        "level": "beginner"
    }
}
```

