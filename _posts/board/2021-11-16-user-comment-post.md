---
title: "유저 댓글 추가 [POST]"
date: 2021-11-15 22:21:00 +0900
categories: user-comment POST
published: true
---

query로 전달된 게시글의 유저 댓글 추가

`POST` `http://3.135.231.171/api/user/comment`

### URI Parameter

| Name    | In    | Required | Type | Description             |
| ------- | ----- | -------- | ---- | ----------------------- |
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

`POST` `http://3.135.231.171/api/user/comment?post_id=1025`

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
    "id": 1043,
    "post":{
        "id": 1025,
        "interest":{
            "id": 0,
            "subject": "general"
        },
        "title": "teset",
        "content": "test",
        "member":{
            "id": 1001,
            "username": "jjj",
            "password": "$2a$10$nl1du0FdjzK9HQmWw1eT0eXJtuO3g.9aL22JbXSHymW7gQ1XhCOJe"
        },
        "writingDate": "2021-12-04T15:41:08"
    },
    "content": "댓글",
    "member":{
        "id": 1030,
        "username": "test",
        "password": "$2a$10$7JpJLI4KUV82mMcmNMY2A.rptegu4WxvgtjYsONETJQNrpSR8rZa6"
    },
    "writingDate": "2021-12-06T18:40:27.183677"
}
```

