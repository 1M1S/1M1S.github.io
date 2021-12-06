---
title: "유저 일정 삭제 [DELETE]"
date: 2021-11-15 22:21:00 +0900
categories: user-schedule DELETE
published: true
---

path로 전달된 유저의 일정 삭제

> #### 점수 연동
>
> 일정의 완료여부가 true면 부여됐던 점수가 제거된다.

`DELETE` `http://3.135.231.171/api/user/schedule/{member_schedule_id}`

### URI Parameter

| Name               | In   | Required | Type | Description      |
| ------------------ | ---- | -------- | ---- | ---------------- |
| member_schedule_id | path | true     | Long | 삭제할 일정의 id |

### Response

| Status code | Type           | Description             |
| ----------- | -------------- | ----------------------- |
| 200 OK      | MemberSchedule | 삭제된 일정             |
| 500         |                | 삭제할 일정이 없는 경우 |



### 예제

#### Sample Request

`DELETE` `http://3.135.231.171/api/user/schedule/9`

#### Sample Response

Status code: 200

```json
{
    "id": 9,
    "member":{
        "id": 3,
        "username": "test",
        "password": "$2a$10$ox4kqouwAtL1Bi7grOEXROfsZfEvr1qR160Cggn17ugdoPbNjLqvO"
    },
    "content": "post",
    "startTime": "2021-11-18T13:54:57",
    "endTime": "2021-11-18T17:54:25",
    "finish": true,
    "interest":{
        "id": 1,
        "subject": "exercise"
    }
}
```

