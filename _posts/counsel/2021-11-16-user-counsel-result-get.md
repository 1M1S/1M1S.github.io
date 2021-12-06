---
title: "유저 상담결과 목록 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-counsel-result GET
published: true


---

path로 전달된 유저의 상담 결과들 목록을 상담시간 기준으로 내림차순 정렬해서 반환

`GET` `http://3.135.231.171/api/user/counsel-result`

### URI Parameter

### Response

| Status code | Type                           | Description         |
| ----------- | ------------------------------ | ------------------- |
| 200 OK      | Iterable\<MemberCounselResult> | 유저 상담 결과 목록 |



### 예제

#### Sample Request

`GET` `http://3.135.231.171/api/user/counsel-result`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 16,
        "member":{
            "id": 3,
            "username": "test",
            "password": "$2a$10$ox4kqouwAtL1Bi7grOEXROfsZfEvr1qR160Cggn17ugdoPbNjLqvO"
        },
        "counselSolution": "{\n  \"result\" : \"휴식의 중요성 알기\"\n}",
        "counselTime": "2021-12-07T03:03:16.978364",
        "memberId": 3
    },
    {
        "id": 15,
        "member":{
            "id": 3,
            "username": "test",
            "password": "$2a$10$ox4kqouwAtL1Bi7grOEXROfsZfEvr1qR160Cggn17ugdoPbNjLqvO"
        },
        "counselSolution": "{\n  \"result\" : \"작은 일부터 시작하라.\n  큰 목표는 당신이 당신이 매일 하는 모든 작은 일이 목표에 점점 다가갈때 이루어진다. - Maren Kate\n  주변 정리부터 시작해보는것을 추천한다.\n  시간은 금으로도 살 수 없다.\"\n}",
        "counselTime": "2021-12-07T02:59:52.102645",
        "memberId": 3
    }
]
```

