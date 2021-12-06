---
title: "유저 댓글 추가 [POST]"
date: 2021-11-15 22:21:00 +0900
categories: user-comment POST
published: true
---

query로 전달된 게시글의 유저 댓글 추가

`POST` `http://localhost:8080/api/user/{user_id}/comment`

### URI Parameter

| Name    | In    | Required | Type | Description             |
| ------- | ----- | -------- | ---- | ----------------------- |
| user_id | path  | true     | Long | 유저의 id               |
| post_id | query | true     | Long | 댓글을 작성할 게시글 id |

### Request Body

DB `Comment`

| Name    | Type   | Description |
| ------- | ------ | ----------- |
| content | String | 댓글 내용   |

### Response

| Status code | Type    | Description |
| ----------- | ------- | ----------- |
| 200 OK      | Comment | 생성된 댓글 |



### 예제

#### Sample Request

`POST` `http://localhost:8080/api/user/1/comment?post_id=1032`

Request Body

```json
{
    "content" : "댓글"
}
```

#### Sample Response

Status code: 200

```json
{
    "id": 1035,
    "post":{
        "id": 1032,
        "interest":{
            "id": 1,
            "subject": "workout"
        },
        "title": "수정",
        "content": "내용",
        "member":{
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "writingDate": "2021-11-16T18:54:23.171422"
    },
    "content": "댓글",
    "member":{
        "id": 1,
        "username": "user1",
        "password": "1234"
    },
    "writingDate": "2021-11-16T20:13:38.3669651"
}
```

