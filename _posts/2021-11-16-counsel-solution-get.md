---
title: "시간관리 상담 설문조사 상담결과-솔루션 목록 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: counsel GET
published: true
---

시간관리 상담 결과에 따른 솔루션 목록들 리턴

> 상담결과를 어떻게 정할지는 아직 미정.
>
> 설문조사에 따라 시간관리 능력을 상, 중, 하로 분류?

`GET` `http://localhost:8080/api/counsel-solution`

### Response

| Status code | Type                       | Description      |
| ----------- | -------------------------- | ---------------- |
| 200 OK      | Iterable\<CounselSolution> | 솔루션 목록 리턴 |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/counsel-solution`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1,
        "result": "beginner",
        "solution": "계획세우기"
    },
    {
        "id": 2,
        "result": "junior",
        "solution": "실천하기"
    },
    {
        "id": 3,
        "result": "senior",
        "solution": "앞으로도 지금처럼"
    }
]
```

