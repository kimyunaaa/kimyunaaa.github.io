---
title: 웹 데이터베이스
description: 웹 데이터베이스
author: yuna
date: 2022-08-26 13:39:00 +0900
categories: [Study, WebDatabase]
tags: [WebDatabase]
pin: false
math: true
mermaid: true
---


#### 웹 스토리지
웹 브라우저의 로컬 디스크 저장 공간  
쿠키는 4KB 크기의 제한 있음  
localStorage,sessionStorage객체가 있다  

#### localStorage
웹 사이트 도메인 단위로 별도 운영  
저장된 데이터의 유효 시간이 없는 구조  

#### sessionStorage
로컬 디스크를 사용하여 데이터를 도메인 단위로 별도 저장  
웹 브라우저 종료시 데이터 소멸  
웹 브라우저와 동일한 생존 기간  

#### 웹 데이터베이스
웹 스토리지와 같이 로컬 저장 장치에 저장되고,  
HTML5의 자바스크립트 코드를 사용하여 데이터베이스를 생성, 데이터 CRUD 가능.  
'웹 SQL 데이터베이스', '인덱스드 데이터베이스'가 있다.  


웹 SQL 데이터베이스 생성(SF, CR, OP)  
openDatabase(사용할 데이터베이스 이름, version, 사용자를 위해 표시되는 이름, 데이터베이스 크기 바이트단위)
반환값  
- version: 현재 버전
- changeVersion: 버전 변경하는 메서드
- transaction(callback, error_callback, success_callback): 트랜잭션을 여는 메서드, executeSQL(sql, args, success_callback, error_callback) 메서드는 SQL 문장을 실행하기 위해 사용
- readTransaction: 읽기 전용의 트랜잭션을 여는 메서드

웹 SQL 데이터베이스 레코드 처리(SF, CR, OP)  
executeSQL(sql, args, success_callback, error_callback)  

웹 SQL 데이터베이스 버전 관리(SF, CR, OP)  
changeVersion(이전버전, 새로운버전, 버전 변경 시 처리할 콜백 함수, error_callback, success_callback)  

동기식 웹 SQL 데이터베이스 사용(SF, CR, OP)  
워커(Worker)를 사용, 사용자 인터페이스(UI)에 접근하지 못하는 자바스크립트 스레드(Thread)  
```
var worker = new Worker("test.js");
worker.postMessage("insert") // 워커에게 "insert" 메시지 전송
worker.onmessage = function(event) { // 워커로부터 메시지를 수신했을 경우 }
```

인덱스드 데이터베이스 사용(FF, CR)  
SQL 문장을 사용하지 않고 키와 값의 쌍으로 이루어진 구조로 대용량 자료 저장  
FF(파이어폭스): window.mozIndexedDB  
CR(크롬): window.webkitIndexedDB  

생성  
createObjectStore(name, optional)  
- name: 오브젝트 스토어의 이름
- optional: keyPath와 autoIncrement에 대해 기술

삭제  
deleteObjectStore(name)  

데이터 추가  
add({ key1: value1, key2: value2, key3: value3, ... })  

데이터 삭제  
delete(value)  

SQLite 데이터베이스  
별도의 환경 설정이 필요 없고, 서버가 없으며 파일로 처리하는 데이터베이스  