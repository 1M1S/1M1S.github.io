---
title: "시간관리 상담 설문조사 항목 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: counsel GET
published: true


---

problemNumber 기준으로 오름차순 정렬된 **시간관리 상담 설문조사 항목**들 목록 읽어오기.

`GET` `http://3.135.231.171/api/counsel-survey`

### Response

| Status code | Type                     | Description          |
| ----------- | ------------------------ | -------------------- |
| 200 OK      | Iterable\<CounselSurvey> | 설문조사 항목들 목록 |



### 예제

#### Sample Request

`GET` `http://3.135.231.171/api/counsel-survey`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 0,
        "problemNumber": 1,
        "question": "주/월 단위의 목표를 세우는가?",
        "choices": "예|아니요"
    },
    {
        "id": 1,
        "problemNumber": 2,
        "question": "일일 계획을 세우는가?",
        "choices": "예|아니요"
    },
    {
        "id": 2,
        "problemNumber": 3,
        "question": "일정들 간의 우선순위를 정하는가?",
        "choices": "예|아니요"
    },
    {
        "id": 3,
        "problemNumber": 4,
        "question": "계획을 잘 지키는가?",
        "choices": "예|아니요"
    },
    {
        "id": 4,
        "problemNumber": 5,
        "question": "시간관리의 중요성을 아는가?",
        "choices": "예|아니요"
    },
    {
        "id": 5,
        "problemNumber": 6,
        "question": "휴식(+숙면)의 중요성을 아는가?",
        "choices": "예|아니요"
    }
]
```

