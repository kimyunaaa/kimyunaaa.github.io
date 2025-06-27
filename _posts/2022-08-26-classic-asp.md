---
title: classic ASP
description: classic ASP
author: yuna
date: 2023-08-26 12:41:00 +0900
categories: [Study, ASP]
tags: [ASP]
pin: false
math: true
mermaid: true
---

### ASP.NET Core
# ASP.NET Core 소개

ASP.NET Core는 클라우드 기반 인터넷에 연결된 최신 응용 프로그램을 빌드하기 위한 플랫폼 간 고성능 오픈 소스 프레임워크입니다.  

ASP.NET Core를 사용하면 다음과 같은 작업을 수행할 수 있습니다.  
* 웹앱 및 서비스, IoT 앱 및 모바일 백 엔드를 빌드합니다.  
* Windows, macOS 및 Linux에서 즐겨 찾는 개발 도구를 사용합니다.  
* 클라우드 또는 온-프레미스에 배포합니다.  
* .NET Core 또는.NET Framework를 실행합니다.  

##### ASP.NET Core를 사용하는 이유는 무엇인가요?  
수백만 명의 개발자가 ASP.NET 4.x를 사용하여 웹앱을 만들었습니다(계속 사용 중).  
ASP.NET Core는 간결한 모듈식 프레임워크를 만드는 아키텍처 변경 내용을 포함한 ASP.NET 4.x의 새로운 디자인입니다.  

ASP.NET Core는 다음과 같은 이점을 제공합니다.  
>* 웹 UI 및 웹 API를 동일한 과정으로 빌드합니다.  
>* 최신 클라이언트 쪽 프레임워크 및 워크플로 개발을 통합합니다.  
>* 클라우드를 갖춘 환경 기반 구성 시스템입니다.  
>* 종속성 주입이 기본 제공됩니다.  
>* 간단한 고성능 모듈식 HTTP 요청 파이프라인을 포함합니다.  
>* IIS, Nginx, Apache, Docker에서 호스트하거나 고유한 프로세스에서 자체 호스트하는 기능이 있습니다.  
>* .NET Core를 대상으로 하는 경우 앱 버전을 함께 관리할 수 있습니다.  
>* 최신 웹 개발을 간소화하는 도구를 포함합니다.  
>* Windows, macOS 및 Linux에서 빌드하고 실행할 수 있습니다.  
>* 오픈 소스이며 커뮤니티에 중점을 둡니다.  

ASP.NET Core는 완전히 NuGet 패키지로 제공됩니다. NuGet 패키지를 사용하면 필요한 종속성만 포함하도록 앱을 최적화할 수 있습니다. 
실제로 .NET Core를 대상으로 하는 ASP.NET Core 2.x 앱에는 단일 NuGet 패키지만 필요합니다. 작은 앱 노출 영역의 혜택에는 보안 강화, 서비스 절감, 성능 향상이 포함됩니다.  

##### ASP.NET Core MVC를 사용하여 웹 API 및 웹 UI 빌드  
ASP.NET Core MVC에서는 Web API 및 웹앱을 빌드하는 기능을 제공합니다.  
MVC(모델-뷰-컨트롤러) 패턴을 통해 웹 API 및 웹앱을 테스트 가능하게 합니다.  
Razor 페이지 (2.0의 새로운 기능)는 웹 UI를 쉽게 빌드하고 생산성을 높일 수 있는 페이지 기반 프로그래밍 모델입니다.  
Razor 태그는 Razor 페이지 및 MVC 뷰에 생산적인 구문을 제공합니다.  
태그 도우미를 사용하면 서버 쪽 코드를 Razor 파일에서 HTML 요소를 만들고 렌더링하는 데 사용할 수 있습니다.  
여러 데이터 형식 및 콘텐츠 협상에 대한 기본 제공 지원을 통해 웹 API를 브라우저 및 모바일 장치를 포함한 다양한 클라이언트에 연결할 수 있습니다.  
모델 바인딩은 작업 메서드 매개 변수에 HTTP 요청의 데이터를 자동으로 매핑합니다.  
유효성 검사 모델은 자동으로 클라이언트와 서버 쪽 유효성 검사를 수행합니다.  
  
클라이언트 쪽 개발  
ASP.NET Core는 Angular, React, 부트스트랩 등 유명한 클라이언트 쪽 프레임워크 및 라이브러리와 원활하게 통합합니다. 자세한 내용은 클라이언트 쪽 개발을 참조하세요.  

