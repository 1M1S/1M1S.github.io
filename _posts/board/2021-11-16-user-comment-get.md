---
title: "유저가 작성한 댓글 목록 반환 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-comment GET
published: true


---

유저가 작성한 댓글 목록 작성날짜를 기준으로 오름차순 정렬해서 반환

`GET` `http://3.135.231.171/api/user/comment`

### URI Parameter

### Response

| Status code | Type               | Description |
| ----------- | ------------------ | ----------- |
| 200 OK      | Iterable\<Comment> | 댓글 목록   |



### 예제

#### Sample Request

`GET` `http://3.135.231.171/api/user/comment`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1043,
        "post":{"id": 1025, "interest":{"id": 0, "subject": "general" },…},
        "content": "댓글",
        "member":{
            "id": 1030,
            "username": "test",
            "password": "$2a$10$7JpJLI4KUV82mMcmNMY2A.rptegu4WxvgtjYsONETJQNrpSR8rZa6"
        },
        "writingDate": "2021-12-06T18:40:27.183677"
    },
    {
        "id": 1044,
        "post":{"id": 1025, "interest":{"id": 0, "subject": "general" },…},
        "content": "댓글22",
        "member":{
            "id": 1030,
            "username": "test",
            "password": "$2a$10$7JpJLI4KUV82mMcmNMY2A.rptegu4WxvgtjYsONETJQNrpSR8rZa6"
        },
        "writingDate": "2021-12-06T18:40:58.50907"
    }
]
```

