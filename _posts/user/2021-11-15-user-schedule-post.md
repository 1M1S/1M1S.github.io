---
title: "유저 일정 추가 [POST]"
date: 2021-11-15 22:21:00 +0900
categories: user-schedule POST
published: true
---

유저의 일정 추가

> 일정 생성시 완료여부는 자동으로 false로 설정되어 생성된다.

`POST` `http://3.135.231.171/api/user/schedule`

### URI Parameter

### Request Body

DB `MemberSchedule`

| Name        | Type          | Description               |
| ----------- | ------------- | ------------------------- |
| content     | String        | 일정 내용                 |
| startTime   | LocalDateTime | 일정 시작 시간            |
| endTime     | LocalDateTime | 일정 종료 시간            |
| interest_id | Long          | 일정이 해당되는 관심사 id |

### Response

| Status code | Type           | Description |
| ----------- | -------------- | ----------- |
| 200 OK      | MemberSchedule | 생성된 일정 |



### 예제

#### Sample Request

`POST` `http://3.135.231.171/api/user/schedule`

Request Body

```json
{
    "content": "post2",
    "startTime": "2021-11-18T13:54:57",
    "endTime": "2021-11-18T14:54:25",
    "interest": {
        "id": 3
    }
}
```

#### Sample Response

Status code: 200

```json
{
    "id": 10,
    "member":{
        "id": 3,
        "username": "test",
        "password": "$2a$10$ox4kqouwAtL1Bi7grOEXROfsZfEvr1qR160Cggn17ugdoPbNjLqvO"
    },
    "content": "post2",
    "startTime": "2021-11-18T13:54:57",
    "endTime": "2021-11-18T14:54:25",
    "finish": false,
    "interest":{
        "id": 3,
        "subject": null
    }
}
```

