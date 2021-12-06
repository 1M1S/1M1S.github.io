---
title: "유저 상담결과 삭제 [DELETE]"
date: 2021-11-15 22:21:00 +0900
categories: user-counsel-result DELETE
published: true


---

path로 전달된 유저의 상담 결과 삭제

`DELETE` `http://3.135.231.171/api/user/counsel-result/{member_counsel_result_id}`

### URI Parameter

| Name                     | In   | Required | Type | Description         |
| ------------------------ | ---- | -------- | ---- | ------------------- |
| member_counsel_result_id | path | true     | Long | 삭제할 상담 결과 id |

### Response

| Status code | Type                | Description           |
| ----------- | ------------------- | --------------------- |
| 200 OK      | MemberCounselResult | 삭제한 유저 상담 결과 |



### 예제

#### Sample Request

`DELETE` `http://3.135.231.171/api/user/1/counsel-result/16`

#### Sample Response

Status code: 200

```json
{
    "id": 16,
    "member":{
        "id": 3,
        "username": "test",
        "password": "$2a$10$ox4kqouwAtL1Bi7grOEXROfsZfEvr1qR160Cggn17ugdoPbNjLqvO"
    },
    "counselSolution": "{\n  \"result\" : \"휴식의 중요성 알기\"\n}",
    "counselTime": "2021-12-07T03:03:16.978364",
    "memberId": 3
}
```

