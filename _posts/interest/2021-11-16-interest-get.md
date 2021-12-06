---
title: "관심분야 목록 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: interest GET
published: true



---

관심분야 목록 리턴

`GET` `http://3.135.231.171/api/interest`

### Response

| Status code | Type                | Description   |
| ----------- | ------------------- | ------------- |
| 200 OK      | Iterable\<Interest> | 관심분야 목록 |



### 예제

#### Sample Request

`GET` `http://3.135.231.171/api/interest`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 0,
        "subject": "general"
    },
    {
        "id": 1,
        "subject": "exercise"
    },
    {
        "id": 2,
        "subject": "programming"
    },
    {
        "id": 3,
        "subject": "employ"
    }
]
```

