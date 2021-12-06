---
title: "그룹 탈퇴 및 삭제(그룹장) [DELETE]"
date: 2021-11-15 22:21:00 +0900
categories: user-group DELETE
published: true
---

유저가 그룹장일 경우, 해당 그룹 삭제

그룹장이 아닐 경우, 해당 그룹 탈퇴

> 그룹 가입 취소를 할때에도 해당 그룹을 탈퇴하면 된다.

`DELETE` `http://localhost:8080/api/user/{user_id}/group/{group_id}`

### URI Parameter

| Name     | In   | Required | Type | Description           |
| -------- | ---- | -------- | ---- | --------------------- |
| user_id  | path | true     | Long | 유저의 id             |
| group_id | path | true     | Long | 탈퇴/삭제할 그룹의 id |

### Response

| Status code | Type  | Description      |
| ----------- | ----- | ---------------- |
| 200 OK      | Party | 삭제/탈퇴한 그룹 |



### 예제

#### Sample Request

`DELETE` `http://localhost:8080/api/user/1/group/4`

#### Sample Response

Status code: 200

```json
{
    "id": 4,
    "name": "new group 2",
    "interest":{
        "id": 1,
        "subject": "workout"
    },
    "goal": "목표",
    "maximumNumberOfPeople": 10,
    "recruit": true
}
```

