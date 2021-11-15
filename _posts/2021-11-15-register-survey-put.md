---
title: "회원가입 설문조사 항목 수정 [PUT]"
date: 2021-11-15 22:21:00 +0900
categories: admin register-survey put
published: true
---

회원가입 설문조사 항목 수정.

`PUT` `http://localhost:8080/api/admin/register-survey/{register_survey_id}`

### URI Parameter

| Name               | In   | Required | Type | Description             |
| ------------------ | ---- | -------- | ---- | ----------------------- |
| register_survey_id | path | true     | long | 수정할 설문조사 항목 id |

### Request Body

DB `RegisterSurvey`

> 수정할 항목들만 전달하면 된다. 나머지는 null로 전달됨.

| Name          | Type          | Description                    |
| ------------- | ------------- | ------------------------------ |
| interest      | Interest (DB) | 관심분야 id                    |
| problemNumber | Integer       | 항목 번호                      |
| question      | String        | 질문                           |
| choices       | String        | 선택지 (`|`로 구분되어서 전달) |

### Response

| Status code | Type           | Description          |
| ----------- | -------------- | -------------------- |
| 200 OK      | RegisterSurvey | 수정된 설문조사 항목 |

### 예제

#### Sample Request

`PUT` `http://localhost:8080/api/admin/register-survey/1022`

Request Body

```json
{
    "interest" : {
        "id" : 3
    },
    "question" : "질문 2"
}
```

#### Sample Response

Status code: 200

```json
{
    "id": 1022,
    "interest":{
        "id": 3,
        "subject": null
    },
    "problemNumber": 3,
    "question": "질문 2",
    "choices": "1|2|3|4|5"
}
```

