---
title: "댓글 유저의 작성여부 반환 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user-comment
published: true

---

path로 전달받은 id의 유저와 댓글의 작성자를 비교해서 해당 유저가 댓글을 작성했는지 여부 체크

`GET` `http://3.135.231.171/api/user/comment/{comment_id}`

### URI Parameter

| Name       | In   | Required | Type | Description               |
| ---------- | ---- | -------- | ---- | ------------------------- |
| comment_id | path | true     | Long | 작성여부를 체크할 댓글 id |

### Response

| Status code | Type         | Description                       |
| ----------- | ------------ | --------------------------------- |
| 200 OK      | Boolean      | true. 해당 댓글은 유저가 작성함.  |
| 401         | UNAUTHORIZED | 해당 댓글은 유저가 작성하지 않음. |



### 예제

#### Sample Request

`GET` `http://3.135.231.171/api/user/comment/1043`

#### Sample Response

Status code: 200

```json
true
```

