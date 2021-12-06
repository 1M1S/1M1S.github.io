---
title: "유저의 커리큘럼 삭제 [DELETE]"
date: 2021-11-15 22:21:00 +0900
categories: user-curriculum DELETE
published: true
---

path로 전달된 유저의 커리큘럼 삭제

`DELETE` `http://3.135.231.171/api/user/curriculum`

### URI Parameter

| Name          | In    | Required | Type | Description        |
| ------------- | ----- | -------- | ---- | ------------------ |
| curriculum_id | query | true     | Long | 삭제할 커리큘럼 id |

> user_curriculum_id가 아니라 curriculum_id임에 주의. 예시를 보면 이해하기 더 쉬울 것이다.

### Response

| Status code | Type             | Description          |
| ----------- | ---------------- | -------------------- |
| 200 OK      | MemberCurriculum | 삭제된 유저 커리큘럼 |
| 500         |                  | 삭제 실패            |



### 예제

#### Sample Request

`DELETE` `http://3.135.231.171/api/user/curriculum?curriculum_id=0`

#### Sample Response

Status code: 200

```json
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
}
```

