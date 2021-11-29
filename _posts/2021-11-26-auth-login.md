---
title: "로그인 [GET]"
date: 2021-11-26 22:21:00 +0900
categories: auth
published: true
---

유저가 그룹장일 경우, 해당 그룹 수정

`PUT` `http://localhost:8080/auth/login`

### URI Parameter

### Request Body

DB `Group`

> 수정할 항목들의 값만 전달하면 된다. 나머진 null로 자동전달.

```json
{
	"username": "asdqwr",//string
    "password": "aqwe"//string
}
```





### Response

| Status code | Type   | Description |
| ----------- | ------ | ----------- |
| 200 OK      | tokens | 토큰 정보   |
| 500         |        | 서버 오류   |



### 예제

#### Sample Request

GET `http://localhost:8080/login`

Request Body

```json
{
	"username": "asdqwr", //string
    "password": "aqwe" //string
}
```

#### Sample Response

Status code: 200

```json
{
  "accessToken": "eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJudWxsIiwiaWF0IjoxNjM4MTcwNjgwLCJleHAiOjE2MzgxNzE2ODB9.Lcw_f2-fEkye86tR4UVNxzfYk4fiBTyc0PRdgKIEMRs"
}
```

