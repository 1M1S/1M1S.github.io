---
title: "모든 일정 가져오기"
date: 2021-11-7 12:21:00 +0900
categories: tutorial
---
`GET` `http://localhost:8080/`

### Request
없음

### Respond
모든 일정
```json
[
    {
        "id": 1,
        "time": "3:00PM",
        "content": "workout"
    },
    {
        "id": 2,
        "time": "7:00PM",
        "content": "dinner"
    }
]
```
