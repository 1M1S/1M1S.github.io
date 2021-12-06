---
title: "시간관리 상담 설문조사 항목별 솔루션 가져오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: counsel GET
published: true
---

시간관리 상담 설문조사 항목에 따른 솔루션 목록들 리턴

`GET` `http://localhost:8080/api/counsel-solution/{counsel_survey_id}`

### URI Parameter

| Name              | In   | Required | Type | Description                    |
| ----------------- | ---- | -------- | ---- | ------------------------------ |
| counsel_survey_id | path | true     | Long | 시간관리 상담 설문조사 항목 id |

### Response

| Status code | Type            | Description                          |
| ----------- | --------------- | ------------------------------------ |
| 200 OK      | CounselSolution | 설문조사 항목에 해당하는 솔루션 리턴 |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/counsel-solution/1`

#### Sample Response

Status code: 200

```json
{
    "id": 1,
    "counselSurvey": {
        "id": 1,
        "problemNumber": 1,
        "question": "잘자는가?",
        "choices": "yes|no"
    },
    "solution": "잘자라"
}
```

