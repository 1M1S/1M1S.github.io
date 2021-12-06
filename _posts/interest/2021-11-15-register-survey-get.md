---
title: "회원가입 설문조사 항목 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: register-survey GET
published: true

---

query로 전달된 관심분야에 해당되고, problemNumber 기준으로 오름차순 정렬된 **회원가입 설문조사 항목**들 목록 읽어오기.

`GET` `http://3.135.231.171/api/register-survey`

### URI Parameter

| Name        | In    | Required | Type | Description                   |
| ----------- | ----- | -------- | ---- | ----------------------------- |
| interest_id | query | true     | Long | 읽어올 설문조사의 관심분야 id |

### Response

| Status code | Type                      | Description                              |
| ----------- | ------------------------- | ---------------------------------------- |
| 200 OK      | Iterable\<RegisterSurvey> | 관심분야에 해당하는 설문조사 항목들 목록 |



### 예제

#### Sample Request

`GET` `http://3.135.231.171/api/register-survey?interest_id=1`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 0,
        "interest":{
            "id": 1,
            "subject": "exercise"
        },
        "problemNumber": 1,
        "question": "규칙적으로 운동하는가?",
        "choices": "아니다 | 보통이다 | 그렇다"
    },
    {
        "id": 1,
        "interest":{
            "id": 1,
            "subject": "exercise"
        },
        "problemNumber": 2,
        "question": "근력 운동을 일주일에 몇 번 하는가?",
        "choices": "안한다 | 1~3번 | 4회 이상"
    },
    {
        "id": 2,
        "interest":{
            "id": 1,
            "subject": "exercise"
        },
        "problemNumber": 3,
        "question": "유산소 운동을 일주일에 몇 번 하는가?",
        "choices": "안한다 | 1~3번 | 4회 이상"
    },
    {
        "id": 3,
        "interest":{
            "id": 1,
            "subject": "exercise"
        },
        "problemNumber": 4,
        "question": "평소 자신이 운동이 부족하다고 느끼는가?",
        "choices": "아니다 | 보통이다 | 그렇다"
    },
    {
        "id": 4,
        "interest":{
            "id": 1,
            "subject": "exercise"
        },
        "problemNumber": 5,
        "question": "체력적으로 힘든가?",
        "choices": "아니다 | 보통이다 | 그렇다"
    },
    {
        "id": 5,
        "interest":{
            "id": 1,
            "subject": "exercise"
        },
        "problemNumber": 6,
        "question": "자신에게 알맞은 운동방법을 알고 있는가?",
        "choices": "아니다 | 보통이다 | 그렇다"
    }
]
```