##### ASP.NET Core 대상 .NET Framework  
ASP.NET Core는 .NET Core 또는 .NET Framework를 대상으로 지정할 수 있습니다.  
.NET Framework를 대상으로 지정한 ASP.NET Core 앱은 플랫폼 간 교차 사용이 불가능하며 —Windows에서만 실행됩니다.  
ASP.NET Core에서 .NET Framework를 대상으로 지정에 대한 지원은 제거되지 않을 예정입니다.  
일반적으로 ASP.NET Core는 .NET Standard 라이브러리로 구성됩니다.  
.NET Standard 2.0으로 작성된 앱은 .NET Standard 2.0이 지원되는 모든 위치에서 실행됩니다.  
.NET Core를 대상으로 지정하면 여러 이점이 있으며 이러한 장점은 릴리스마다 늘어나고 있습니다.  
.NET Framework에서 .NET Core의 몇 가지 장점은 다음과 같습니다.  
* 플랫폼 간 사용 가능. macOS, Linux 및 Windows에서 실행됩니다.  
* 향상된 성능  
* Side-by-side 버전 관리.  
* 새로운 API  
* 소스 열기  
.NET Framework에서 .NET Core 사이의 API 차이를 줄이기 위해 최선을 다하고 있습니다.  
Windows 호환 팩을 통해 수천 개의 Windows 전용 API를 .NET Core에서 사용할 수 있습니다. 이러한 API는 .NET Core 1.x에서 사용할 수 없습니다.  



### classic ASP 날짜 시간 계산
```
response.charset="utf-8"
'-------------------------------------------------
' 날짜 확인 테스트
'-------------------------------------------------
response.write "Now() ==> " & Now() & "<br>"
response.write "Date() ==> " & Date() & "<br>"
response.write "Time() ==> " & Time() & "<br>"

response.write "<hr>"

response.write mid(FormatDateTime(Now(), 2), 6,2)
response.write "<br />"
response.write right(FormatDateTime(Now(), 2), 2)
response.write "<br />"
response.write left("201809150923", 8)
response.write "<br />"


response.write CDate("2018-10-04 00:00:000")
response.write Month(FormatDateTime("2018-11-22", 2))&"-"&Day(FormatDateTime("2018-11-22", 2))
response.write "<br />"
response.write "FormatDateTime('2018-12-06 12:00:00', 0) ==> " & FormatDateTime("2018-12-06 12:00:00", 0) & "<br>"

response.write "<hr>"

response.write "Now() ==> " & Now() & "<br>"
response.write FormatDateTime("2018-12-06 13:57:00") & "<br>"
response.write (cdate("2018-12-06 13:57:00") < Now()) & "<br>"
 
response.write (cdate("2018-12-06 14:30:00") < Now()) & "<br>"

response.write "<hr>"

response.write "FormatDateTime(Now(), 0) ==> " & FormatDateTime(Now(), 0) & "<br>"
response.write "FormatDateTime(Now(), 1) ==> " & FormatDateTime(Now(), 1) & "<br>"
response.write "FormatDateTime(Now(), 2) ==> " & FormatDateTime(Now(), 2) & "<br>"
response.write "FormatDateTime(Now(), 3) ==> " & FormatDateTime(Now(), 3) & "<br>"
response.write "FormatDateTime(Now(), 4) ==> " & FormatDateTime(Now(), 4) & "<br>"
response.write "-----------------------" & "<br>"

response.write "FormatDateTime(Now(), 4) ==> " & FormatDateTime(Now(), 4) & "<br>"
response.write "Right(Now(), 3) ==> " & Right(Now(), 3) & "<br>"
 
response.write "====> " & FormatDateTime(Now(), 2) & " " & FormatDateTime(Now(), 4) & Right(Now(), 3) & "<br>"
```

시간계산 테스트
```
Dim mm 
'mm = 59-CInt(Minute(now()))
mm = 59-51

Dim timeNum
timeNum = 23 - CInt(hour(now())) & mm

if len(Cstr(mm)) < 2 then
  timeNum = 23 - CInt(hour(now())) & "0" & mm
end if 

response.write timeNum
```


결과
```
Now() ==> 2019-01-08 오후 5:26:16
Date() ==> 2019-01-08
Time() ==> 오후 5:26:16
_______________________________________________

01
08
20180915
2018-10-0411-22
FormatDateTime('2018-12-16 12:00:00', 0) ==> 2018-12-06 오후 12:00:00
_______________________________________________

Now() ==> 2019-01-08 오후 5:26:16
2018-12-06 오후 1:57:00
True
True
_______________________________________________

FormatDateTime(Now(), 0) ==> 2019-01-08 오후 5:26:16
FormatDateTime(Now(), 1) ==> 2019년 1월 8일 화요일
FormatDateTime(Now(), 2) ==> 2019-01-08
FormatDateTime(Now(), 3) ==> 오후 5:26:16
FormatDateTime(Now(), 4) ==> 17:26
------------------
FormatDateTime(Now(), 4) ==> 17:26
Right(Now(), 3) ==> :16
====> 2019-01-08 17:26:16
608
```
