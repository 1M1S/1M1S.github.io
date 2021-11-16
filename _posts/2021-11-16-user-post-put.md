---
title: "유저 게시글 수정 [PUT]"
date: 2021-11-15 22:21:00 +0900
categories: user-post PUT
published: true
---

path로 전달받은 id의 유저와 게시글의 작성자를 비교해서 해당 유저가 게시글을 작성했다면 게시글 수정.

`PUT` `http://localhost:8080/api/user/{user_id}/post/{post_id}`

### URI Parameter

| Name    | In   | Required | Type | Description        |
| ------- | ---- | -------- | ---- | ------------------ |
| user_id | path | true     | Long | 유저의 id          |
| post_id | path | true     | Long | 수정할 게시글의 id |

### Request Body

DB `Post`

> 수정할 항목만 전달하면 된다. 나머지는 자동으로 null로 전달.

| Name        | Type   | Description        |
| ----------- | ------ | ------------------ |
| interest_id | Long   | 게시글 관심분야 ID |
| title       | String | 게시글 제목        |
| content     | String | 게시글 내용        |

### Response

| Status code | Type | Description                                                 |
| ----------- | ---- | ----------------------------------------------------------- |
| 200 OK      | Post | 수정된 게시글                                               |
| 400         |      | 유저가 게시글 작성자가 아닌 경우, 수정할 게시글이 없는 경우 |



### 예제

#### Sample Request

`PUT` `http://localhost:8080/api/user/1/post/1033`

Request Body

```json
{
    "title" : "수정된 제목"
}
```

#### Sample Response

Status code: 200

```json
{
    "id": 1033,
    "interest":{
        "id": 2,
        "subject": "job"
    },
    "title": "수정된 제목",
    "content": "내용",
    "member":{
        "id": 1,
        "username": "user1",
        "password": "1234"
    },
    "writingDate": "2021-11-16T19:00:52.098342"
}
```

