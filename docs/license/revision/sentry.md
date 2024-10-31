---
layout: default
title: Sentry
parent: 라이선스 변경 사례
grand_parent: 오픈소스 라이선스
nav_order: 4
---
# {{ page.title }}

## Sentry: BUSL1.1 라이선스 적용
### 변경사항
라이선스 변경사항은 아래와 같습니다.


{: .div_box}
Sentry의 라이선스가 Apache 2.0에서 <span>BUSL 1.1</span>{: .text-red-400} 라이선스로 변경되었습니다.<br>
[Sentry 10.0.0](https://github.com/getsentry/sentry/blob/10.0.0/LICENSE){:target="_blank" .line} 버전부터 <span>BUSL 1.1</span>{: .text-red-400} 라이선스가 적용됩니다.

### 주의사항

변경에 따른 주의사항은 아래와 같습니다.

- BUSL 1.1 라이선스는 일정 기간 동안 상용 목적으로의 사용이 제한되고, 일정 기간이 지나면 오픈소스 라이선스로 전환되는 라이선스입니다.
- 버전에 명시된 날짜 또는 버전이 배포된 지 만 3년(36개월)이 지났을 때 BUSL 1.1 라이선스에서 Apache 2.0 라이선스로 적용이 가능합니다.
  

### Business Source License 1.1 (BUSL 1.1)
- 일정 기간(명시된 날짜 혹은 36개월) 동안 상용 목적으로의 사용할 수 없는 제약을 가지고 있습니다.
- 단, 상용 목적이 아닌 경우에는 자유롭게 사용이 가능합니다.
- 해당 소프트웨어 버전에 명시된 날짜 또는 버전이 배포된 지 일정 기간이 지났을 때 BUSL 1.1 라이선스에서 Apache 2.0 라이선스로 적용할 수 있습니다.
- 라이선스 보유자(Licensor)가 일정 조건하에 상용 목적 사용자에게 권리를 부여할 수 있는 부가 조항(Additional Use Grant)이 있습니다.
  - Sentry의 경우 어플리케이션 모니터링 서비스를 상업적으로 제공하지 않는다면 예외 적용되어 사용 가능합니다.
  

>  **Sentry 라이선스 전환 예시**
>
>  23.7.0 버전: [Change Date: 2026-07-17, Change License: Apache License, Version 2.0](https://github.com/getsentry/sentry/blob/23.7.0/LICENSE#L19){:target="_blank"}


### 참고: [Sentry FAQ](https://forum.sentry.io/t/re-licensing-sentry-faq-discussion/8044){:target="_blank" .line} for Re-licensing

#### BUSL 1.1 라이선스로 변경된 리포지토리(Reposotiry)
아래의 경우들이 모두 BUSL 1.1 라이선스로 변경되었습니다.
{: .h5_box}
- [https://github.com/getsentry/sentry](https://github.com/getsentry/sentry){:target="_blank"}
- [https://github.com/getsentry/sentry-plugins](https://github.com/getsentry/sentry-plugins){:target="_blank"}
- [https://github.com/getsentry/sentry-docs](https://github.com/getsentry/sentry-docs){:target="_blank"}
- [https://github.com/getsentry/snuba/](https://github.com/getsentry/snuba/){:target="_blank"}
- [https://github.com/getsentry/semaphore](https://github.com/getsentry/semaphore){:target="_blank"}
- [https://github.com/getsentry/onpremise](https://github.com/getsentry/onpremise){:target="_blank"}
- [https://github.com/getsentry/docker-sentry](https://github.com/getsentry/docker-sentry){:target="_blank"}
- All Docker images produced by the repositories above


#### Sentry 코드를 얻고 재사용하기 위한 옵션 4가지
1. <a href="https://github.com/getsentry/sentry/tree/ca8674c533a0dffc48a177554479bb85fa05891b" target="_blank">SHA ca8674c533a0dffc48a177554479bb85fa05891b</a> 커밋 이전의 코드 버전을 사용합니다(BSD-3 라이선스가 적용되었습니다).
2. 코드를 사용할 프로젝트에 Sentry의 BUSL 1.1 라이선스를 적용합니다.
3. 재사용하려는 코드가 최종적으로 Apache 2.0 라이선스로 변환될 때까지 기다립니다(일반적으로 3년의 리드 타임).
4. Sentry에서 재사용 가능한 구성 요소를 오픈소스 저장소로 가져가려면 [oss@sentry.io](mailto:oss@sentry.io)로 문의합니다. 이것이 가능하지 않은 경우에도 상황에 따라 Sentry 팀에게 해당 코드에 대한 명시적 허가를 받을 수 있습니다.  
   

#### Apache 2.0 라이선스
- Sentry의 기본 라이선스입니다.
- GPL 2.0과 호환성 이슈가 없는 경우, 기본 라이선스로 채택합니다.
  


#### MIT 라이선스
- Apache 2.0 라이선스로 인해 GPL 2.0 등과 라이선스 충돌 문제가 있는 경우 사용합니다.
- Sentry에서 제공하는 모든 SDK에 적용되어 있습니다.
  
