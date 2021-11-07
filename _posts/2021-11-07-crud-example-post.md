---
title: "일정 생성"
date: 2021-11-7 12:21:00 +0900
categories: tutorial
---
`POST` `http://localhost:8080/add`

### Request
추가할 일정 전달
```json
{
	"time" : "6:00PM",
	"content" : "dinner"
}
```

### Response
추가 요청 처리 여부 문자열로 반환
```string
6:00PM dinner Saved
```
