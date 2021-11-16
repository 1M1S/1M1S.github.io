---
title: "커리큘럼의 일정들 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: curriculum schedule get
published: true

---

커리큘럼에 포함되어 있는 일정 목록 반환

`GET` `http://localhost:8080/api/curriculum/{curriculum_id}/schedule`

### URI Parameter

| Name          | In    | Required | Type | Description |
| ------------- | ----- | -------- | ---- | ----------- |
| curriculum_id | query | true     | Long | 커리큘럼 id |

### Response

| Status code | Type                          | Description                        |
| ----------- | ----------------------------- | ---------------------------------- |
| 200 OK      | Iterable\<CurriculumSchedule> | 커리큘럼에 포함되어 있는 일정 목록 |

CurriculumSchedule

| Name          | Type   | Description                 |
| ------------- | ------ | --------------------------- |
| id            | Long   | PK(Primary Key)             |
| curriculum_id | Long   | 일정이 속해있는 커리큘럼 id |
| content       | String | 내용                        |
| interest_id   | Long   | 일정의 관심분야 id          |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/curriculum/1/schedule`

#### Sample Response

Status code: 200

```json
[
    {
        "id": 1,
        "curriculum": {
            "id": 1,
            "name": "sample_curriculum",
            "interest": {
                "id": 1,
                "subject": "workout"
            },
            "level": 7
        },
        "content": "running",
        "interest": {
            "id": 1,
            "subject": "workout"
        }
    },
    {
        "id": 2,
        "curriculum": {
            "id": 1,
            "name": "sample_curriculum",
            "interest": {
                "id": 1,
                "subject": "workout"
            },
            "level": 7
        },
        "content": "push-ups",
        "interest": {
            "id": 1,
            "subject": "workout"
        }
    }
]
```
