---
title: "유저 상담결과 목록 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-counsel-result GET
published: true


---

path로 전달된 유저의 상담 결과들 목록을 상담시간 기준으로 내림차순 정렬해서 반환

`GET` `http://3.135.231.171/api/user/{user_id}/counsel-result`

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

`GET` `http://3.135.231.171/api/user/1/counsel-result`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 2,
        "member": {
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "counselSolution": "{\n  \"result\" : \"솔루션1\n  솔루션2\n  솔루션3\"\n}",
        "counselTime": "2021-11-27T02:18:51.157082"
    },
    {
        "id": 1,
        "member": {
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "counselSolution": "{\n  \"result\" : \"솔루션1\n  솔루션2\n  솔루션3\"\n}",
        "counselTime": "2021-11-27T02:17:38.062546"
    }
]
```

