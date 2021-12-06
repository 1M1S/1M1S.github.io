---
title: "커리큘럼 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: curriculum GET
published: true
---

query로 전달된 수준, 관심분야에 해당하는 커리큘럼 목록 반환

`GET` `http://3.135.231.171/api/curriculum`

### URI Parameter

커리큘럼을 검색할 조건 전달.

두 값이 모두 전달되지 않으면 모든 커리큘럼 목록 반환

| Name        | In    | Required | Type    | Description |
| ----------- | ----- | -------- | ------- | ----------- |
| interest_id | query | false    | Long    | 관심분야 id |
| level       | query | false    | String | 수준        |

### Response

| Status code | Type                  | Description   |
| ----------- | --------------------- | ------------- |
| 200 OK      | Iterable\<Curriculum> | 커리큘럼 목록 |



### 예제 1

#### Sample Request

`GET` `http://3.135.231.171/api/curriculum`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1,
        "name": "sample_curriculum",
        "interest": {
            "id": 1,
            "subject": "workout"
        },
        "level": "beginner"
    },
    {
        "id": 2,
        "name": "beginner",
        "interest": {
            "id": 2,
            "subject": "job"
        },
        "level": "expert"
    }
]
```



### 예제 2

#### Sample Request

`GET` `http://3.135.231.171/api/curriculum?interest_id=2&level=3`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 2,
        "name": "beginner",
        "interest": {
            "id": 2,
            "subject": "job"
        },
        "level": "beginner"
    }
]
```

