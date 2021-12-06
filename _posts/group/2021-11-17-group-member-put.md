---
title: "그룹 멤버 권한수정 (그룹장) [PUT]"
date: 2021-11-15 22:21:00 +0900
categories: group-member PUT
published: true
---

유저가 그룹장일 경우 해당 그룹의 멤버들 권한 수정

`PUT` `http://3.135.231.171/api/user/{user_id}/group/{group_id}/member/{member_id}`

### URI Parameter

| Name      | In    | Required | Type   | Description  |
| --------- | ----- | -------- | ------ | ------------ |
| user_id   | path  | true     | Long   | 유저 id      |
| group_id  | path  | true     | Long   | 그룹 id      |
| member_id | path  | true     | Long   | 그룹 멤버 id |
| authority | query | true     | String | 설정할 권한  |

### Response

| Status code | Type        | Description             |
| ----------- | ----------- | ----------------------- |
| 200 OK      | PartyMember | 권한이 수정된 그룹 멤버 |
| 400         |             | 그룹장이 아닌 경우      |



### 예제 1

#### Sample Request

`PUT` `http://3.135.231.171/api/user/1/group/2/member/4?authority=일반회원`

#### Sample Response

Status code: 200

```json
{
    "id": 4,
    "party":{
        "id": 2,
        "name": "new group",
        "interest":{
            "id": 1,
            "subject": "workout"
        },
        "goal": "수정된 목표",
        "maximumNumberOfPeople": 10,
        "recruit": true
    },
    "member":{
        "id": 2,
        "username": "user2",
        "password": "2345"
    },
    "authority": "일반회원"
}
```

