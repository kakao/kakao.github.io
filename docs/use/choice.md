---
layout: default
title: 오픈소스 선택
parent: 오픈소스 사용하기
nav_order: 1
---
# {{ page.title }}
선택할 수 있는 수많은 오픈소스 중에서, 프로젝트 요구 사항에 가장 적합한 오픈소스를 선택하는 것이 어려울 수 있습니다.<br>
이 가이드에서는 적절한 선택을 위한 기준들을 살펴보고 설명합니다.  
{: .summary }

## 오픈소스 선택 기준
아래의 기준에 따라 오픈소스를 선택하고 사용하면 좋은 선택을 할 수 있습니다.

- [기능 비교 분석]({{page.url}}#기능-비교-분석)
- [저장소 확인]({{page.url}}#저장소-확인)
- [라이선스 확인]({{page.url}}#라이선스-확인)
- [보안]({{page.url}}#보안)

아래의 목차는 각 기준에 대한 설명입니다.

### 기능 비교 분석

가장 적합한 오픈소스를 선택하기 위해, 각 오픈소스가 제공하는 기능을 분석하고 비교합니다.

* **프로젝트에서 필요한 기능 충족**
  - 기본 기능이 적합하게 제공되는가?
  - 필요한 기능만을 제공하는가?
  - 특정 팀에서 사용하기에 어렵지는 않은가
  - 적절한 레퍼런스가 있는가?
  - 사용 시 수정이 필요하다면 수정이 가능한가?
* **프로젝트와의 호환성 및 확장성**
  - 언어
  - 운영체제
* **성능 확인 및 기능 테스트**


### 저장소 확인
선택할 오픈소스 저장소의 품질을 확인합니다.

* **가이드 문서**
  - README 파일 
  - 사용자를 위한 가이드 문서
* **저장소 정보 확인**
  - 스타(Star) 수
  - 참조 횟수
  - 오픈된 이슈 수
  - 오픈된 PR 수
  - 마지막 커밋일시
  - 릴리스 주기
* **소스 코드 품질**
* **범용성 및 레퍼런스**


### 라이선스 확인
선택할 오픈소스의 라이선스를 확인합니다. 오픈소스에 따라 방법이 상이할 수 있습니다.

* **GitHub 저장소가 있는 경우**: [예: Alamofire github](https://github.com/Alamofire/Alamofire){:target="_blank"}
  - README 문서
  - 소스 코드 내 COPYING 문서, LICENSE 문서
  - 소스 코드 내 주석
* **별도의 홈페이지가 있는 경우**: [예: Tomcat 홈페이지](https://tomcat.apache.org/){:target="_blank"}
  - LICENSE 메뉴
  - 소프트웨어 설명 내 표기
  - 소스 코드 내 COPYING 문서, README 문서
  - 소스 코드 내 주석
* **검색으로 찾은 소스 코드인 경우**
  - 소스 코드 내 주석
  - 개발자의 답변


### 보안

선택할 오픈소스의 보안 관련 정보를 확인합니다.

* **보안 관련 이슈 확인**
* **취약점 발생 시 대응 조치**
* **이슈에서 보안 문제 있는지 확인**
* **릴리스 노트 확인**
* **[CVE](https://cve.mitre.org/index.html){:target="_blank"} 확인**
  - CVE가 제공하는 알려진 오픈소스 보안 취약점을 확인합니다.
  - 사용하려는 오픈소스를 CVE에서 검색하여, 보안 취약점이 있는지 확인합니다.
* **GitHub**
  - [Dependabot](https://docs.github.com/en/github/managing-security-vulnerabilities/about-alerts-for-vulnerable-dependencies#dependabot-alerts-for-vulnerable-dependencies){:target="_blank"}을 사용해, 오픈소스 리포지토리의 의존성(종속성) 취약점들을 감지하고 경고를 받을 수 있습니다.

----

## 오픈소스 선택 시 도움말
아래는 오픈소스를 선택할 때 도움이 될만한 내용입니다.

### awesome 검색
아래와 같이 **awesome**을 오픈소스 이름과 함께 검색하면 좋은 오픈소스를 찾아볼 수 있습니다.

```
awesome + { keyword }
```

>  **참고하기**
>
> * [awesome android-ui](https://www.google.com/search?q=awesome+android-ui&oq=awesome+android-ui){:target="_blank" .fs-3}



### 잘 만들어진 애플리케이션에서 사용 중인 오픈소스 확인
애플리케이션의 고지문에서 사용한 오픈소스를 확인할 수 있습니다.잘 만들어진 여러 애플리케이션들이 사용하고 있는 오픈소스를 선택하는 것도 한 방법입니다.
