---
title: "게시글 유저의 작성여부 반환 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user 게시글 GET
published: true

---

path로 전달받은 id의 유저와 게시글의 작성자를 비교해서 해당 유저가 게시글을 작성했는지 여부 체크

`GET` `http://localhost:8080/api/user/{user_id}/post/{post_id}`

### URI Parameter

| Name    | In   | Required | Type | Description                 |
| ------- | ---- | -------- | ---- | --------------------------- |
| user_id | path | true     | Long | 유저의 id                   |
| post_id | path | true     | Long | 작성여부를 체크할 게시글 id |

### Response

| Status code | Type    | Description            |
| ----------- | ------- | ---------------------- |
| 200 OK      | Boolean | 게시글 유저의 작성여부 |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/user/1/post/1033`

#### Sample Response

Status code: 200

```json
true
```
