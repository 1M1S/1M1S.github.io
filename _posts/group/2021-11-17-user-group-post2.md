---
title: "그룹 가입 요청 [POST]"
date: 2021-11-15 22:21:00 +0900
categories: user-group POST
published: true
---

path로 전달된 유저가 그룹에 가입 요청

> authority 항목의 값이 "승인대기"인 PartyMember row 생성.
>
> 추후에 그룹장이 authority를 "일반멤버"로 수정해주면 그룹 가입 완료.

`POST` `http://3.135.231.171/api/user/{user_id}/group/{group_id}`

### URI Parameter

| Name     | In   | Required | Type | Description           |
| -------- | ---- | -------- | ---- | --------------------- |
| user_id  | path | true     | Long | 유저의 id             |
| group_id | path | true     | Long | 가입 요청할 그룹의 id |

### Response

| Status code | Type  | Description         |
| ----------- | ----- | ------------------- |
| 200 OK      | Party | 요청 보낸 그룹 리턴 |



### 예제

#### Sample Request

`POST` `http://3.135.231.171/api/user/1/group/4`

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

