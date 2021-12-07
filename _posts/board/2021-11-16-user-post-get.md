---
title: "유저가 작성한 게시글 목록 반환 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-post
published: true

---

유저가 작성한 게시글 목록 작성날짜를 기준으로 내림차순 정렬해서(최근 작성한 순으로) 반환

`GET` `http://3.135.231.171/api/user/post`

### URI Parameter

### Response

| Status code | Type            | Description |
| ----------- | --------------- | ----------- |
| 200 OK      | Iterable\<Post> | 게시글 목록 |



### 예제

#### Sample Request

`GET` `http://3.135.231.171/api/user/post`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 19,
        "interest":{
            "id": 3,
            "subject": "employ"
        },
        "title": "제목2",
        "content": "내용2",
        "member":{
            "id": 3,
            "username": "test",
            "password": "$2a$10$ox4kqouwAtL1Bi7grOEXROfsZfEvr1qR160Cggn17ugdoPbNjLqvO"
        },
        "writingDate": "2021-12-07T03:31:24"
    },
    {
        "id": 18,
        "interest":{
            "id": 0,
            "subject": "general"
        },
        "title": "제목",
        "content": "내용",
        "member":{
            "id": 3,
            "username": "test",
            "password": "$2a$10$ox4kqouwAtL1Bi7grOEXROfsZfEvr1qR160Cggn17ugdoPbNjLqvO"
        },
        "writingDate": "2021-12-07T03:30:12"
    }
]
```

