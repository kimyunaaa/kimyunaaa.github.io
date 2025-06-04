---
title: SSL 사설 인증서(Self Signed) 생성
description: SSL
author: yuna
date: 2022-08-26 18:09:00 +0900
categories: [Study, DevOps]
tags: [DevOps, SSL]
pin: false
math: true
mermaid: true
---

#### SSL 사설 인증서(Self Signed) 생성    
1. 개인 키 파일 생성

openssl genrsa -out server.key 2048

2. 인증서 서명 요청(Certificate signing request) 파일 생성

openssl req -new -key server.key -out server.csr

- Country Name: 국가 코드, 대문자로 KO 입력  
- State or Province Name: 주 또는 도  
- Locality Name: 도시  
- Organization Name: 회사명  
- Organizational Unit Name: 조직 이름  
- Common Name: Docker 레지스크리를 실행하는 서버 도메인. /etc/hosts 파일에 입력 한 내용  


3. 서버 인증서 파일 생성

openssl x509 -req -days 365 in server.csr -signkey server.key -out server.crt

4. server.crt 인증서 파일을 시스템에 설치
- 인증서 파일을 설치하지 않으려면 --insecure-registry 옵션 사용

> 우분투
sudo cp server.crt /usr/share/ca-certificates/
echo "server.crt" | sudo tee -a /etc/ca-certificates.conf
sudo update-ca-certificates

> CentOS
sudo cp server.crt /etc/pki/ca-trust/source/anchors
sudo update-ca-trust enable
sudo update-ca-trust extract

5. Docker 서비스 재시작  

