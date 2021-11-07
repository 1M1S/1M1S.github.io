---
title: "일정 수정하기"
date: 2021-11-7 12:21:00 +0900
categories: tutorial
---
`DELETE` `http://localhost:8080/`

### Request
삭제할 일정 id
```json
{
	"id" : "1"
}
```

### Respond
삭제 요청 처리 여부 문자열로 반환
```string
6:00PM dinner Deleted
```
