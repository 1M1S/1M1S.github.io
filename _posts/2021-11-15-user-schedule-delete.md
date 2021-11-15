---
title: "유저 일정 삭제 [DELETE]"
date: 2021-11-15 22:21:00 +0900
categories: user schedule delete
published: true

---

path로 전달된 유저의 일정 삭제

`DELETE` `http://localhost:8080/api/user/{user_id}/schedule/{member_schedule_id}`

### URI Parameter

| Name               | In   | Required | Type | Description      |
| ------------------ | ---- | -------- | ---- | ---------------- |
| user_id            | path | true     | long | 유저의 id        |
| member_schedule_id | path | true     | long | 삭제할 일정의 id |

### Response

| Status code | Type           | Description             |
| ----------- | -------------- | ----------------------- |
| 200 OK      | MemberSchedule | 삭제된 일정             |
| 500         |                | 삭제할 일정이 없는 경우 |



### 예제

#### Sample Request

`DELETE` `http://localhost:8080/api/user/1/schedule/1025`

#### Sample Response

Status code: 200

```json
{
    "id": 1025,
    "member":{
        "id": 1,
        "username": "user1",
        "password": "1234"
    },
    "content": "수정된 일정",
    "startTime": "2021-11-18T13:54:57",
    "endTime": "2021-11-18T14:54:25",
    "finish": true,
    "interest":{
        "id": 1,
        "subject": "workout"
    }
}
```

