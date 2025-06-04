---
title: Docker 컴파일
description: Docker 컴파일
author: yuna
date: 2022-08-26 18:11:00 +0900
categories: [Study, DevOps]
tags: [Docker, DevOps, Docker Compile]
pin: false
math: true
mermaid: true
---

###### Docker 컴파일
make 설치  
우분투> sudo apt-get install make  
centOS> sudo yum install make  

소스 받기  
> git clone ...  

docker 디렉토리로 이동한 뒤 make 명령 실행  
> sudo make build  
Docker 컴파일을 위한 docker:master 이미지가 생성된다.(Git 브랜치를 전환하지 않고 master 그대로일때)  
> sudo make binary
컴파일이 끝나면 Docker 소스 디렉터리 아래에 bundles 디렉터리가 생성된다  
해당 디렉터리 아래 Docker 실행 파일이 있음  
파일명은 docker-<버전> 형식  

해당 파일로 시스템에 설치된 Docker 실행 파일을 교체 가능  
> sudo service docker stop  
> cp 바이너리생성폴더 $(type -P docker)  
> sudo service docker start  