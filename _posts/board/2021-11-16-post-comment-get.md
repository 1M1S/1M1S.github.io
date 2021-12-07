---
title: "게시글 댓글 목록 반환 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: comment
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

`GET` `http://3.135.231.171/api/post/1026/comment`

#### Sample Response

Status code: 200

```json

[
    {
        "id": 1027,
        "post":{
            "id": 1026,
            "interest":{
                "id": 0,
                "subject": "general"
            },
            "title": "하이 치산",
            "content": "하이 준화",
            "member":{
                "id": 1,
                "username": "vcho1958",
                "password": "$2a$10$jI1tgF/qoAB6PEN.NUroOOoVfbVQaasSdMNPkvFR/15R3a0QQFuQi"
            },
            "writingDate": "2021-12-04T15:41:40"
        },
        "content": "ㅁㄴㅇ",
        "member":{
            "id": 1,
            "username": "vcho1958",
            "password": "$2a$10$jI1tgF/qoAB6PEN.NUroOOoVfbVQaasSdMNPkvFR/15R3a0QQFuQi"
        },
        "writingDate": "2021-12-04T15:42:16.547277"
    }
]
```

