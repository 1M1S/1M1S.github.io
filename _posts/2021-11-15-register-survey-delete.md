---
title: "회원가입 설문조사 항목 삭제 [DELETE]"
date: 2021-11-15 22:21:00 +0900
categories: admin register-survey delete
published: false
---

회원가입 설문조사 항목 삭제.

`DELETE` `http://localhost:8080/api/admin/register-survey/{register_survey_id}`

### URI Parameter

| Name               | In   | Required | Type | Description             |
| ------------------ | ---- | -------- | ---- | ----------------------- |
| register_survey_id | path | true     | long | 삭제할 설문조사 항목 id |

### Response

| Status code | Type           | Description          |
| ----------- | -------------- | -------------------- |
| 200 OK      | RegisterSurvey | 삭제된 설문조사 항목 |



### 예제

#### Sample Request

`DELETE` `http://localhost:8080/api/admin/register-survey/1022`

#### Sample Response

Status code: 200

```json
{
    "id": 1022,
    "interest":{
        "id": 3,
        "subject": "programming"
    },
    "problemNumber": 3,
    "question": "질문 2",
    "choices": "1|2|3|4|5"
}
```

