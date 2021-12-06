---
title: "로그인 [POST]"
date: 2021-11-26 22:21:00 +0900
categories: auth
published: true
---

유저명과 암호를 전달하면 앞으로 유저 인증을 할때 사용할 토큰을 반환해준다.

로그인 이후로 요청을 보낼때 `x-access-token` 값으로 이 토큰을 넣어서 전달해주면 된다.

`POST` `http://3.135.231.171/auth/login`

### URI Parameter

### Request Body

```json
{
    "username": "test",
    "password": "1234"
}
```

### Response

| Status code | Type   | Description |
| ----------- | ------ | ----------- |
| 200 OK      | tokens | 토큰 정보   |
| 500         |        | 서버 오류   |



### 예제

#### Sample Request

GET `http://3.135.231.171/login`

Request Body

```json
{
    "username": "test",
    "password": "1234"
}
```

#### Sample Response

Status code: 200

```json
{
    "accessToken": "eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiIxMDMwIiwiaWF0IjoxNjM4NzgzMDc5LCJleHAiOjEwMDAwMDE2Mzg3ODMwNzl9.05kaxXmS9xHCtE1_nBMTDReZu1gE0FOcIcBxMbb6ZrU"
}
```

