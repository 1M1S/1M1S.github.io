---
title: "유저 일정 수정 [PUT]"
date: 2021-11-15 22:21:00 +0900
categories: user schedule put
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

`PUT` `http://localhost:8080/api/user/{user_id}/schedule/{member_schedule_id}`

### URI Parameter

| Name               | In   | Required | Type | Description      |
| ------------------ | ---- | -------- | ---- | ---------------- |
| user_id            | path | true     | long | 유저의 id        |
| member_schedule_id | path | true     | long | 수정할 일정의 id |

### Request Body

DB `MemberSchedule`

> 수정할 항목들만 전달하면 된다. 나머지는 null로 전달됨.

| Name        | Type          | Description               |
| ----------- | ------------- | ------------------------- |
| content     | String        | 일정 내용                 |
| startTime   | LocalDateTime | 일정 시작 시간            |
| endTime     | LocalDateTime | 일정 종료 시간            |
| finish      | Boolean       | 일정 완료 여부            |
| interest_id | long          | 일정이 해당되는 관심사 id |

### Response

| Status code | Type           | Description |
| ----------- | -------------- | ----------- |
| 200 OK      | MemberSchedule | 수정된 일정 |



### 예제

#### Sample Request

`PUT` `http://localhost:8080/api/user/1/schedule/1025`

Request Body

```json
{
    "content": "수정된 일정",
    "finish": true
}
```

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

