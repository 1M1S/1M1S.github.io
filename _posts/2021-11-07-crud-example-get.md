---
title: "[예제]모든 일정 가져오기"
date: 2021-11-7 12:21:00 +0900
categories: tutorial
---
시간 순서대로 정렬해서 모든 일정들을 반환한다.

`GET` `http://3.135.231.171/`

### Response

| Status code | Type                | Description |
| ----------- | ------------------- | ----------- |
| 200 OK      | Iterable\<TodoList> | 모든 일정들 |

### 예제

#### Sample Request

`GET` `http://3.135.231.171/`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 32,
        "time": "4:00PM",
        "content": "workout"
    },
    {
        "id": 33,
        "time": "6:00PM",
        "content": "dinner"
    },
    {
        "id": 34,
        "time": "6:00PM",
        "content": "dinner"
    }
]
```

