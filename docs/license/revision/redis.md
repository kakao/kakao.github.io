---
layout: default
title: Redis
parent: 라이선스 변경 사례
grand_parent: 오픈소스 라이선스
nav_order: 6
---
# {{ page.title }}

## Redis : RSAL, SSPL Dual License 적용
### 변경사항
라이선스 변경사항은 아래와 같습니다.


{: .div_box}
Redis의 라이선스가 BSD-3 에서  <span> RSALv2(Redis Source Available License) 또는 SSPLv1(Server Side Public License)</span>{: .text-red-400 }로 변경되었습니다.<br>
Redis 7.4 버전부터 RSALv2(Redis Source Available License) 또는 SSPLv1(Server Side Public License) 라이선스가 적용됩니다.([Redis Dual 라이선스 적용](https://redis.io/blog/redis-adopts-dual-source-available-licensing/){:target="_blank" .line})<br>
이전에 사용되던 BSD-3 라이선스가 더이상 적용되지 않습니다.<br>

### 주의 사항
변경에 따른 주의사항은 아래와 같습니다.

- 새로운 라이선스에 따라 Redis 제품을 호스팅하는 클라우드 서비스 제공업체는 더 이상 Redis 소스 코드를 무료로 사용할 수 없습니다. 
- 예를 들어, 클라우드 서비스 제공업체는 Redis 코드 유지 관리업체인 Redis와의 라이선스 조건에 동의한 후에만 Redis 7.4를 제공할 수 있습니다.
- [RSALv2(Redis Source Available License)](https://redis.com/legal/rsalv2-agreement/){:target="_blank"} 특징
  - 사용/배포등은 자유롭지만 Redis 이외 다른 클라우드 등에서 서비스하는 것을 제한하는 형태의 라이선스
  

### FAQ 주요 사항
#### 3. Redis 오픈 소스 제품의 최종 사용자에게 이러한 변경이 미치는 영향은 무엇입니까?
{: .fs-4 .mt-0}
Redis 오픈 소스 버전의 Redis와 내부 또는 개인 용도로 이중 라이선스 중 하나를 사용하는 새 릴리스를 사용하는 최종 사용자의 경우에는 변경 사항이 없습니다.


#### 7. Redis RSALv2 또는 SSPLv1 라이선스에 정의된 "경쟁 제품"이란 무엇입니까?
{: .fs-4}
"경쟁 제품"은 유료 지원 계약을 포함하여 제3자에게 판매되는 제품으로, Redis의 코드 기반에서 파생되었으며 Redis 상용 제품의 기능과 상당히 중복됩니다. 예를 들어, 이 정의에는 Redis 상용 버전(Redis 엔터프라이즈 소프트웨어 또는 Redis 클라우드)과 경쟁적으로 판매되는 솔루션의 일부로 Redis를 호스팅하거나 내장하는 것이 포함됩니다. 더욱 명확성을 제공하고 RSALv2 또는 SSPLv1 제한을 뛰어넘는 사용 사례를 지원하기 위해 맞춤형 라이선스 조건도 제공됩니다.


#### 11. 원래의 3절 BSD 라이센스에 따라 제공된 제품 버전을 계속 사용할 수 있습니까?
{: .fs-4}
예. 라이센스 변경은 소급 적용되지 않습니다. 이는 변경 이전의 모든 소스 코드와 릴리스가 3절 BSD 라이센스에 따라 유지된다는 것을 의미합니다. 귀하는 해당 이용 약관을 준수하는 한 원래 라이센스에 따라 해당 버전을 무기한으로 계속 사용할 수 있습니다. Redis는 [현재 보안 정책](https://github.com/redis/redis/security/policy){:target="_blank"}에 따라 Redis Community Edition이 출시될 때까지 계속해서 보안 업데이트를 제공하고 이러한 릴리스 내에서 기타 중요한 결함을 해결할 계획입니다 .

#### 12. Redis는 3절 BSD 라이센스에 따라 보안 패치를 이전 릴리스로 백포트합니까?
{: .fs-4}
Redis는 [현재 보안 정책](https://github.com/redis/redis/security/policy){:target="_blank"}에 따라 Redis Community Edition 9.0이 출시될 때까지 사용 가능한 중요한 보안 패치를 3항 라이선스에 따라 기존 버전으로 계속 백포트할 것입니다 . 해당 날짜 이후의 모든 패치는 새로운 이중 라이센스에 따라 제공됩니다.

#### 20. Redis를 조직 내부의 서비스로 호스팅할 수 있습니까?
{: .fs-4}
예. RSALv2 또는 SSPLv1의 조건은 당사 소프트웨어를 포함하거나 호스팅하는 제3자에게 경쟁 제품을 제공하는 경우를 제외하고 모든 비프로덕션 및 프로덕션 사용을 허용합니다. 조직 내부 사용을 위한 제품 호스팅은 허용됩니다. 조직에는 계열사와 자회사가 포함됩니다. 이는 한 부서가 다른 내부 부서에서 사용할 Redis를 호스팅할 수 있음을 의미합니다.

### 참고
- Linux Foundataion에서 [Valkey](https://valkey.io/){:target="_blank"} 라는 이름으로 Redis 프로젝트를 계속 개발해 나갈 예정입니다.
> 개발 기준이 되는 버전은 7.2.4이고 BSD-3 라이선스가 적용됩니다. <br>
> [https://www.linuxfoundation.org/press/linux-foundation-launches-open-source-valkey-community](https://www.linuxfoundation.org/press/linux-foundation-launches-open-source-valkey-community){:target="_blank"}
