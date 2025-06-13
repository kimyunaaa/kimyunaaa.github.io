---
description: 웹 워커
author: yuna
date: 2022-08-26 13:45:00 +0900
categories: [Study, WebWorker]
tags: [WebWorker]
pin: false
math: true
mermaid: true
---


웹 워커(Web Worker)  
자바스크립트를 이용하여 백그라운드로 처리되는 일종의 스레드  
```
var worker - new Worker("worker_prime.js");
worker.onmessage = function(evt) { ... }
```
- postMessage: 메시지를 워커에게 전송한다
- terminate: 워커를 강제로 종료한다
- onmessage: 워커가 보낸 메시지를 수신하는 이벤트 핸들러
- onerror: 에러 발생을 통지받기 위한 이벤트 핸들러
- close: 워커의 메시지 수신을 중지하는 메서드
- importScript: 지정한 주소의 자바스크립트 파일을 읽어 실행하는 메서드
- self: 워커 자신을 나타내는 변수
- location: 워커 생성 시 갖는 location에 관한 정보
- navigator: 워커 생성 시 갖는 location에 관한 정보
- setTimeout, setInterval, clearInterval: 타이머 관련 작업을 수행할 수 있는 메서드
- openDatabase, openDatabaseSync, indexedDB: 웹 데이터베이스를 처리하기 위한 객체
- XMLHttpRequest: Ajax를 처리하기 위한 객체
- Worker, SharedWorker: 워커 사용을 위한 객체
- WebSocket: 웹 소켓을 위한 객체
- applicationCache: 공용 워커의 소스 파일 이름이 menifest 파일에 수록되어 오프라인으로 처리될 경우의 applicationCache 객체이다.


전용 워커(dedicated worker)  
워커가 페이지별로 생성된다.  

공용 워커(shared worker)  
여러 창에대해 공용 워커의 이름만 같을 경우 하나만 생성되는 워커  
메시지 교환을 위해 MessagePort 객체가 같이 사용된다.  
공용으로 사용할 데이터를 한곳에 모아 처리하고 그 결과를 함께 공유할 경우 유용  