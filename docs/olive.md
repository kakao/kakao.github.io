---
layout: default
title: <img src="https://t1.kakaocdn.net/olive/ossguide/logo_olive.png" width="16" style="vertical-align:middle; margin-bottom:2px"> OLIVE Platform
nav_order: 7

---
# OLIVE Platform
<div class="summary">
<a href="https://olive.kakao.com/intro" target="_blank" class="line fw-700">OLIVE Platform</a>은 프로젝트를 실시간으로 스캔하고 프로젝트에 사용된 오픈소스와 라이선스를 확인하여,<br>
오픈소스 라이선스 의무 사항을 준수할 수 있도록 지원하는 오픈소스 관리 서비스입니다.
</div>


![img.png](https://t1.kakaocdn.net/olive/ossguide/oliveplatform.png)
{: .olive_bg .mb-8}

## OLIVE Platform 탄생 배경
카카오는 2014년 11월, 오픈소스를 올바르게 사용하고 관리하기 위해  **오픈소스 관리 조직을 신설**했습니다.<br>
오픈소스 라이선스 검증은 카카오톡 애플리케이션을 시작으로, 현재는 배포되는 모든 서비스와 SDK 및 오픈소스를 대상으로 검증이 진행되고 있습니다.

### OLIVE, 그 첫 시작 Hermes
카카오는 **새로운 연결, 더 나은 세상**이라는 슬로건에 맞춰 다양한 서비스를 제공하고 있습니다.<br>
따라서 다양한 서비스에서 **사용한 오픈소스를 확인하고 관리**할 수 있는 자동화된 도구가 필요했었는데요, 코드 레벨의 분석 솔루션 도입을 시작으로, 오픈소스 관리 도구인 **Hermes**를 개발하여 Android와 iOS 애플리케이션 대응부터 검증 과정을 자동화하기 시작했습니다.<br>


### OLIVE, Next level 오픈소스 검증 도구의 필요성
시간이 흐르며, 점차 증가하는 다양한 서비스의 개발 환경, 언어 및 플랫폼에 대응하게 되었습니다. <br>
특히 카카오 미니 출시 당시, 오픈소스 검증 범위가 운영체제(OS) 레벨까지 확장되었습니다. 동시에, 사내 오픈소스 정책을 수립하고 개발자를 대상으로 오픈소스 교육을 진행하며, 오픈소스 사용에 대한 인식을 점차 개선해 나갔습니다.<br>


정책 수립과 교육, 검증 자동화 및 효율화를 통해 오픈소스 검증 시간은 단축되고 검증 품질은 향상되었습니다. 그러나 검증 작업을 오픈소스 관리 조직에서 전담하며 한정된 리소스로 인해, 오픈소스 관리 조직에서 모든 서비스의 요청을 대응하기가 어려워졌습니다.<br>

무엇보다 각 서비스는 오픈소스 관리 조직에서 검증을 완료한 후에야 비로소 관련 이슈를 확인하고 대응할 수 있었습니다. 이로 인해, 단순 자동화 이상의 새로운 오픈소스 검증 전략이 필요한 상황이 발생했습니다.<br>

이에 카카오는 **개발자가 주도적으로 오픈소스 관리 시스템에 참여**할 수 있는 시스템을 목표로, 검증 시스템을 확장했습니다.<br>

이렇게 탄생한 OLIVE의 도입으로 서비스 개발자는 언제든 오픈소스 검증을 진행하고, 사용한 오픈소스를 리포트로 확인하며 즉시 대응할 수 있게 되었습니다.<br>


아울러 서비스 개발이 완료되면 배포 전에 검증을 수행하고, 오픈소스 관리자에게 검증 리뷰를 요청하는 프로세스를 구축했습니다. 이와 같이 필수적인 검증 결과의 최종 확인 절차는 **오픈소스 관리 조직**에서 전담하도록 하여, 전체 검증 프로세스의 효율이 크게 증가할 수 있었습니다.


### OLIVE Platform 탄생
OLIVE Platform은 카카오 서비스에서 사용하는 오픈소스를 올바르게 사용하고 관리하기 위해 개발된 OLIVE를 모두가 사용할 수 있도록 공개한 오픈소스 관리 서비스입니다.<br>
신뢰할 수 있는 오픈소스 DB를 구축해 보다 쉽고, 빠르고, 정확하게 오픈소스를 검증할 수 있도록 지속적인 기능 추가 및 개선 작업을 진행하고 있습니다.<br>
우리가 오랜 시간 고민 끝에 만든 이 서비스가 모든 개발자들의 오픈소스에 대한 이해를 높이고 서비스의 오픈소스 관리에 도움이 되기를 바랍니다.<br>


----

## OLIVE Platform 사용 시 기대효과
OLIVE Platform을 도입하면, 아래 효과를 기대할 수 있습니다.
- 서비스 개발자의 오픈소스 라이선스에 대한 이해도 상승
- 개발문화 개선 
- 개발한 소프트웨어의 보안 문제점을 빠르게 파악하고 대처 가능 
- 개발한 소프트웨어의 라이선스 의무 수행 
- 개발한 소프트웨어의 취약점 발견

----

## [OLIVE Platform](https://olive.kakao.com){:target="_blank"} 기능

###  **프로젝트 분석** <img src="https://t1.kakaocdn.net/olive/ossguide/img-analyze.png" class="ic_image_vertical" alt="" />
- GitHub 계정을 연동하거나 CLI로 프로젝트를 분석하여, 사용 중인 의존성 정보와 코드스니펫 정보를 확인할 수 있습니다.<br>
- 다른 사람을 프로젝트의 멤버 초대하고 공유하여, 프로젝트를 함께 관리할 수 있습니다.


### **매핑** <img src="https://t1.kakaocdn.net/olive/ossguide/img-mapping.png" class="ic_image_vertical" alt="" />
- 분석된 의존성과 코드스니펫에 매핑된 오픈소스 컴포넌트를 확인하고, 매핑되지 않은 의존성을 직접 매핑할 수 있습니다.
- 직접 매핑한 오픈소스는 오픈소스 데이터베이스(Database, DB)에 추가하여 추후 자신의 프로젝트의 자동분석에 재활용할 수 있습니다.


###  **라이선스 검증** <img src="https://t1.kakaocdn.net/olive/ossguide/img-verify.png" class="ic_image_vertical" alt="" />
- 프로젝트에서 사용한 오픈소스 컴포넌트의 라이선스와 의무 사항을 확인할 수 있습니다.
- 라이선스 관련 이슈가 발견되었을 경우, 그 해결 방법을 함께 가이드하고 있습니다.


###  **리포트 생성** <img src="https://t1.kakaocdn.net/olive/ossguide/img-report.png" class="ic_image_vertical" alt="" />
- 스캔이 완료되면 체크리스트와 리포트가 자동으로 생성됩니다.
- 이전 스캔 시점의 검증 결과와 현재를 비교할 수 있고, 검증이 진행되는 중에도 오픈소스 고지문을 미리 확인할 수 있습니다.
- 검증이 완료되면 고지문(참고용)을 다운로드할 수 있습니다.

----

## OLIVE Platform 기능 참고
- 웹 서비스: [https://olive.kakao.com/](https://olive.kakao.com/){:target="_blank"}
- CLI 서비스: [https://olive.kakao.com/docs/cli/v2/overview](https://olive.kakao.com/docs/cli/overview){:target="_blank"}
- 체험하기: [https://olive.kakao.com/simple-check/analysis](https://olive.kakao.com/simple-check/analysis){:target="_blank"}
- 사용자 문서: [https://olive.kakao.com/docs/](https://olive.kakao.com/docs/){:target="_blank"}

----

## OLIVE Platform 히스토리
- 2020.11.18: OLIVE Platform(Beta) 서비스 오픈
- 2021.06.30: OLIVE Platform 정식 서비스 오픈
- 2022.03.24: 프로젝트 추가 시 파일 업로드 지원
- 2022.04.21: OLIVE Platform CLI 오픈
- 2022.11.14: 소셜 로그인 지원
- 2022.11.23: 코드스니펫 분석 기능 추가
- 2023.09.11: OLIVE CLI v2.0.0 출시
- 2023.11.07: ESG 가입 오픈
- 2023.11.27: OLIVE Platform 서비스 개편 (오픈소스 데이터 추가,  취약성 정보 추가)

