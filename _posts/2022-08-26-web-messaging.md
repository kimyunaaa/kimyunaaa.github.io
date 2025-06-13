---
title: 웹 메세징
description: 웹 메세징
author: yuna
date: 2022-08-26 13:44:00 +0900
categories: [Study, WebMessage]
tags: [WebMessage]
pin: false
math: true
mermaid: true
---


웹 메세징  
한 페이지에 의해 활성화된 다른 웹 페이지 간의 비동기식 메시지 교환  
postMessage 메서드와, message 이벤트 핸들러를 사용하여 서로 다른 도메인 간 메시지 교환  

도큐먼트 간 메시지 교환(IE, FF, SF, OP, CR)  
```
window.postMessage(data, [ports], 메시지를 수신하는 도메인을 지정하는 문자열)  
```

message 이벤트 핸들러 등록  
- IE: window.attachEvent("onmessage", event_handler);  
- FF, SF, OP, CR: window.addEventListener("message", event_handler); 또는 window.onmessge = event_handler;  
 
message 이벤트에 의해 전달되는 MessageEvent 객체  
- data: 수신된 메시지 내용
- origin: 메시지 송신 측의 도메인
- source: 메시지 송신 측의 window 객체
- ports: 전달된 포트
- lastEventId: 마지막 이벤트 아이디

메시지 채널의 사용(SF, OP, CR)  
MessageChannel 객체로 다대다 메시지 교환 가능  

MessagePort 객체 속성  
- postMessage: 메시지 송신을처리하는 메서드
- start: 포트에 메시지가 도착할 경우 message 이벤트 활성화 시키는 메서드
- close: start 메서드에 의해 시작된 message 이벤트 비활성화
- onmessage: 포트에 메시지가 도착하면 message 이벤트 발생, message 이벤트 핸들러 설정을 위해 사용되는 속성
- addEventListener: 이벤트 핸들러 설정을 위해 사용되는 메서드
- removeEventListener: 이벤트 핸들러 설정을 제거하기 위해 사용되는 메서드

메시지 포트의 전달(SF, OP, CR)  
MessageChannel 객체의 MessagePort를 서로 다른 도메인에서 사용하려면 하나의 포트를 다른 쪽의 window 객체에 통지해야 한다.  

