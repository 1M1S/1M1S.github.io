---
title: "그룹 멤버들 목록 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: group-member GET
published: true
---

유저가 그룹 멤버일 경우 그룹 멤버들 목록 반환

> authority 값이 "승인대기"일 경우 그룹 멤버 목록을 볼 수 없다.

`GET` `http://3.135.231.171/api/user/{user_id}/group/{group_id}/member`

### URI Parameter

| Name     | In   | Required | Type | Description |
| -------- | ---- | -------- | ---- | ----------- |
| user_id  | path | true     | Long | 유저 id     |
| group_id | path | true     | Long | 그룹 id     |

### Response

| Status code | Type                   | Description             |
| ----------- | ---------------------- | ----------------------- |
| 200 OK      | Iterable\<PartyMember> | 그룹 멤버들 목록        |
| 400         |                        | 그룹 구성원이 아닌 경우 |



### 예제 1

#### Sample Request

`GET` `http://3.135.231.171/api/user/1/group/2/member`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 3,
        "party": {
            "id": 2,
            "name": "new group",
            "interest": {
                "id": 1,
                "subject": "workout"
            },
            "goal": "수정된 목표",
            "maximumNumberOfPeople": 10,
            "recruit": true
        },
        "member": {
            "id": 1,
            "username": "user1",
            "password": "1234"
        },
        "authority": "그룹장"
    },
    {
        "id": 4,
        "party": {
            "id": 2,
            "name": "new group",
            "interest": {
                "id": 1,
                "subject": "workout"
            },
            "goal": "수정된 목표",
            "maximumNumberOfPeople": 10,
            "recruit": true
        },
        "member": {
            "id": 2,
            "username": "user2",
            "password": "2345"
        },
        "authority": "승인대기"
    },
    {
        "id": 5,
        "party": {
            "id": 2,
            "name": "new group",
            "interest": {
                "id": 1,
                "subject": "workout"
            },
            "goal": "수정된 목표",
            "maximumNumberOfPeople": 10,
            "recruit": true
        },
        "member": {
            "id": 3,
            "username": "user3",
            "password": "3456"
        },
        "authority": "일반회원"
    }
]
```



### 예제 2

#### Sample Request

`GET` `http://3.135.231.171/api/user/2/group/2/member`

#### Sample Response

Status code: 400

```json

```

