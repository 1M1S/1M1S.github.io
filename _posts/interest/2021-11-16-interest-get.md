---
title: "관심분야 목록 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: interest GET
published: true



---

관심분야 목록 리턴

`GET` `http://localhost:8080/api/interest`

### Response

| Status code | Type                | Description   |
| ----------- | ------------------- | ------------- |
| 200 OK      | Iterable\<Interest> | 관심분야 목록 |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/interest`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1,
        "subject": "workout"
    },
    {
        "id": 2,
        "subject": "job"
    },
    {
        "id": 3,
        "subject": "programming"
    }
]
```

