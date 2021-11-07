---
title: "[예제]일정 수정"
date: 2021-11-7 12:21:00 +0900
categories: tutorial
---
`PUT` `http://localhost:8080/`

### Request
수정할 일정 id, 수정할 내용(time, content)
```json
{
	"id" : "1",
	"time" : "",
	"content" : "dinner"
}
```

### Respond
수정 요청 처리 여부 문자열로 반환
```
6:00PM dinner Edited
```
