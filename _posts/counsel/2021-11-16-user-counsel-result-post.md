---
title: "유저별 상담결과 추가 [POST]"
date: 2021-11-15 22:21:00 +0900
categories: user-counsel-result POST
published: true

---

유저별 시간관리 상담 후 결과 저장.

`POST` `http://3.135.231.171/api/user/counsel-result`

### URI Parameter

### Request Body

| Name   | Type   | Description |
| ------ | ------ | ----------- |
| result | String | 상담 결과   |

### Response

| Status code | Type                | Description           |
| ----------- | ------------------- | --------------------- |
| 200 OK      | MemberCounselResult | 추가된 유저 상담 결과 |



### 예제

#### Sample Request

`POST` `http://3.135.231.171/api/user/1/counsel-result`

Request Body

```json
{
  "result" : "작은 일부터 시작하라.
  큰 목표는 당신이 당신이 매일 하는 모든 작은 일이 목표에 점점 다가갈때 이루어진다. - Maren Kate
  주변 정리부터 시작해보는것을 추천한다.
  시간은 금으로도 살 수 없다."
}
```

#### Sample Response

Status code: 200

```json
{
    "id": 15,
    "member":{
        "id": 3,
        "username": "test",
        "password": "$2a$10$ox4kqouwAtL1Bi7grOEXROfsZfEvr1qR160Cggn17ugdoPbNjLqvO"
    },
    "counselSolution": "{\n  \"result\" : \"작은 일부터 시작하라.\n  큰 목표는 당신이 당신이 매일 하는 모든 작은 일이 목표에 점점 다가갈때 이루어진다. - Maren Kate\n  주변 정리부터 시작해보는것을 추천한다.\n  시간은 금으로도 살 수 없다.\"\n}",
    "counselTime": "2021-12-07T02:59:52.1026455",
    "memberId": 3
}
```

