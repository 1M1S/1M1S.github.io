---
title: "관심분야별 유저 랭킹 읽어오기 [GET]"
date: 2021-11-15 22:21:00 +0900
categories: user ranking get
published: true

---

query로 전달된 관심분야에서의 유저 순위 반환

> 동점자들의 경우 같은 순위로 처리되고 바로 다음 순위가 이어진다.
>
> ```
> 1, 2, 3, 3, 3, 4, ...
> ```

`GET` `http://localhost:8080/api/ranking`

### URI Parameter

| Name        | In    | Required | Type | Description |
| ----------- | ----- | -------- | ---- | ----------- |
| user_id     | query | true     | long | 유저의 id   |
| interest_id | query | true     | long | 관심분야 id |

### Response

| Status code | Type | Description              |
| ----------- | ---- | ------------------------ |
| 200 OK      | long | 관심분야에서 유저의 랭킹 |



### 예제

#### Sample Request

`GET` `http://localhost:8080/api/ranking?user_id=3&interest_id=1`

#### Sample Response

Status code: 200

```json
1
```
