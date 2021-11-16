---
title: "유저 상담결과 추가 [POST]"
date: 2021-11-15 22:21:00 +0900
categories: user counsel result post
published: true

---

시간관리 상담 후 결과 저장.

>상담결과를 어떻게 정할지는 아직 미정.
>
>설문조사에 따라 시간관리 능력을 상, 중, 하로 분류?

`POST` `http://localhost:8080/api/user/{user_id}/counsel-result`

### URI Parameter

| Name    | In    | Required | Type   | Description |
| ------- | ----- | -------- | ------ | ----------- |
| user_id | path  | true     | Long   | 유저의 id   |
| result  | query | true     | String | 상담결과    |

### Response

| Status code | Type                | Description           |
| ----------- | ------------------- | --------------------- |
| 200 OK      | MemberCounselResult | 추가된 유저 상담 결과 |



### 예제

#### Sample Request

`POST` `http://localhost:8080/api/user/1/counsel-result?result=beginner`

#### Sample Response

Status code: 200

```json
{
    "id": 1029,
    "member":{
        "id": 1,
        "username": "user1",
        "password": "1234"
    },
    "counselSolution":{
        "id": 1,
        "result": "beginner",
        "solution": "계획세우기"
    },
    "counselTime": "2021-11-16T17:09:07.5895581"
}
```

