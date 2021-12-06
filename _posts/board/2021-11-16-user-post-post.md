---
title: "유저 게시글 추가 [POST]"
date: 2021-11-15 22:21:00 +0900
categories: user-post POST
published: true

---

path로 전달된 유저의 게시글 추가

`POST` `http://3.135.231.171/api/user/{user_id}/post`

### URI Parameter

| Name    | In   | Required | Type | Description |
| ------- | ---- | -------- | ---- | ----------- |
| user_id | path | true     | Long | 유저의 id   |

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

`POST` `http://3.135.231.171/api/user/1/post`

Request Body

```json
{
    "interest" : {
        "id" : 1
    },
    "title" : "제목",
    "content" : "내용"
}
```

#### Sample Response

Status code: 200

```json
{
    "id": 1032,
    "interest":{
        "id": 1,
        "subject": null
    },
    "title": "제목",
    "content": "내용",
    "member":{
        "id": 1,
        "username": "user1",
        "password": "1234"
    },
    "writingDate": "2021-11-16T18:54:23.1714225"
}
```

