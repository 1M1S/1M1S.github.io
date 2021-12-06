---
title: "유저 게시글 추가 [POST]"
date: 2021-11-15 22:21:00 +0900
categories: user-post POST
published: true

---

path로 전달된 유저의 게시글 추가

`POST` `http://3.135.231.171/api/user/post`

### URI Parameter

### Request Body

DB `Post`

| Name        | Type   | Description        |
| ----------- | ------ | ------------------ |
| interest_id | Long   | 게시글 관심분야 ID |
| title       | String | 게시글 제목        |
| content     | String | 게시글 내용        |

### Response

| Status code | Type | Description   |
| ----------- | ---- | ------------- |
| 200 OK      | Post | 생성된 게시글 |



### 예제

#### Sample Request

`POST` `http://3.135.231.171/api/user/post`

Request Body

```json
{
    "interest" : {
        "id" : 0
    },
    "title" : "제목",
    "content" : "내용"
}
```

#### Sample Response

Status code: 200

```json
{
    "id": 18,
    "interest":{
        "id": 0,
        "subject": "general"
    },
    "title": "제목",
    "content": "내용",
    "member":{
        "id": 3,
        "username": "test",
        "password": "$2a$10$ox4kqouwAtL1Bi7grOEXROfsZfEvr1qR160Cggn17ugdoPbNjLqvO"
    },
    "writingDate": "2021-12-07T03:30:12"
}
```

