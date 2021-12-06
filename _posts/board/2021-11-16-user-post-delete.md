---
title: "유저 게시글 삭제 [DELETE]"
date: 2021-11-15 22:21:00 +0900
categories: user-post DELETE
published: true
---

path로 전달받은 id의 유저와 게시글의 작성자를 비교해서 해당 유저가 게시글을 작성했다면 게시글 삭제.

`DELETE` `http://3.135.231.171/api/user/post/{post_id}`

### URI Parameter

| Name    | In   | Required | Type | Description        |
| ------- | ---- | -------- | ---- | ------------------ |
| post_id | path | true     | Long | 삭제할 게시글의 id |

### Response

| Status code | Type | Description                                                 |
| ----------- | ---- | ----------------------------------------------------------- |
| 200 OK      | Post | 삭제된 게시글                                               |
| 400         |      | 유저가 게시글 작성자가 아닌 경우, 삭제할 게시글이 없는 경우 |



### 예제

#### Sample Request

`DELETE` `http://3.135.231.171/api/user/post/1034`

#### Sample Response

Status code: 200

```json
{
    "id": 19,
    "interest":{
        "id": 3,
        "subject": "employ"
    },
    "title": "수정된 제목",
    "content": "수정된 내용",
    "member":{
        "id": 3,
        "username": "test",
        "password": "$2a$10$ox4kqouwAtL1Bi7grOEXROfsZfEvr1qR160Cggn17ugdoPbNjLqvO"
    },
    "writingDate": "2021-12-07T03:31:24"
}
```

