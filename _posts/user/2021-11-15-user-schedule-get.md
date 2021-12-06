---
title: "일별 유저 일정목록 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-schedule GET
published: true


---

path로 전달된 유저, 날짜에 해당하는 일정 목록들을 시작 시간 기준으로 오름차순 정렬해서 반환해준다.

`GET` `http://localhost:8080/api/user/{user_id}/schedule`

### URI Parameter

| Name        | In    | Required | Type   | Description                            |
| ----------- | ----- | -------- | ------ | -------------------------------------- |
| user_id     | path  | true     | Long   | 유저의 id                              |
| search_time | query | true     | String | yyyy-MM-dd 형식의 문자열 (검색할 날짜) |

### Response

| Status code | Type                      | Description |
| ----------- | ------------------------- | ----------- |
| 200 OK      | Iterable\<MemberSchedule> | 일정들 목록 |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/user/1/schedule?search_time=2021-11-21`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1004,
        "member":{
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "content": "post",
        "startTime": "2021-11-21T13:54:57",
        "endTime": "2021-11-21T14:54:25",
        "finish": false,
        "interest":{
            "id": 1,
            "subject": "workout"
        }
    },
    {
        "id": 1005,
        "member":{
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "content": "post",
        "startTime": "2021-11-21T14:54:57",
        "endTime": "2021-11-21T15:54:25",
        "finish": false,
        "interest":{
            "id": 1,
            "subject": "workout"
        }
    }
]
```

