---
title: "유저 댓글 수정 [PUT]"
date: 2021-11-15 22:21:00 +0900
categories: user-comment PUT
published: true
---

path로 전달받은 id의 유저와 댓글의 작성자를 비교해서 해당 유저가 댓글을 작성했다면 댓글 수정.

`PUT` `http://localhost:8080/api/user/{user_id}/comment/{comment_id}`

### URI Parameter

| Name       | In   | Required | Type | Description      |
| ---------- | ---- | -------- | ---- | ---------------- |
| user_id    | path | true     | Long | 유저의 id        |
| comment_id | path | true     | Long | 수정할 댓글의 id |

### Request Body

DB `Comment`

> 수정할 항목만 전달하면 된다. 나머지는 자동으로 null로 전달.

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

`PUT` `http://localhost:8080/api/user/1/comment/1036`

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
    "id": 1036,
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
    "content": "수정된 댓글",
    "member":{
        "id": 1,
        "username": "user1",
        "password": "1234"
    },
    "writingDate": "2021-11-16T20:16:39.56691"
}
```

