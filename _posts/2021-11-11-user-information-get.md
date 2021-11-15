---
Lotitle: "유저 개인정보 읽어오기"
date: 2021-11-11 21:09:00 +0900
categories: my_page
published: false
---

유저의 개인정보를 읽어온다.

`GET` `http://localhost:8080/api/user/{user_id}/information`

### URI Parameter

| Name    | In   | Required | Type | Description                 |
| ------- | ---- | -------- | ---- | --------------------------- |
| user_id | path | true     | Long | 개인정보를 읽어올 유저의 id |

### Response

| Status code | Type            | Description     |
| ----------- | --------------- | --------------- |
| 200 OK      | UserInformation | 유저의 개인정보 |

### 예제

#### Sample Request

`GET` `http://localhost:8080/api/user/2/information`

#### Sample Response

Status code: 200

```json
{
    "id" : 1,
    "name" : "Mr.Kim"
}
```

