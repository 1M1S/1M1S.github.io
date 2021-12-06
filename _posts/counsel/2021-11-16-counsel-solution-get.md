---
title: "시간관리 상담 설문조사 항목별 솔루션 가져오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: counsel GET
published: true
---

시간관리 상담 설문조사 항목에 따른 솔루션 목록들 리턴

`GET` `http://3.135.231.171/api/counsel-solution/{counsel_survey_id}`

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

`GET` `http://3.135.231.171/api/counsel-solution/1`

#### Sample Response

Status code: 200

```json
{
    "id": 1,
    "counselSurvey":{
        "id": 1,
        "problemNumber": 2,
        "question": "일일 계획을 세우는가?",
        "choices": "예|아니요"
    },
    "solution": "작은 일부터 시작하라.\\n큰 목표는 당신이 당신이 매일 하는 모든 작은 일이 목표에 점점 다가갈때 이루어진다. - Maren Kate\\n주변 정리부터 시작해보는것을 추천한다."
}
```

