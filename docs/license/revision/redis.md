---
layout: default
title: Redis
parent: 라이선스 변경 사례
grand_parent: 오픈소스 라이선스
nav_order: 6
---
# {{ page.title }}

## Redis : AGPL License 추가
### 변경사항
라이선스 변경사항은 아래와 같습니다.


{: .div_box}
Redis의 라이선스가 BSD-3 에서  <span> RSALv2(Redis Source Available License) 또는 SSPLv1(Server Side Public License)</span>{: .text-red-400 }로 변경되었습니다.<br>
Redis 7.4 버전부터 RSALv2(Redis Source Available License) 또는 SSPLv1(Server Side Public License) 라이선스가 적용됩니다.([Redis Dual 라이선스 적용](https://redis.io/blog/redis-adopts-dual-source-available-licensing/){:target="_blank" .line})<br>
이전에 사용되던 BSD-3 라이선스가 더이상 적용되지 않습니다.<br><br>
Redis 8.0 버전부터 AGPLv3 라이선스가 추가된 <span> RSALv2(Redis Source Available License), SSPLv1(Server Side Public License), AGPLv3(Server Side Public License)의 [Triple 라이선스](https://redis.io/blog/agplv3/){:target="_blank" .line}</span>{: .text-red-400 }가 적용됩니다.<br>

### 라이선스 별 제한 사항
#### RSAL 2.0 (Redis Source Available License 2.0)
{: .fs-4 .mt-0}
- Redis의 기능을 제3자에게 서비스 형태로 제공할 수 없습니다.(클라우드 서비스 또는 SaaS 형태로도 제공이 불가합니다.)
- Redis를 기반으로 기능이 중심이 되는 제품 또는 서비스를 제공하는 것은 제한됩니다.

#### SSPL 1.0 (Server Side Public License 1.0)
{: .fs-4 .mt-0}
- Redis를 **네트워크 기반 서비스(SaaS, 클라우드 등)**로 제공할 경우, 서비스를 구성하는 **모든 프로그램의 소스 코드(Service Source Code)**를 전체 공개해야 합니다.
- 이는 Redis뿐만 아니라 서비스를 구현하는 모든 관련 소프트웨어에도 적용됩니다.

#### AGPL 3.0 (Affero General Public License 3.0)
{: .fs-4 .mt-0}
- Redis를 **네트워크를 통한 서비스(SaaS, 클라우드 등)**로 제공하는 경우, Redis의 소스 코드뿐 아니라, 이를 기반으로 한 모든 수정 사항과 추가 개발 코드까지 공개해야 합니다.
- 사용자가 소프트웨어에 네트워크를 통해 접근하는 경우에도 Copyleft 조건이 적용됩니다.


### 라이선스 변경
#### 2024.03.22 – 1차 라이선스 변경
{: .fs-4 .mt-0}
- Redis 7.4 ~ 7.8 버전부터는 RSALv2(Redis Source Available License) 또는 SSPLv1 중 하나를 선택하여 적용합니다.
- Redis Stack과 Redis Core의 통합이 본격적으로 시작됩니다.
- 커뮤니티 사용자에게는 Redis가 계속 무료로 제공되며, 클라우드 서비스 제공업체는 Redis와의 계약을 체결한 후에만 사용이 가능합니다.

#### 2025.05.01 – 2차 라이선스 변경 (Redis 8 출시와 함께)
{: .fs-4 .mt-0}
- Redis 8부터는 AGPLv3가 추가된 트리플 라이선스 (RSALv2 / SSPLv1 / AGPLv3) 로 변경 되었습니다.
- Redis Stack의 고급 기능들(JSON, 시계열, 벡터, 확률적 데이터 등)이 핵심 Redis에 통합됩니다.
- 최대 87% 더 빠른 명령 처리 속도와 2배 향상된 처리량을 포함한 30가지 이상의 성능 개선을 제공합니다.
- Redis의 창시자 Salvatore Sanfilippo(antirez)가 복귀하며, 커뮤니티 주도 개발이 다시 활성화됩니다.

### 주의 사항
변경에 따른 주의사항은 아래와 같습니다.

- 새로운 라이선스에 따라, Redis 제품을 호스팅하는 클라우드 서비스 제공업체는 더 이상 Redis 소스 코드를 자유롭게 사용할 수 없습니다.
  예를 들어, 클라우드 서비스 제공업체는 Redis 코드 유지 관리업체인 Redis와의 정식 라이선스 계약을 체결한 경우에만 Redis 7.4를 제공할 수 있습니다.
- Redis는 [RSALv2(Redis Source Available License)](https://redis.com/legal/rsalv2-agreement/){:target="_blank"} 를 도입하였으며,
  이는 사용 및 배포는 자유롭지만 Redis 이외의 클라우드 서비스 환경에서 Redis를 서비스 형태로 제공하는 것을 제한하는 라이선스입니다.
- Redis 클라이언트 라이브러리는 기존과 동일하게 오픈소스 라이선스를 유지합니다.
- Redis는 파트너 프로그램을 통해 클라우드 제공업체 및 시스템 통합업체에게 정식 라이선스를 기반으로 지속적인 업데이트 및 기술 지원을 제공합니다.
- 기존 Redis Enterprise 고객에게는 이번 변경으로 인한 영향이 없습니다.
- 이번 라이선스 변경은 커뮤니티 사용자에게 불이익을 주지 않으면서도, Redis 생태계의 지속 가능한 발전과 기술 혁신을 위한 전략적 결정입니다.


### FAQ 주요 사항 (v8.0)
#### Q. AGPLv3 라이선스는 BSD3 라이선스와 어떻게 다릅니까?
{: .fs-4 .mt-0}
BSD3와 AGPLv3는 오픈소스 라이선스에 대한 서로 다른 접근 방식을 나타냅니다.<br>
BSD3는 저작권 고지와 면책 조항을 유지하는 한, 코드를 독점 소프트웨어에 사용하는 것을 포함하여 거의 모든 방식으로 활용할 수 있도록 허용하는 관대한(permissive) 라이선스입니다.<br>
반면, AGPLv3는 수정된 버전을 동일한 조건으로 배포해야 하는 카피레프트(Copyleft) 라이선스이며, 여기에 더해 네트워크를 통해 소프트웨어와 상호작용하는 사용자에게 소스 코드를 공개해야 한다는 추가 요건이 있습니다.<br>
이러한 "네트워크 조항"은 AGPLv3의 핵심 특징으로, 웹 애플리케이션 사용자 또한 소스 코드에 접근할 수 있도록 보장하기 위해 설계된 조건입니다.

#### Q. Redis가 다시 라이선스를 변경하면 어떻게 되나요?
{: .fs-4}
현재 Redis 오픈소스 라이선스 구성(RSALv2/SSPLv1/AGPLv3)을 변경하거나 추가할 계획은 없습니다.<br>
우리는 Redis의 오픈소스를 AGPLv3 라이선스 하에 계속 유지할 계획입니다.<br>
AGPLv3는 우리의 비즈니스 모델에 가장 적합한 라이선스이고, 라이선스의 안정성은 커뮤니티의 필수라고 판단했기 때문입니다.<br>
Redis 커뮤니티는 우리의 핵심 기반이라는 사실을 잘 알고 있으며 앞으로도 이를 계속 유지할 것입니다.

#### Q. 저는 Redis 커뮤니티 사용자입니다. AGPLv3 추가가 영향을 미칠까요?
{: .fs-4}
대부분의 경우 별도의 영향을 받지 않습니다.<br>
만약 Redis Community Edition(7.4.x 이상) 또는 Redis Stack에서 Redis 8로 전환하는 경우,<br>
Redis 7.2 이하의 오픈소스 버전을 사용하되, Redis에서 제공한 코드나 바이너리를 수정 없이 그대로 사용하는 경우 영향을 받지 않습니다.<br>

그러나, Redis 7.2 이하 버전의 코드를 수정해서 사용하고, 이를 네트워크 서버 형태로 제공하는 경우에는, 해당 서버 운영자는 사용 중인 수정된 버전의 소스 코드를 사용자에게 공개해야 합니다.<br>

#### Q. 저는 Redis 포크(fork)를 사용 중입니다. 그런데 왜 공식 Redis를 고려해야 하나요?
{: .fs-4}
Redis Ltd.는 공식 Redis 프로젝트를 주도하는 회사로, 커뮤니티를 위한 발전에 전념하고 있으며, 상충되는 이해관계 없이 Redis의 비전 수립과 실현을 주도합니다.<br>
Redis와 유사한 다른 제품이나 포크들이 존재하지만, Redis에 투자하고 혁신을 이끄는 정도는 우리가 가장 앞서 있고, 다른 포크나 모방 프로젝트는 종종 우리의 API나 기능을 복제하지만, 수개월에서 수년 이상 뒤처져 있는 경우가 많습니다.<br>
공식 Redis는 공식 클라이언트 라이브러리, Redis Insight, Redis Copilot, VS Code용 Redis 확장 등 모든 개발자 도구와 리소스가 최신 Redis를 지원하도록 유지하고 있습니다.<br>
새로운 기능이 출시될 때는 Redis Insight의 가이드 및 튜토리얼을 통해 학습을 지원하고, 전용 Discord 채널, GitHub 이슈, Stack Overflow, Reddit 등에서 활발히 커뮤니티를 지원하고 있습니다.<br>
공식 문서는 Redis API뿐만 아니라 모든 클라이언트 라이브러리 API에 대해서도 폭넓게 다루고 있습니다.

### FAQ 주요 사항 (v7.4)
#### 3. Redis 오픈 소스 제품의 최종 사용자에게 이러한 변경이 미치는 영향은 무엇입니까?
{: .fs-4 .mt-0}
Redis 오픈 소스 버전의 Redis와 내부 또는 개인 용도로 이중 라이선스 중 하나를 사용하는 새 릴리스를 사용하는 최종 사용자의 경우에는 변경 사항이 없습니다.


#### 7. Redis RSALv2 또는 SSPLv1 라이선스에 정의된 "경쟁 제품"이란 무엇입니까?
{: .fs-4}
"경쟁 제품"은 유료 지원 계약을 포함하여 제3자에게 판매되는 제품으로, Redis의 코드 기반에서 파생되었으며 Redis 상용 제품의 기능과 상당히 중복됩니다. 예를 들어, 이 정의에는 Redis 상용 버전(Redis 엔터프라이즈 소프트웨어 또는 Redis 클라우드)과 경쟁적으로 판매되는 솔루션의 일부로 Redis를 호스팅하거나 내장하는 것이 포함됩니다. 더욱 명확성을 제공하고 RSALv2 또는 SSPLv1 제한을 뛰어넘는 사용 사례를 지원하기 위해 맞춤형 라이선스 조건도 제공됩니다.


#### 11. 원래의 3절 BSD 라이선스에 따라 제공된 제품 버전을 계속 사용할 수 있습니까?
{: .fs-4}
예. 라이선스 변경은 소급 적용되지 않습니다. 이는 변경 이전의 모든 소스 코드와 릴리스가 3절 BSD 라이선스에 따라 유지된다는 것을 의미합니다. 귀하는 해당 이용 약관을 준수하는 한 원래 라이선스에 따라 해당 버전을 무기한으로 계속 사용할 수 있습니다. Redis는 [현재 보안 정책](https://github.com/redis/redis/security/policy){:target="_blank"}에 따라 Redis Community Edition이 출시될 때까지 계속해서 보안 업데이트를 제공하고 이러한 릴리스 내에서 기타 중요한 결함을 해결할 계획입니다 .

#### 12. Redis는 3절 BSD 라이선스에 따라 보안 패치를 이전 릴리스로 백포트합니까?
{: .fs-4}
Redis는 [현재 보안 정책](https://github.com/redis/redis/security/policy){:target="_blank"}에 따라 Redis Community Edition 9.0이 출시될 때까지 사용 가능한 중요한 보안 패치를 3항 라이선스에 따라 기존 버전으로 계속 백포트할 것입니다 . 해당 날짜 이후의 모든 패치는 새로운 이중 라이선스에 따라 제공됩니다.

#### 20. Redis를 조직 내부의 서비스로 호스팅할 수 있습니까?
{: .fs-4}
예. RSALv2 또는 SSPLv1의 조건은 당사 소프트웨어를 포함하거나 호스팅하는 제3자에게 경쟁 제품을 제공하는 경우를 제외하고 모든 비프로덕션 및 프로덕션 사용을 허용합니다. 조직 내부 사용을 위한 제품 호스팅은 허용됩니다. 조직에는 계열사와 자회사가 포함됩니다. 이는 한 부서가 다른 내부 부서에서 사용할 Redis를 호스팅할 수 있음을 의미합니다.


> **참고하기**
>
> - 현재 버전(v8.0) FAQ는 [https://redis.io/legal/licenses/](https://redis.io/legal/licenses/){:target="_blank"}, v7.4 FAQ는 [https://redis.io/blog/redis-adopts-dual-source-available-licensing/](https://redis.io/blog/redis-adopts-dual-source-available-licensing/){:target="_blank"} 하단에서 확인할 수 있습니다. 
{: .fs-3}
︎ 

### 참고
- Linux Foundataion에서 [Valkey](https://valkey.io/){:target="_blank"} 라는 이름으로 Redis 프로젝트를 Fork 하여 개발하고 있습니다.
> 개발 기준이 되는 버전은 7.2.4이고 BSD-3 라이선스가 적용됩니다. <br>
> [https://www.linuxfoundation.org/press/linux-foundation-launches-open-source-valkey-community](https://www.linuxfoundation.org/press/linux-foundation-launches-open-source-valkey-community){:target="_blank"}
