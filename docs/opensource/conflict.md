---
layout: default
title: 오픈소스 분쟁 사례
parent: 오픈소스
nav_order: 3
---
# {{ page.title }}
오픈소스 라이선스 의무사항을 준수하지 않으면 저작권법 위반으로 코드 공개, 판매금지 및 손해배상 등의 법적 처분을 받을 수 있으므로 주의해야 합니다.<br>
오픈소스 라이선스 분쟁은 계속해서 발생하고 있으며, 이 가이드에서는 그중 일부 사례를 소개합니다.
{: .summary }

## Oracle vs Google
[Google과 Oracle의 Java 소송](http://www.zdnet.co.kr/news/news_view.asp?artice_id=20180328163651&lo=zv40){:target="_blank"}
- Google이 안드로이드(Android)에 Java API 37개를 사용
- Oracle이 Google을 상대로 특허 및 저작권 침해로 10조($90억) 손해배상 소송 제기

### 히스토리(History)
  - 2012년 1심: API 저작권 인정하지 않음
  - 2014년 항소심: API 저작권 인정
  - 2015년 연방대법원: **API 저작권 인정 확정**, 공정이용 여부 확인을 위해 1심으로 돌려보냄
  - 2016년 1심: API 공정이용 판결
  - 2018년 항소심: API 공정이용 아닌 것으로 판결, Goolge 측이 Oracle에 대해 배상 판결
  - 2020년 10월 7일 상고심
  - 2021년 4월 5일 최종 판결: [**공정이용으로 구글 승소**](https://m.yna.co.kr/view/AKR20210405154751071?section=international/all){:target="_blank"}

**최종 판결**<br>
공정이용의 4가지 요건에 대한 판단이 있었고 그중 저작물 이용의 목적과 성격에 대해, Google의 Java API 사용이 새로운 플랫폼인 안드로이드 스마트폰 환경을 위한 창의적이고 혁신적인 도구 제공을 위한 변형적 이용이므로, 공정이용으로 판단되었습니다.<br>
보다 자세한 내용은 [**API는 공정이용(fair use)의 대상인가**](https://m.lawtimes.co.kr/Content/Article?serial=169564){:target="_blank"} 기사를 참고합니다.
{: .div_box}

----

## 한글과컴퓨터 vs Artifex
[한글과컴퓨터와 Artifex의 고스트스크립트(Ghostscript) 소송](http://www.ddaily.co.kr/news/article.html?no=156012){:target="_blank"}

- 한컴오피스가 자사 제품에 Artifex의 고스트스크립트(Ghostscript)를 내장해, 한컴오피스 문서를 PDF 파일로 변환하는 데 사용
- Artifex가 미국법원에 한글과컴퓨터를 상대로 계약 위반 및 저작권 침해 소송 제기

### 히스토리(History)
- 2017년 4월 25일: 법원이 오픈소스 라이선스가 집행력 있는 계약임을 인정
- 12월 합의: [205만 달러 배상](http://www.sisaweek.com/news/articleView.html?idxno=109614){:target="_blank" .line} 
  - 한글과컴퓨터의 2015년 매출인 약 8,630만 달러의 2.37%를 손해배상


>  **참고하기**
>
>  손해배상은 침해로 인해 라이선스 소유자가 얻지 못한 이익 및 침해자가 얻은 이익 등을 고려해서 결정되었습니다.  
>  보다 자세한 내용은 [**Quartz - A federal court has ruled that an open-source license is an enforceable contract**](https://qz.com/981029/a-federal-court-has-ruled-that-an-open-source-license-is-an-enforceable-contract){:target="_blank"} 링크를 참고합니다.



> **고스트스크립트(Ghostscript)**
> - [고스트스크립트(Ghostscript) 라이선스](https://www.ghostscript.com/licensing/){:target="_blank"}: AGPL, Commercial 듀얼 라이선스로 선택 가능
> - AGPL: 9.07 버전부터 GPL → AGPL로 라이선스 변경
> - Commercial: 라이선스 구매 
{: .div_box}
  
----

## VMWare vs 리눅스 개발자
[VMWare와 리눅스 개발자 간 소송](http://www.oss.kr/oss_news/609022){:target="_blank"}
- VMWare ESXi에 리눅스 커널 코드 사용
- 개발자 크리스토프 헬비그(Christoph Hellwig)가 고소 진행, 오픈소스 관련 단체의 지원

### 히스토리(History)
- 2017년 8월 : [함부르크 지방법원이 소송 기각 결정](https://opensource.com/law/16/8/gpl-enforcement-action-hellwig-v-vmware){:target="_blank"}
  - ESXi의 Vmklinux에서 사용 중으로 소스 코드 제공하여 GPL 준수하고 있음
  - Vmkernel에는 사용되지 않음
  - Vmklinux와 Vmkernel의 결합방식은 다루지 않음
- 크리스토프 헬비그가 항소를 밝혔으나 이후 합의

----

## Skype vs gpl-violations.org
[Skype가 판매한 SMC 전화 단말기 WSKP100가 GPL2 위반(2007년 7월 29일)](http://www.zdnet.co.kr/news/news_view.asp?artice_id=00000039159822&type=det&re=){:target="_blank"}
- 소프트웨어 제조 업체는 SMC지만, **Skype가 해당 제품을 실질적으로 웹사이트를 통해 판매(유통)했으므로, 라이선스 요건 충족에 책임을 져야 한다**라고 판결
- 소스 코드 공개 및 벌금 지불 판결
- 유통 업체에게도 GPL 위반 책임을 물은 사례이며, 본국이 아닌 독일에서 소송 및 판결

----

## 엘림넷 vs 하이온넷
[VTUND 기반의 엘림넷 제품을 하이온넷이 개작/상용화해 GPL 위반(2005년)](https://olis.or.kr/library/maindataDetail.do?bbsId=120&bbsNum=546){:target="_blank"}
- GPL이 관련된 대한민국 최초의 법정 사건
- 엘림넷에서 VTUND를 기반으로 개발한 ETUND를 하이온넷에서 HL로 개작 및 상용화
- 엘림넷은 영업비밀 침해에 대한 고소 진행, FSF와 GNU는 저작권법 위반 경고

----

## Xiaomi MIUI의 GPL 위반
[Xiaomi가 MIUI에 리눅스 커널 기반 GPL 코드 포함(2014년)](http://www.hitech.co.kr/main/bbsview.php?gMenu=101&num=783){:target="_blank"}

- [Xiaomi의 MIUI가 리눅스 커널 기반의 GPL 코드](http://www.hitech.co.kr/main/bbsview.php?gMenu=101&num=783){:target="_blank"}를 사용
- 이후 2015년 3월 31일에 Xiaomi의 Mi3, Mi4, Mi Note의 [소스 코드 공개](http://www.oss.kr/oss_news/616161){:target="_blank"} - 2015.3.31
  - 코드 공개는 2014년 10월에 약속했으며, 자사 기기의 정보가 너무 많이 유출된다며 공개를 미루다, 수정 후 공개 진행

----

## Orange GPL위반
[프랑스 법원, 대형 통신사 Orange에게 GPL 위반으로 손해배상 판결](https://heathermeeker.com/2024/02/17/french-court-issues-damages-award-for-violation-of-gpl/){:target="_blank"}
- 2005년 프랑스 대형 통신사인 Orange는 프랑스 전자 행정 개발청과 **My Public Service** 개발 계약 체결
- 개발과정에서 SAML 프로토콜 구현을 위해 [Lasso](https://lasso.entrouvert.org/){:target="_blank" .line} 사용
- Orange는 상업용 라이선스를 구입하지 않고 Lasso 소프트웨어 출처와 라이선스를 명시하지 않으며, 수정된 소스 코드를 공개하지 않음
- Lasso의 개발사인 엔트루베르(Entr’Ouvert)는 해당 케이스를 발견하고 Orange 사를 상대로 손해배상을 청구

### 히스토리(History)
- 2005년: Orange 사는 service-public.fr 포털의 일부를 개발하며 해당 솔루션에 Lasso 소프트웨어를 사용
- 2010년: 엔트루베르 사가 [Orange 사를 고소](https://www.entrouvert.com/actualites/2019/entrouvert-versus-orange/){:target="_blank"}
- 2021년: 항소법원은 엔트루베르의 저작권 침해 청구를 먼저 기각하면서 이 사건이 계약 위반 청구라 함
- 2022년: 프랑스의 대법원인 파기원(Court of Cassation)은 이 사건을 검토하고 2022년 10월 5일에 항소법원의 판결을 뒤집는 명령을 내림
- 2024년 2월 14일: 최종 판결이 내려졌으Orange 사가 패소. 총 650,000유로(한화 약 9억 4천만 원)를 엔트루베르에 지불하라고 명령


**최종 판결**<br>
Orange가 Entr'Ouvert의 Lasso 소프트웨어에 대한 저작권을 침해하고 GPL을 위반하여, Orange에게 50만 유로의 손해배상금과 15만 유로의 정신적 손해배상금을 지불하라고 명령했습니다.<br>
보다 자세한 내용은 프랑스 법원, [GPL 위반에 대한 손해배상 판결 내려](https://heathermeeker.com/2024/02/17/french-court-issues-damages-award-for-violation-of-gpl/){:target="_blank"} 기사를 참고합니다.
{: .div_box}

----

## 게임 관련 분쟁 사례

### 일본 LEAF사의 GPL 위반(2005년)
- 게임 오프닝 화면 동영상에 XviD 코덱 사용
- 홈페이지에 사과문 게재 및 게임 코드 전체 공개
- 일본의 PS2 게임 ICO 오픈소스 위반(2007년)


### SONY가 PlayStation2 게임인 이코(ICO)의 GPL 위반(2007년)
- SONY PlayStation2 게임 ICO에 GPL 라이선스 라이브러리(librac) 사용
- 전체 코드 공개

