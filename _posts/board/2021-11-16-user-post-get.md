---
title: "유저가 작성한 게시글 목록 반환 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-post GET
published: true

---

유저가 작성한 게시글 목록 작성날짜를 기준으로 내림차순 정렬해서(최근 작성한 순으로) 반환

`GET` `http://localhost:8080/api/user/{user_id}/post`

### URI Parameter

| Name    | In   | Required | Type | Description |
| ------- | ---- | -------- | ---- | ----------- |
| user_id | path | true     | Long | 유저의 id   |

### Response

| Status code | Type            | Description |
| ----------- | --------------- | ----------- |
| 200 OK      | Iterable\<Post> | 게시글 목록 |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/user/1/post`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1033,
        "interest": {
            "id": 2,
            "subject": "job"
        },
        "title": "제목2",
        "content": "내용",
        "member": {
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "writingDate": "2021-11-16T19:00:52.098342"
    },
    {
        "id": 1032,
        "interest": {
            "id": 1,
            "subject": "workout"
        },
        "title": "제목",
        "content": "내용",
        "member": {
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "writingDate": "2021-11-16T18:54:23.171422"
    }
]
```

