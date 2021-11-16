---
title: "유저가 작성한 댓글 목록 반환 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user 댓글 GET
published: true


---

유저가 작성한 댓글 목록 작성날짜를 기준으로 내림차순 정렬해서(최근 작성한 순으로) 반환

`GET` `http://localhost:8080/api/user/{user_id}/comment`

### URI Parameter

| Name    | In   | Required | Type | Description |
| ------- | ---- | -------- | ---- | ----------- |
| user_id | path | true     | Long | 유저의 id   |

### Response

| Status code | Type               | Description |
| ----------- | ------------------ | ----------- |
| 200 OK      | Iterable\<Comment> | 댓글 목록   |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/user/1/comment`

#### Sample Response

Status code: 200

```json
[
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
        "writingDate": "2021-11-16T20:16:39.56691"
    },
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
    }
]
```

