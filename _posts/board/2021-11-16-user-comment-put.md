---
title: "유저 댓글 수정 [PUT]"
date: 2021-11-15 22:21:00 +0900
categories: user-comment PUT
published: true
---

path로 전달받은 id의 유저와 댓글의 작성자를 비교해서 해당 유저가 댓글을 작성했다면 댓글 수정.

`PUT` `http://3.135.231.171/api/user/comment/{comment_id}`

### URI Parameter

| Name       | In   | Required | Type | Description      |
| ---------- | ---- | -------- | ---- | ---------------- |
| comment_id | path | true     | Long | 수정할 댓글의 id |

### Request Body

DB `Comment`

| Name    | Type   | Description |
| ------- | ------ | ----------- |
| content | String | 댓글 내용   |

### Response

| Status code | Type    | Description                                             |
| ----------- | ------- | ------------------------------------------------------- |
| 200 OK      | Comment | 수정된 댓글                                             |
| 400         |         | 유저가 댓글 작성자가 아닌 경우, 수정할 댓글이 없는 경우 |



### 예제

#### Sample Request

`PUT` `http://3.135.231.171/api/user/comment/1043`

Request Body

```json
{
    "content" : "수정된 댓글"
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
    "content": "수정된댓글",
    "member":{
        "id": 1030,
        "username": "test",
        "password": "$2a$10$7JpJLI4KUV82mMcmNMY2A.rptegu4WxvgtjYsONETJQNrpSR8rZa6"
    },
    "writingDate": "2021-12-06T18:40:27.183677"
}
```

