---
layout: default
title: mongoDB
parent: 라이선스 변경 사례
grand_parent: 오픈소스 라이선스
nav_order: 2
---
# {{ page.title }}

## mongoDB: SSPL 라이선스 적용
### 변경사항
라이선스 변경사항은 아래와 같습니다.


{: .div_box}
[mongoDB](https://github.com/mongodb/mongo){:target="_blank" .line}의 라이선스가 AGPL에서 <span>SSPL</span>{: .text-red-400 }로 변경되었습니다.<br>
2018년 10월 16일 이후의 릴리스(Release)에 대해 <span>SSPL</span>{: .text-red-400 }이 적용됩니다(이전 버전의 패치도 포함합니다).<br>

### 주의사항

변경에 따른 주의사항은 아래와 같습니다.


- 외부에 서비스로 제공하는 경우 서비스 소스 코드(Service Source Code)를 전체 공개해야 합니다.
- SaaS, 클라우드 등 제 3자에게 제공되는 모든 서비스를 포함합니다.



>  **서비스 소스 코드(Service Source Code)란?**
>
>  본 프로그램 또는 수정된 버전의, 서비스를 구성하는 모든 프로그램의 소스 코드 및 관리 소프트웨어 전체를 의미합니다.
>  애플리케이션 프로그램의 인터페이스, 자동화 소프트웨어, 모니터링 소프트웨어, 백업 소프트웨어, 스토리지 소프트웨어 및 호스팅 소프트웨어 등 사용자가 실행할 수 있는 모든 서비스의 인스턴스가 해당합니다.


### SSPL 라이선스로 변경

2018년 10월 16일 이전 버전은 AGPL 라이선스이며, 그 이후 릴리스는 SSPL로 변경되었습니다(이전 버전의 패치도 포함합니다).


<div class="div_box">
<strong class="fs-3">라이선스 변경 관련 원문</strong><br><br>
<code class="fs-2">MongoDB is free and open-source. Versions released prior to October 16,2018 are published under the AGPL.<br>
All versions released after October 16, 2018, including patch fixes for prior versions, are published under the Server Side Public License (SSPL) v1.<br>See individual files fordetails.</code>
</div>

SSPL 라이선스로 변경한 자세한 이유는 [MongoDB now released under the Server Side Public License](https://www.mongodb.com/blog/post/mongodb-now-released-under-the-server-side-public-license){:target="_blank" .line} 에서 확인할 수 있습니다.

라이선스의 변경사유는 아래와 같습니다.

- AWS와 같은 클라우드 서비스 제공자가 오픈소스를 사용하여 플러그 앤드 플레이(Plug and Play) 형태로 제공하며 수익을 창출하게 됨에 따라, 이를 방지하고자 SSPL 또는 상용 라이선스로 변경하였습니다.
- SSPL 라이선스는 13조에서 해당 라이선스를 사용하는 프로젝트를 서비스로 제공하는 경우 **서비스 소스 코드**를 제공하라는 조항을 추가하고, **서비스 소스 코드**를 새롭게 정의하였습니다.
- SSPL 라이선스는 오픈소스 OSI(Open Source Initiative)에서 승인이 되지 않은 라이선스입니다.
  
