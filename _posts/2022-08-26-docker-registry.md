---
title: Docker Registry
description: Docker
author: yuna
date: 2022-08-26 18:39:00 +0900
categories: [Study, DevOps]
tags: [Docker, DevOps, DockerRegistry]
pin: false
math: true
mermaid: true
---

###### Docker Registry 
도커 이미지를 공유하기 위한 서버 애플리케이션  


###### Remote Repository 원격 저장소  
Docker Registry를 이용하여 원격 저장소에 이미지를 업로드 할 수 있다.  


###### 레지스트리 서버 사용
5000번 포트로 레지스트리 서버 사용
```
sudo docker run -d -p 5000:5000 --name example-registry -v /tmp/registry:/tmp/registry registry
```

