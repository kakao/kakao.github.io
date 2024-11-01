---
layout: default
title: 라이선스 변경 사례
parent: 오픈소스 라이선스
nav_order: 4
---
# {{ page.title }}

<div class="summary">
잘 알려진 유명 오픈소스의 라이선스 변경 사례는 MongoDB, Sentry 및 ElasticSearch가 있습니다.<br>
특히, 이러한 종류의 라이선스 변경은 <strong>클라우드 서비스에 대한 제약사항</strong>을 추가하거나, <strong>상용 목적의 사용이 제한</strong>되는 라이선스로 변경되는 경우가 있으니 주의해야 합니다.<br>
이 가이드에서는 유명한 라이선스 변경 및 제한사항이 추가된 사례를 소개하고, 사용 시 주의사항을 알아봅니다.
</div>

## Grafana, Loki, Tempo: AGPL 3.0 라이선스 적용
### 변경사항
라이선스 변경사항은 아래와 같습니다.
{: .h3_box}

{: .new .h3_box}
Grafana, Loki, Tempo의 라이선스가 Apache 2.0에서 <span>AGPL 3.0</span>{: .text-red-200 }으로 변경되었습니다.<br>
Grafana <a href="https://github.com/grafana/grafana/tree/v7.5.6" target="_blank" class="line">v7.5.6</a>, Loki <a href="https://github.com/grafana/loki/tree/v2.3.0" target="_blank" class="line">v2.3.0</a>, <a href="https://github.com/grafana/tempo/releases/tag/v0.7.0" target="_blank" class="line">Tempo v0.7.0</a> 부터 <span class="text-red-300"> AGPL 3.0</span> 라이선스가 적용됩니다.<br>
기타 플러그인(Plugin), 에이전트(Agent), 일부 라이브러리들은 Apache 2.0 라이선스를 그대로 유지합니다.<br>

### 주의 사항
변경에 따른 주의사항은 아래와 같습니다.
{: .h3_box}
- AGPL 3.0 라이선스는 **GPL 3.0 라이선스에 네트워크 사용 관련 의무사항이 추가**된 라이선스입니다. 
- AGPL이 적용된 서비스가 네트워크(예: REST API)를 통해 클라이언트(예: 브라우저)에게 기능을 제공하는 경우에, 기능을 사용하는 모든 사용자에게 AGPL 서비스를 포함한 전체 소스를 공개하는 의무사항이 발생합니다.
- 위 의무사항은 **웹 서비스의 경우도 해당**합니다.
- 예를 들어, AGPL이 적용된 Grafana 서비스를 제 3자에게 클라이언트(브라우저) 등에서 사용할 수 있도록 제공하는 경우, Grafana 서비스의 전체 소스를 공개해야 합니다.
{: .h3_box}

## mongoDB: SSPL 라이선스 적용
### 변경사항

