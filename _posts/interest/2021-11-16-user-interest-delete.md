---
title: "유저 관심분야 삭제 [DELETE]"
date: 2021-11-15 22:21:00 +0900
categories: user-interest DELETE
published: true


---

path로 전달된 유저의 관심분야 삭제

`DELETE` `http://3.135.231.171/api/user/interest/{member_interest_id}`

### URI Parameter

| Name               | In   | Required | Type | Description               |
| ------------------ | ---- | -------- | ---- | ------------------------- |
| user_id            | path | true     | Long | 유저의 id                 |
| member_interest_id | path | true     | Long | 삭제할 유저의 관심분야 id |

### Response

| Status code | Type           | Description          |
| ----------- | -------------- | -------------------- |
| 200 OK      | MemberInterest | 삭제된 유저 관심분야 |
| 500         |                | 삭제 실패            |



### 예제

#### Sample Request

`DELETE` `http://3.135.231.171/api/user/interest/1040`

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

