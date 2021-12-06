---
title: "유저 일정 수정 [PUT]"
date: 2021-11-15 22:21:00 +0900
categories: user-schedule PUT
published: true
---

path로 전달된 유저의 일정 수정

> #### 점수 연동
>
> 해당 일정의 유저, 관심사가 같은 Ranking의 score가 종료시간-시작시간에 따라 점수가 반영된다.
>
> * 일정완료여부가 false인 경우
>   * 일정완료여부가 true로 변경되면 점수 부여
> * 일정완료여부가 true인 경우
>   * 일정완료여부가 false로 변경되면 점수 제거
>   * 관심사가 변경되면 점수 이동
>   * 시작시간, 종료시간이 변경되면 점수 변경

`PUT` `http://3.135.231.171/api/user/schedule/{member_schedule_id}`

### URI Parameter

| Name               | In   | Required | Type | Description      |
| ------------------ | ---- | -------- | ---- | ---------------- |
| user_id            | path | true     | Long | 유저의 id        |
| member_schedule_id | path | true     | Long | 수정할 일정의 id |

### Request Body

DB `MemberSchedule`

> 수정할 항목들만 전달하면 된다. 나머지는 null로 전달됨.

| Name        | Type          | Description               |
| ----------- | ------------- | ------------------------- |
| content     | String        | 일정 내용                 |
| startTime   | LocalDateTime | 일정 시작 시간            |
| endTime     | LocalDateTime | 일정 종료 시간            |
| finish      | Boolean       | 일정 완료 여부            |
| interest_id | Long          | 일정이 해당되는 관심사 id |

### Response

| Status code | Type           | Description |
| ----------- | -------------- | ----------- |
| 200 OK      | MemberSchedule | 수정된 일정 |



### 예제

#### Sample Request

`PUT` `http://3.135.231.171/api/user/schedule/10`

Request Body

```json
{
    "content": "edited post2",
    "startTime": "2021-11-18T15:54:57",
    "endTime": "2021-11-18T18:54:25"
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
    "content": "edited post2",
    "startTime": "2021-11-18T15:54:57",
    "endTime": "2021-11-18T18:54:25",
    "finish": false,
    "interest":{
        "id": 3,
        "subject": "employ"
    }
}
```

