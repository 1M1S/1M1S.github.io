---
title: "회원가입 설문조사 항목 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: admin register-survey get
published: true

---

query로 전달된 관심분야에 해당되고, problemNumber 기준으로 내림차순 정렬된 **회원가입 설문조사 항목**들 목록 읽어오기.

`GET` `http://localhost:8080/api/admin/register-survey`

### URI Parameter

| Name        | In    | Required | Type | Description                   |
| ----------- | ----- | -------- | ---- | ----------------------------- |
| interest_id | query | true     | long | 읽어올 설문조사의 관심분야 id |

### Response

| Status code | Type                      | Description                              |
| ----------- | ------------------------- | ---------------------------------------- |
| 200 OK      | Iterable\<RegisterSurvey> | 관심분야에 해당하는 설문조사 항목들 목록 |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/admin/register-survey/?interest_id=3`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1022,
        "interest":{
            "id": 3,
            "subject": "programming"
        },
        "problemNumber": 3,
        "question": "질문 2",
        "choices": "1|2|3|4|5"
    },
    {
        "id": 1023,
        "interest":{
            "id": 3,
            "subject": "programming"
        },
        "problemNumber": 4,
        "question": "질문",
        "choices": "1|2|3|4|5"
    }
]
```

