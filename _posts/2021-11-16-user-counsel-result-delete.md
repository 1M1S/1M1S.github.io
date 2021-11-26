---
title: "유저 상담결과 삭제 [DELETE]"
date: 2021-11-15 22:21:00 +0900
categories: user-counsel-result DELETE
published: true


---

path로 전달된 유저의 상담 결과 삭제

`DELETE` `http://localhost:8080/api/user/{user_id}/counsel-result/{member_counsel_result_id}`

### URI Parameter

| Name                     | In   | Required | Type | Description         |
| ------------------------ | ---- | -------- | ---- | ------------------- |
| user_id                  | path | true     | Long | 유저의 id           |
| member_counsel_result_id | path | true     | Long | 삭제할 상담 결과 id |

### Response

| Status code | Type                | Description           |
| ----------- | ------------------- | --------------------- |
| 200 OK      | MemberCounselResult | 삭제한 유저 상담 결과 |



### 예제

#### Sample Request

`DELETE` `http://localhost:8080/api/user/1/counsel-result/2`

#### Sample Response

Status code: 200

```json
{
    "id": 2,
    "member":{
        "id": 1,
        "username": "user1",
        "password": "1234"
    },
    "counselSolution": "{\n  \"result\" : \"솔루션1\n  솔루션2\n  솔루션3\"\n}",
    "counselTime": "2021-11-27T02:18:51.157082"
}
```

