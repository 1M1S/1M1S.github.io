---
title: "유저 상담결과 목록 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user counsel-result get
published: true


---

path로 전달된 유저의 상담 결과들 목록을 상담시간을 기준으로 오름차순 정렬해서 반환

`GET` `http://localhost:8080/api/user/{user_id}/counsel-result`

### URI Parameter

| Name    | In   | Required | Type | Description |
| ------- | ---- | -------- | ---- | ----------- |
| user_id | path | true     | Long | 유저의 id   |

### Response

| Status code | Type                           | Description         |
| ----------- | ------------------------------ | ------------------- |
| 200 OK      | Iterable\<MemberCounselResult> | 유저 상담 결과 목록 |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/user/1/counsel-result`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1029,
        "member": {
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "counselSolution": {
            "id": 1,
            "result": "beginner",
            "solution": "계획세우기"
        },
        "counselTime": "2021-11-16T17:09:07.589558"
    },
    {
        "id": 1031,
        "member": {
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "counselSolution": {
            "id": 3,
            "result": "senior",
            "solution": "앞으로도 지금처럼"
        },
        "counselTime": "2021-11-16T17:17:55.160018"
    }
]
```

