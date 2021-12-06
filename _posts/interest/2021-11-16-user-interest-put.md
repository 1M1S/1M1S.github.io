---
title: "유저 관심분야 수준 변경 [PUT]"
date: 2021-11-15 22:21:00 +0900
categories: user-interest PUT
published: true

---

path로 전달된 유저의 관심분야 수준 변경

`PUT` `http://3.135.231.171/api/user/interest/{member_interest_id}`

### URI Parameter

| Name               | In    | Required | Type   | Description               |
| ------------------ | ----- | -------- | ------ | ------------------------- |
| member_interest_id | path  | true     | Long   | 수정할 유저의 관심분야 id |
| level              | query | true     | String | 유저의 수준으로 변경할 값 |

### Response

| Status code | Type           | Description          |
| ----------- | -------------- | -------------------- |
| 200 OK      | MemberInterest | 수정된 유저 관심분야 |



### 예제

#### Sample Request

`PUT` `http://3.135.231.171/api/user/interest/1040?level=junior`

#### Sample Response

Status code: 200

```json
{
    "id": 1040,
    "member":{
        "id": 1030,
        "username": "test",
        "password": "$2a$10$7JpJLI4KUV82mMcmNMY2A.rptegu4WxvgtjYsONETJQNrpSR8rZa6"
    },
    "interest":{
        "id": 1,
        "subject": "exercise"
    },
    "level": "junior"
}
```

