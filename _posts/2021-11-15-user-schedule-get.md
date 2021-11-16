---
title: "유저 일정들 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-schedule get
published: true


---

path로 전달된 유저의 일정들 시작 시간 기준으로 오름차순 정렬해서 반환

`GET` `http://localhost:8080/api/user/{user_id}/schedule`

### URI Parameter

| Name    | In   | Required | Type | Description |
| ------- | ---- | -------- | ---- | ----------- |
| user_id | path | true     | Long | 유저의 id   |

### Response

| Status code | Type                      | Description |
| ----------- | ------------------------- | ----------- |
| 200 OK      | Iterable\<MemberSchedule> | 일정들 목록 |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/user/1/schedule`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1015,
        "member": {
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "content": "add2",
        "startTime": "2021-11-15T13:54:57",
        "endTime": "2021-11-15T14:54:25",
        "finish": false,
        "interest": {
            "id": 1,
            "subject": "workout"
        }
    },
    {
        "id": 1,
        "member": {
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "content": "schedule33",
        "startTime": "2021-11-17T14:54:57",
        "endTime": "2021-11-17T15:54:25",
        "finish": false,
        "interest": {
            "id": 3,
            "subject": "programming"
        }
    }
]
```

