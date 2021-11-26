---
title: "로그아웃 [POST]"
date: 2021-11-26 22:21:00 +0900
categories: auth
published: true
---

유저가 그룹장일 경우, 해당 그룹 수정

`PUT` `http://localhost:8080/logout`

### URI Parameter

### Request Body

DB `Group`

> 수정할 항목들의 값만 전달하면 된다. 나머진 null로 자동전달.

```json
{
}
```





### Response

| Status code | Type | Description   |
| ----------- | ---- | ------------- |
| 200 OK      | null | 아무것도 없음 |
| 500         |      | 서버 오류     |



### 예제

#### Sample Request

`POST` `http://localhost:8080/join`

Request Body

```json
{

}
```

#### Sample Response

Status code: 200

```json
{

}
```

