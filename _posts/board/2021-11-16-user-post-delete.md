---
title: "유저 게시글 삭제 [DELETE]"
date: 2021-11-15 22:21:00 +0900
categories: user-post DELETE
published: true
---

path로 전달받은 id의 유저와 게시글의 작성자를 비교해서 해당 유저가 게시글을 작성했다면 게시글 삭제.

`DELETE` `http://localhost:8080/api/user/{user_id}/post/{post_id}`

### URI Parameter

| Name    | In   | Required | Type | Description        |
| ------- | ---- | -------- | ---- | ------------------ |
| user_id | path | true     | Long | 유저의 id          |
| post_id | path | true     | Long | 삭제할 게시글의 id |

### Response

| Status code | Type | Description                                                 |
| ----------- | ---- | ----------------------------------------------------------- |
| 200 OK      | Post | 삭제된 게시글                                               |
| 400         |      | 유저가 게시글 작성자가 아닌 경우, 삭제할 게시글이 없는 경우 |



### 예제

#### Sample Request

`DELETE` `http://localhost:8080/api/user/1/post/1034`

#### Sample Response

Status code: 200

```json
{
    "id": 1034,
    "interest":{
        "id": 2,
        "subject": "job"
    },
    "title": "제목2",
    "content": "내용",
    "member":{
        "id": 1,
        "username": "user1",
        "password": "1234"
    },
    "writingDate": "2021-11-16T19:49:30.811646"
}
```

