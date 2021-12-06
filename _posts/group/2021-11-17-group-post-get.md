---
title: "그룹 게시글 목록 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: group-post GET
published: true
---

그룹멤버일 경우 그룹 멤버들이 작성한 게시글 목록 반환

> authority 값이 "승인대기"일 경우 그룹 멤버 목록을 볼 수 없다.

`GET` `http://3.135.231.171/api/user/{user_id}/group/{group_id}/post`

### URI Parameter

| Name     | In   | Required | Type | Description |
| -------- | ---- | -------- | ---- | ----------- |
| user_id  | path | true     | Long | 유저 id     |
| group_id | path | true     | Long | 그룹 id     |

### Response

| Status code | Type            | Description             |
| ----------- | --------------- | ----------------------- |
| 200 OK      | Iterable\<Post> | 그룹 게시글 목록        |
| 400         |                 | 그룹 구성원이 아닌 경우 |



### 예제 1

#### Sample Request

`GET` `http://3.135.231.171/api/user/2/group/1/post`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1,
        "interest":{
            "id": 2,
            "subject": "programming"
        },
        "title": "제목1",
        "content": "내용",
        "member":{
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "writingDate": "2021-11-17T02:40:26"
    },
    {
        "id": 2,
        "interest":{
            "id": 3,
            "subject": "job"
        },
        "title": "제목2",
        "content": "내용",
        "member":{
            "id": 2,
            "username": "user2",
            "password": "2345"
        },
        "writingDate": "2021-11-17T02:40:26"
    }
]
```



### 예제 2

#### Sample Request

`GET` `http://3.135.231.171/api/user/3/group/1/post`

#### Sample Response

Status code: 400

```json

```

