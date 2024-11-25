---
layout: default
title: ElasticSearch
parent: 라이선스 변경 사례
grand_parent: 오픈소스 라이선스
nav_order: 3
---
# {{ page.title }}

## ElasticSearch: Elastic License 2.0, SSPL 듀얼 라이선스 적용
### 변경사항
라이선스 변경사항은 아래와 같습니다.


{: .div_box}
Elasticsearch와 Kibana의 라이선스가 Apache 2.0에서 <span>Elastic License 2.0, SSPL의 듀얼 라이선스</span>{: .text-red-400 }로 변경되었습니다.<br>
Elastic 7.11 릴리즈부터 ElasticSearch와 Kibana에 <span>Elastic License 2.0, SSPL의 듀얼 라이선스</span>{: .text-red-400 }가 적용됩니다.([Elastic 라이선스 변경](https://www.elastic.co/kr/blog/licensing-change){:target="_blank" .line})<br><br>
Elastic 8.16 릴리즈부터는 ElasticSearch와 Kibana에 AGPL3.0이 추가된 <span>AGPL 3.0, Elastic License 2.0, SSPL의 멀티 라이선스</span>{: .text-red-400 }가 적용됩니다.([Elasticsearch Is Open Source. Again!](https://www.elastic.co/kr/blog/elasticsearch-is-open-source-again){:target="_blank" .line})<br>

> **라이선스 설명**
>
> - **Elastic License 2.0:** 클라우드 서비스 공급자가 Elasticsearch 및 Kibana를 서비스로 제공하지 못하도록 제한합니다.
> - **SSPL:** 외부에 서비스로 제공하는 경우 **서비스 소스 코드(Service Source Code)** 전체 공개의 의무가 있습니다.
{: .fs-3}

### 주의사항

변경에 따른 주의사항은 아래와 같습니다.

- 베이식(Basic) 라이선스는 자체 서비스 등을 위해 직접 구축할 경우, 계속 무료로 사용할 수 있으며, 상업적으로 제품에 포함시키는 등의 재판매는 금지합니다.
- 오픈소스 버전의 경우 기본적으로 SSPL(Server Side Public License) 1.0과 Elastic License 2.0의 듀얼 라이선스가 적용되며, 각 파일 헤더에 명시된 라이선스가 우선 적용됩니다.
- x-pack 디렉터리 하위는 Elastic License가 적용되므로, 베이식(Basic) 이상에 포함되는 기능인 보안(Security), 모니터링(Monitoring) 등을 사용하고자 하는 경우, Elastic사와 OEM 계약을 체결할 필요가 있습니다.
  
