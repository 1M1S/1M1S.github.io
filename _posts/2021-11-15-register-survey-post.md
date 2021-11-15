---
title: "회원가입 설문조사 항목 추가 [POST]"
date: 2021-11-15 22:21:00 +0900
categories: admin register-survey post
published: true


---

회원가입 설문조사 항목 추가.

`POST` `http://localhost:8080/api/admin/register-survey`

### Request Body

DB RegisterSurvey

| Name          | Type          | Description                    |
| ------------- | ------------- | ------------------------------ |
| interest      | Interest (DB) | 관심분야 id                    |
| problemNumber | Integer       | 항목 번호                      |
| question      | String        | 질문                           |
| choices       | String        | 선택지 (`|`로 구분되어서 전달) |

### Response

| Status code | Type           | Description          |
| ----------- | -------------- | -------------------- |
| 200 OK      | RegisterSurvey | 생성된 설문조사 항목 |

### 예제

#### Sample Request

`POST` `http://localhost:8080/api/admin/register-survey`

Request Body

```json
{
    "interest" : {
        "id" : 1
    },
    "problemNumber": 3,
    "question" : "질문",
    "choices" : "1|2|3|4|5"
}
```

#### Sample Response

Status code: 200

```json
{
    "id" : 1022,
    "interest" : {
        "id" : 1,
        "subject" : null
    },
    "problemNumber" : 3,
    "question" : "질문",
    "choices" : "1|2|3|4|5"
}
```

