---
title: "게시글 댓글 목록 반환 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: comment GET
published: true



---

path로 전달받은 id 게시글의 댓글 목록 작성날짜를 기준으로 오름차순 정렬해서 반환

`GET` `http://3.135.231.171/api/post/{post_id}/comment`

### URI Parameter

| Name    | In   | Required | Type | Description |
| ------- | ---- | -------- | ---- | ----------- |
| post_id | path | true     | Long | 게시글의 id |

### Response

| Status code | Type               | Description |
| ----------- | ------------------ | ----------- |
| 200 OK      | Iterable\<Comment> | 댓글 목록   |



### 예제

#### Sample Request

`GET` `http://3.135.231.171/api/post/1032/comment`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1035,
        "post": {
            "id": 1032,
            "interest": {
                "id": 1,
                "subject": "workout"
            },
            "title": "수정",
            "content": "내용",
            "member": {
                "id": 1,
                "username": "user1",
                "password": "1234"
            },
            "writingDate": "2021-11-16T18:54:23.171422"
        },
        "content": "댓글",
        "member": {
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "writingDate": "2021-11-16T20:13:38.366965"
    },
    {
        "id": 1036,
        "post": {
            "id": 1032,
            "interest": {
                "id": 1,
                "subject": "workout"
            },
            "title": "수정",
            "content": "내용",
            "member": {
                "id": 1,
                "username": "user1",
                "password": "1234"
            },
            "writingDate": "2021-11-16T18:54:23.171422"
        },
        "content": "댓글2",
        "member": {
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "writingDate": "2021-11-16T20:17:38.366965"
    }
]
```

