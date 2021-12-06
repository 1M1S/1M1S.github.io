---
title: "일별 유저 일정목록 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-schedule GET
published: true


---

path로 전달된 유저, 날짜에 해당하는 일정 목록들을 시작 시간 기준으로 오름차순 정렬해서 반환해준다.

`GET` `http://3.135.231.171/api/user/schedule`

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

`GET` `http://3.135.231.171/api/user/schedule?search_time=2021-11-18`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 9,
        "member":{
            "id": 3,
            "username": "test",
            "password": "$2a$10$ox4kqouwAtL1Bi7grOEXROfsZfEvr1qR160Cggn17ugdoPbNjLqvO"
        },
        "content": "post",
        "startTime": "2021-11-18T13:54:57",
        "endTime": "2021-11-18T14:54:25",
        "finish": true,
        "interest":{
            "id": 1,
            "subject": "exercise"
        }
    },
    {
        "id": 10,
        "member":{
            "id": 3,
            "username": "test",
            "password": "$2a$10$ox4kqouwAtL1Bi7grOEXROfsZfEvr1qR160Cggn17ugdoPbNjLqvO"
        },
        "content": "edited post2",
        "startTime": "2021-11-18T15:54:57",
        "endTime": "2021-11-18T18:54:25",
        "finish": false,
        "interest":{
            "id": 3,
            "subject": "employ"
        }
    }
]
```

