---
title: "댓글 유저의 작성여부 반환 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user 댓글 GET
published: true

---

path로 전달받은 id의 유저와 댓글의 작성자를 비교해서 해당 유저가 댓글을 작성했는지 여부 체크

`GET` `http://localhost:8080/api/user/{user_id}/comment/{comment_id}`

### URI Parameter

| Name       | In   | Required | Type | Description               |
| ---------- | ---- | -------- | ---- | ------------------------- |
| user_id    | path | true     | Long | 유저의 id                 |
| comment_id | path | true     | Long | 작성여부를 체크할 댓글 id |

### Response

| Status code | Type    | Description          |
| ----------- | ------- | -------------------- |
| 200 OK      | Boolean | 댓글 유저의 작성여부 |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/user/1/comment/1035`

#### Sample Response

Status code: 200

```json
true
```