{: .new .h3_box}
[mongoDB](https://github.com/mongodb/mongo){:target="_blank" .line}의 라이선스가 AGPL에서 <span>SSPL</span>{: .text-red-200 }로 변경되었습니다.<br>
2018년 10월 16일 이후의 릴리스(Release)에 대해 <span>SSPL</span>{: .text-red-200 }이 적용됩니다(이전 버전의 패치도 포함합니다).<br>

### 주의사항

변경에 따른 주의사항은 아래와 같습니다.
{: .h3_box}

- 외부에 서비스로 제공하는 경우 서비스 소스코드(Service Source Code)를 전체 공개해야 합니다. 
- SaaS, 클라우드 등 제 3자에게 제공되는 모든 서비스를 포함합니다.

{: .h3_box}

>  **서비스 소스코드(Service Source Code)란?**
>
>  본 프로그램 또는 수정된 버전의, 서비스를 구성하는 모든 프로그램의 소스코드 및 관리 소프트웨어 전체를 의미합니다.
>  애플리케이션 프로그램의 인터페이스, 자동화 소프트웨어, 모니터링 소프트웨어, 백업 소프트웨어, 스토리지 소프트웨어 및 호스팅 소프트웨어 등 사용자가 실행할 수 있는 모든 서비스의 인스턴스가 해당합니다.
{: .h3_box} 

### SSPL 라이선스로 변경

2018년 10월 16일 이전 버전은 AGPL 라이선스이며, 그 이후 릴리스는 SSPL로 변경되었습니다(이전 버전의 패치도 포함합니다).
{: .h3_box}

<div class="new h3_box">
<strong class="fs-3">라이선스 변경 관련 원문</strong><br><br>
<code class="fs-2">MongoDB is free and open-source. Versions released prior to October 16,2018 are published under the AGPL.<br>
All versions released after October 16, 2018, including patch fixes for prior versions, are published under the Server Side Public License (SSPL) v1.<br>See individual files fordetails.</code>
</div>

SSPL 라이선스로 변경한 자세한 이유는 [MongoDB now released under the Server Side Public License](https://www.mongodb.com/blog/post/mongodb-now-released-under-the-server-side-public-license){:target="_blank" .line} 에서 확인할 수 있습니다.
{: .h3_box}
간략하게는 아래의 이유로 라이선스를 변경하였습니다.
{: .h3_box}
- AWS와 같은 클라우드 서비스 제공자가 오픈소스를 사용하여 플러그 앤드 플레이(Plug and Play) 형태로 제공하며 수익을 창출하게 됨에 따라, 이를 방지하고자 SSPL 또는 상용 라이선스로 변경하였습니다.
- SSPL 라이선스는 13조에서 해당 라이선스를 사용하는 프로젝트를 서비스로 제공하는 경우 **서비스 소스코드**를 제공하라는 조항을 추가하고, **서비스 소스코드**를 새롭게 정의하였습니다. 
- SSPL 라이선스는 오픈소스 OSI(Open Source Initiative)에서 승인이 되지 않은 라이선스입니다.
{: .h3_box}


## ElasticSearch: Elastic License 2.0, SSPL 듀얼 라이선스 적용
### 변경사항

{: .new .h3_box}
오픈소스 버전 ElasticSearch 및 Kibana의 [ElasticSearch의 라이선스](https://www.elastic.co/kr/subscriptions){:target="_blank" .line}가 Apache 2.0에서 <span>Elastic License 2.0, SSPL의 듀얼 라이선스</span>{: .text-red-200 }로 변경되었습니다.<br>
7.11 버전의 ElasticSearch와 Kibana부터 <span>Elastic License 2.0, SSPL의 듀얼 라이선스</span>{: .text-red-200 }가 적용됩니다.  <br>

> **라이선스 설명**
>
> - **Elastic License 2.0:** 클라우드 서비스 공급자가 Elasticsearch 및 Kibana를 서비스로 제공하지 못하도록 제한합니다.
> - **SSPL:** 외부에 서비스로 제공하는 경우 **서비스 소스코드(Service Source Code)** 전체 공개의 의무가 있습니다.
{: .h3_box .fs-3}

### 주의사항

변경에 따른 주의사항은 아래와 같습니다.
{: .h3_box}
- 베이식(Basic) 라이선스는 자체 서비스 등을 위해 직접 구축할 경우, 계속 무료로 사용할 수 있으며, 상업적으로 제품에 포함시키는 등의 재판매는 금지합니다.
- 오픈소스 버전의 경우 기본적으로 SSPL(Server Side Public License) 1.0과 Elastic License 2.0의 듀얼 라이선스가 적용되며, 각 파일 헤더에 명시된 라이선스가 우선 적용됩니다.
- x-pack 디렉터리 하위는 Elastic License가 적용되므로, 베이식(Basic) 이상에 포함되는 기능인 보안(Security), 모니터링(Monitoring) 등을 사용하고자 하는 경우, Elastic사와 OEM 계약을 체결할 필요가 있습니다.
{: .h3_box}

## Sentry: BUSL1.1 라이선스 적용
### 변경사항

{: .new  .h3_box}
Sentry의 라이선스가 Apache 2.0에서 <span>BUSL 1.1</span>{: .text-red-200} 라이선스로 변경되었습니다.<br>
[Sentry 10.0.0](https://github.com/getsentry/sentry/blob/10.0.0/LICENSE){:target="_blank" .line} 버전부터 <span>BUSL 1.1</span>{: .text-red-200} 라이선스가 적용됩니다.  

### 주의사항

변경에 따른 주의사항은 아래와 같습니다.
{: .h3_box}
- BUSL 1.1 라이선스는 일정 기간 동안 상용 목적으로의 사용이 제한되고, 일정 기간이 지나면 오픈소스 라이선스로 전환되는 라이선스입니다. 
- 버전에 명시된 날짜 또는 버전이 배포된 지 만 3년(36개월)이 지났을 때 BUSL 1.1 라이선스에서 Apache 2.0 라이선스로 적용이 가능합니다.
{: .h3_box}

### Business Source License 1.1 (BUSL 1.1)
- 일정 기간(명시된 날짜 혹은 36개월) 동안 상용 목적으로의 사용할 수 없는 제약을 가지고 있습니다.
- 단, 상용 목적이 아닌 경우에는 자유롭게 사용이 가능합니다. 
- 해당 소프트웨어 버전에 명시된 날짜 또는 버전이 배포된 지 일정 기간이 지났을 때 BUSL 1.1 라이선스에서 Apache 2.0 라이선스로 적용할 수 있습니다.
{: .h3_box}

>  **Sentry 라이선스 전환 예시**
>
>  23.7.0 버전: [Change Date: 2026-07-17, Change License: Apache License, Version 2.0](https://github.com/getsentry/sentry/blob/23.7.0/LICENSE#L19){:target="_blank" .line}
{: .h3_box}

### 참고: [Sentry FAQ](https://forum.sentry.io/t/re-licensing-sentry-faq-discussion/8044){:target="_blank" .line} for Re-licensing

#### BUSL 1.1 라이선스로 변경된 리포지토리(Reposotiry)
아래의 경우들이 모두 BUSL 1.1 라이선스로 변경되었습니다.
{: .h5_box}
- [https://github.com/getsentry/sentry](https://github.com/getsentry/sentry){: .target="_blank" .link}
- [https://github.com/getsentry/sentry-plugins](https://github.com/getsentry/sentry-plugins){: .target="_blank" .link}
- [https://github.com/getsentry/sentry-docs](https://github.com/getsentry/sentry-docs){: .target="_blank" .link}
- [https://github.com/getsentry/snuba/](https://github.com/getsentry/snuba/){: .target="_blank" .link}
- [https://github.com/getsentry/semaphore](https://github.com/getsentry/semaphore){: .target="_blank" .link}
- [https://github.com/getsentry/onpremise](https://github.com/getsentry/onpremise){: .target="_blank" .link}
- [https://github.com/getsentry/docker-sentry](https://github.com/getsentry/docker-sentry){: .target="_blank" .link}
- All Docker images produced by the repositories above
{: .h5_box}

#### Sentry 코드를 얻고 재사용하기 위한 옵션 4가지
1. <a href="https://github.com/getsentry/sentry/tree/ca8674c533a0dffc48a177554479bb85fa05891b" target="_blank">SHA ca8674c533a0dffc48a177554479bb85fa05891b</a> 커밋 이전의 코드 버전을 사용합니다(BSD-3 라이선스가 적용되었습니다).
2. 코드를 사용할 프로젝트에 Sentry의 BUSL 1.1 라이선스를 적용합니다.
3. 재사용하려는 코드가 최종적으로 Apache 2.0 라이선스로 변환될 때까지 기다립니다(일반적으로 3년의 리드 타임).
4. Sentry에서 재사용 가능한 구성 요소를 오픈소스 저장소로 가져가려면 [oss@sentry.io](mailto:oss@sentry.io)로 문의합니다. 이것이 가능하지 않은 경우에도 상황에 따라 Sentry 팀에게 해당 코드에 대한 명시적 허가를 받을 수 있습니다.  
{: .h4_box}

#### Apache 2.0 라이선스
- Sentry의 기본 라이선스입니다. 
- GPL 2.0과 호환성 이슈가 없는 경우, 기본 라이선스로 채택합니다.
{: .h4_box}


#### MIT 라이선스
- Apache 2.0 라이선스로 인해 GPL 2.0 등과 라이선스 충돌 문제가 있는 경우 사용합니다. 
- Sentry에서 제공하는 모든 SDK에 적용되어 있습니다.
{: .h4_box}

## OpenSSL: Apache 2.0 라이선스 적용
### 변경사항

{: .new }
[OpenSSL 라이선스](https://www.openssl.org/source/license-openssl-ssleay.txt){:target="_blank" .line}가 OpenSSL License and SSLeay License 듀얼 라이선스에서 <span>Apache 2.0</span>{: .text-red-200} 라이선스로 변경되었습니다.<br>
OpenSSL 3.0.0 버전부터 <span>Apache 2.0</span>{: .text-red-200}가 적용됩니다.  
{: .h3_box}

### OpenSSL 라이선스
OpenSSL 라이선스의 내용을 정리하면 아래와 같습니다.
{: .h3_box}

- 원본 및 수정된 형태의 소스코드 및 바이너리의 사용, 복제, 수정, 배포 허용
  - 소스코드 형태로 재배포 시 저작권 고지, 조건 목록, 면책조항 포함
  - 바이너리 형식 재배포 시 함께 제공되는 문서에 해당 내용 포함
  - 어떠한 형태로던 재배포될 경우 해당 문구를 포함: **This product includes software developed by the OpenSSL Project for use in the OpenSSL Toolkit.**
- 해당 기능이나 사용을 언급하는 모든 광고 자료에는 다음의 내용을 포함: **This product includes software developed by the OpenSSL Project for use in the OpenSSL Toolkit.**
- 배포된 모든 복제본은 라이선스 사항들과 저작권 고지사항을 포함
- **OpenSSL Project**와 **OpenSSL Toolkit** 이름은 특정 제품이나 서비스의 홍보에 사용될 수 없음
- 있는 그대로 제공되며 모든 보증 부인
- OpenSSL 프로젝트나 기여자는 본 소프트웨어의 사용으로 인한 직접적, 간접적, 우발적, 특별, 징벌적 또는 결과적인 손해에 대해 책임지지 않음
{: .h3_box}


### SSLeay 라이선스

SSLeay 라이선스의 내용을 정리하면 아래와 같습니다.
{: .h3_box}
- 원본 및 수정된 형태의 소스코드 및 바이너리의 사용, 복제, 수정, 배포 허용
  - 소스코드 재배포 시 저작권 고지, 조건 목록, 면책조항이 포함되어야 함
  - 바이너리 형식 재배포 시 배포와 함께 제공되는 문서 및 기타 자료에 저작권 고지, 조건 목록, 면책조항이 포함되어야 함
- 배포된 모든 복제본은 라이선스 사항, 저작권 고지사항 그리고 면책 조건을 포함
- 소프트웨어를 광고하는 모든 자료는 다음의 특정 문구를 포함: **This product includes cryptographic software written by Eric Young (eay@cryptsoft.com)**
- Windows 특정 코드나 파생된 코드를 포함할 경우 특정 문구 포함: **This product includes software written by Tim Hudson (tjh@cryptsoft.com)**
- 있는 그대로 제공되며 모든 보증 부인
- 해당 라이선스가 적용된 프로젝트 또는 그 파생물이 다른 배포 라이선스에 따라 배포하는 것은 허용되지 않음(GPL 계열 포함)
{: .h3_box}
