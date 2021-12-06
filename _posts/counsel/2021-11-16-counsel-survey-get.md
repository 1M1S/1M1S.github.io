---
title: "시간관리 상담 설문조사 항목 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: counsel GET
published: true


---

problemNumber 기준으로 오름차순 정렬된 **시간관리 상담 설문조사 항목**들 목록 읽어오기.

`GET` `http://localhost:8080/api/counsel-survey`

### Response

| Status code | Type                     | Description          |
| ----------- | ------------------------ | -------------------- |
| 200 OK      | Iterable\<CounselSurvey> | 설문조사 항목들 목록 |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/counsel-survey`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1,
        "problemNumber": 1,
        "question": "질문1",
        "choices": "1|2|3|4|5"
    },
    {
        "id": 2,
        "problemNumber": 2,
        "question": "질문2",
        "choices": "1|2|3|4|5"
    }
]
```

