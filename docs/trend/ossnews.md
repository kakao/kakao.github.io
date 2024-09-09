---
layout: default
title: 오픈소스 뉴스
parent: 오픈소스 동향
#has_children: true
nav_order: 1
---
# {{ page.title }}
<div class="summary">
이 가이드에서는 오픈소스 동향을 알아봅니다.
</div>

## 오픈소스 AI 업계 판도 바꿀까?··· 애널리스트가 본 리눅스재단 AI 모델의 가능성
- [https://www.ciokorea.com/news/347512](https://www.ciokorea.com/news/347512){:target="_blank" .link}

### 요약
기존 AI 모델은 소스코드를 비공개 또는 공개하되 사용 정책 관련하여 제한을 두고 있습니다.<br>
리눅스 재단에서 계확하고 있는 OMI는 이러한 제한없이 사용할 수 있는 AI 모델을 만드는 것을 목표로 하고 있다고 합니다.<br>
OMI가 기존 빅테크 모델보다 경정력이 있지는 않겠지만, Small Language Model에서는 활용 가능성이 있을것으로 전망하고 있습니다.<br>
{: .h3_box}

### 내용
지난 12일 리눅스 재단이 OMI를 지원하겠다는 발표가 나온 뒤, 이 프로젝트가 윤리적 LLM의 개발을 이끌 수 있을 것이라는 분석이 나오고 있다.<br>
OMI는 기존의 상용 모델과 동등하거나 더 나은 품질을 유지하면서도 사용 제한이 없는 커뮤니티 기반 LLM을 만드는 것을 목표로 삼고 있다.<br><br>
<strong>OMI(Open Model Initiative)</strong>란 무엇인가?<br>
OMI는 인보크(Invoke), 시비타이(Civitai), 컴피 오르그(Comfy Org)라는 세 개의 스타트업이 6월에 만든 프로젝트로, 개발자, 연구자, 기업이 함께 모여 개방적이고 허용적인 라이선스를 가진 AI 관련 모델 기술을 만들겠다는 목표를 추구하고 있다.<br>
리눅스 재단에 따르면, 허용적인 라이선스는 커뮤니티 구성원이 별도의 의무 없이 기여를 할 수 있는 환경을 만들어 많은 사람의 참여를 독려할 수 있다.<br>
오픈소스 코드를 바탕으로 상용 소프트웨어를 개발하는 경우에도 매우 유용하다.<br><br>
OMI Github Project: [https://github.com/Open-Model-Initiative](https://github.com/Open-Model-Initiative){:target="_blank" .link}
{: .h3_box}

#### 참고
* [https://www.ciokorea.com/news/347512](https://www.ciokorea.com/news/347512){:target="_blank" .link}
{: .fs-3 .h4_box }


## 깃허브 코파일럿 vs. 오픈소스 개발자 집단 소송, 개발자 측 패소
- [https://www.itworld.co.kr/news/343788#csidxac69a879cc30827a9dd6433f988397a](https://www.itworld.co.kr/news/343788#csidxac69a879cc30827a9dd6433f988397a){:target="_blank" .link}

### 요약
2022년 11월에 제기된 github 코파일럿 관련 소송이 샌프란시스코 지방법원에 의해 대부분 기각되었다는 소식입니다.<br>
향후 오픈소스 개발자 집단에서 어떤 형태로 대응이 진행될지 지켜봐야 할것 같네요.<br>
{: .h3_box}


### 내용
6월 24일에 처음 발표되었지만 7월 5일에야 일반 공개된 판결문에서 캘리포니아 북부 지방법원 판사 존 타이가는 "<strong>원고의 주장은 추구하는 구제책을 뒷받침하지 못했다. 원고는 부당이득에 대한 배상이 계약 위반 청구에 대한 원고의 손해 배상 수단으로 가능하다는 점을 법적으로 입증하지 못했다</stong>"라고 판시했다.<br><br>
{: .h3_box}
타이가 판사는 이어서 "<strong>법원은 원고의 1202(b) 조항 청구를 재소 불가능 조건으로 기각한다. 법원은 모든 피고를 대상으로 오픈소스 라이선스 위반 계약에 대한 원고의 청구를 기각한다. 마지막으로, 원고의 부당이득금 형태의 금전적 구제 요청과 원고의 징벌적 손해배상 요청을 기각한다</strong>”라고 판결했다.<br><br>
{: .h3_box}

#### 참고: 집단 소송 관련 뉴스
* [https://www.itworld.co.kr/news/264316](https://www.itworld.co.kr/news/264316){:target="_blank" .link}
* [https://www.copyright.or.kr/information-materials/trend/the-copyright/viewPress.do?brdctsno=51490](https://www.itworld.co.kr/news/264316){:target="_blank" .link}
{: .fs-3 .h4_box }


## 오픈소스 인공지능 인프라 Ollama에서 확인된 취약점: Probllama
- [https://nvd.nist.gov/vuln/detail/CVE-2024-37032](https://nvd.nist.gov/vuln/detail/CVE-2024-37032){:target="_blank" .link}
- [https://github.com/advisories/GHSA-8hqg-whrw-pv92](https://nvd.nist.gov/vuln/detail/CVE-2024-37032){:target="_blank" .link}


### 요약
지난 6월 Ollama에서 CVE-2024-37032 취약점이 확인됐습니다.
보안 업체 위즈(Wiz)는 이를 발견하여 Probllama로 명명하여 추적 중에 있습니다.
모델 경로를 가져올 때 digest 형식에 유효성 검사를 하지 않아 발생하는 문제로 0.1.34 이후 버전으로는 관련 문제가 발생하지 않습니다.
{: .h3_box}

Probllama: Ollama Remote Code Execution Vulnerability (CVE-2024-37032) – Overview and Mitigations
WIZ에서 작성한 위 블로그 글에 이번 취약점에 대한 자세한 설명과 관련 타임라인 등이 나와있습니다.
{: .h3_box}

### 원문
Ollama before 0.1.34 does not validate the format of the digest (sha256 with 64 hex digits) when getting the model path, and thus mishandles the TestGetBlobsPath test cases such as fewer than 64 hex digits, more than 64 hex digits, or an initial ../ substring.
{: .h3_box}

#### 참고
* [https://m.boannews.com/html/detail.html?idx=130827](https://m.boannews.com/html/detail.html?idx=130827){:target="_blank" .link}
* [https://ethicalhacking.uk/a-deep-dive-into-cve-2024-37032-ollama-rce-vulnerability/#gsc.tab=0](https://ethicalhacking.uk/a-deep-dive-into-cve-2024-37032-ollama-rce-vulnerability/#gsc.tab=0){:target="_blank" .link}
{: .fs-3 .h4_box }



## 국내외 오픈소스 소송 동향 분석
- 다운로드 : [https://www.iitp.kr/kr/1/knowledge/periodicalViewA.it?masterCode=publication&searClassCode=B_ITA_01&identifier=1327](https://www.iitp.kr/kr/1/knowledge/periodicalViewA.it?masterCode=publication&searClassCode=B_ITA_01&identifier=1327){:target="_blank" .link}

### 내용
2000년 이후 진행 되었던 주요한 30개의 사례 정리
{: .h3_box}
#### 국내사례
- 엘림넷 v. 하이온넷 소송 : 라이선스 위반이 아니라 영업비밀 보호 위반으로 결론
- 삼성이 BusyBox에 의해 소송당함  : 패소하였고 손해배상
- 한컴이 Artifex에 의해 소송 : 당사자 간 합의 종결. 한컴이 GS 사용 중지 및 23억 원 정도 손해배상
{: .h4_box}

### 요약
- 2000년대 이후 오픈소스 사용으로 인한 소송이 지속적으로 발생
- (초기) FSF, Gpl-violations.org 등의 비영리 기관에서 오픈소스 라이선스 준수 없이 상업적으로 활용하는 경우들에 대해 소송을 제기하기 시작
- (2010년대) 오픈소스 확산에 따라 소송건수도 증가하고 위반 라이선스도 다양해짐
- (2020년대) AI 기술이 오픈소스와 결합하면서 AI 모델에 대한 분쟁 발생, 오픈소스 특성으로 인해 제 3자에 의한 저작권침해 소송도 발생
{: .h3_box}



## 정부, 소프트웨어 공급망 보안 지침(가이드라인) 1.0 발표 (2024.05.12)
부제 : 소프트웨어 공급망 보안 국제동향 및 소프트웨어 구성명세서(SBOM) 활용사례
- [https://www.msit.go.kr/bbs/view.do;jsessionid=mQdTP8pS7R_JdfMcMj1x2rIT63MtNYOusm7Zs2a2.AP_msit_2?sCode=user&mPid=238&mId=113&bbsSeqNo=94&nttSeqNo=3184474](부제 : 소프트웨어 공급망 보안 국제동향 및 소프트웨어 구성명세서(SBOM) 활용사례
https://www.msit.go.kr/bbs/view.do;jsessionid=mQdTP8pS7R_JdfMcMj1x2rIT63MtNYOusm7Zs2a2.AP_msit_2?sCode=user&mPid=238&mId=113&bbsSeqNo=94&nttSeqNo=3184474){:target="_blank" .link}

### 내용
#### 추진배경
* 악성코드 및 보안취약점의 전파가 쉬운 공개 SW에 대한 사이버 위협 증가 
  * Log4j 2 보안 취약점 사태 (Log4Shell)
  * 2024 XZ Open Source Attack 
* 공급망 공격은 피해가 광범위하고 지속적인 특징 
* 미국, 유럽 등은 SW 구성요소 명세서(SBOM, SW Bill of Materials) 도입 등 제도화 추진
{: .h4_box}

#### SW 공급망 위험관리 방안
SW 개발-공급(유통)-운영 등 공급망 각 단계에서 SBOM을 활용함으로써 SW 구성요소를 안전하게 관리할 수 있으며, SBOM을 활용하여 SW 자산관리, 공개 SW 라이선스 및 보안취약점 관리가 가능
{: .h4_box}

#### SBOM 기반 SW 공급망 보안 실증 사례
SBOM 유효성 검증, SW 구성요소 관리 요령 및 SBOM 기반 SW 공급망 보안 관리 방안 등을 상세하게 수록
{: .h4_box}

#### SBOM 기반 SW 공급망 보안 활성화 지원
기업들의 애로사항을 해결하기 위해 정부는 SBOM 기반 SW 공급망 보안 관리체계를 구축하고 기업 지원 서비스를 제공
{: .h4_box}
* 기업지원허브, 판교  : 사이버보안 위협시연, 보안취약점 점검지원
* 디지털헬스케어 보안 리빙랩, 원주 : 사이버보안 위협시연, 보안취약점 점검지원, (의료기기 인허가 지원)
* 국가사이버안보협력센터 기술공유실, 판교 : 공급망 보안 테스트베드 시범운영
{: .h4_box}

#### 향후
정부는 기업들에 대한 SBOM 적용 지원을 강화하면서 SW 공급망 보안 저변을 확대하고,
향후 주요국의 제도화 동향과 국내 산업 성숙도를 고려하며 점진적으로 제도화를 준비해나갈 방침
{: .h4_box}

올해 하반기에는 산·학·연 전문가들이 참여하는 범정부 합동TF를 구성
세부적인 정부지원 방안, 제도화 추진방향 등에 대한 심도 있는 논의를 진행한 후 ‘SW 공급망 보안 로드맵’을 마련할 계획
{: .h4_box}




## XZ Open Source Attack : 오픈소스 커뮤니티의 신뢰를 이용한 최초의 공급망 공격 사례
- [XZ Utils 백도어 악성코드, 2021년부터 공들여 준비해온 공급망 공격이었다](https://www.boannews.com/media/view.asp?idx=128372){:target="_blank" .link}


### 내용
- [CVE-2024-3094 Detail - NVD](https://nvd.nist.gov/vuln/detail/CVE-2024-3094){:target="_blank" .link} (2024-03-28)
- 2년 넘게 "Jia Tan"이라는 공격자가 XZ 오픈소스 프로젝트에 성실하고 효과적인 기여자로 활동하여 최종적으로 커밋 권한과 관리자 권한을 부여받음.
- 그 권한을 사용하여 Debian, Ubuntu, Fedora 및 기타 systemd 기반 Linux 시스템에서 OpenSSH sshd의 종속성이기도 한 xz의 일부인 liblzma에 매우 미묘하고 주의 깊게 숨겨진 백도어를 설치함. : XZ Utils 5.6.0 및 5.6.1
{: .h3_box}

#### 공격 타임라인
- (원문) Timeline of the xz open source attack
- (한글) https://news.hada.io/topic?id=14122
{: .h4_box}

#### 시사점
- 오픈소스 프로젝트의 거버넌스와 관리에 대한 재고 (악의적인 기여를 어떻게 막을 것인가?)
- 보안감사 및 코드 리뷰의 중요성
{: .h4_box}



## 2023년 오픈소스 동향 그리고, 2024년

### 요약
오픈소스는 2023년에도 [GitHub 개발자 1억명](https://github.blog/2023-01-25-100-million-developers-and-counting/){:target="_blank" .link} (3억건 이상의 기여) 돌파하는 등 크게 성장하고 있습니다.
2023년 오픈소스의 가장 큰 이슈는 2가지로 요약할 수 있을 것 같습니다.
{: .h3_box}
- 생성형 AI의 폭발적인 성장
- 기업의 오픈소스 라이선스 정책 변화
{: .h3_box}


### 내용
#### 생성형 AI의 폭발적인 성장

ChatGPT(OpenAI)를 시작으로 LLaMa(Meta), Bard(Google), Ferret(Apple) 등 생성형 AI 모델이 출시되면서 오픈소스 프로젝트를 이끌고 있습니다. <br>
"[생성 AI 글로벌 시장, 5년 뒤 77조로 확대...10배 성장](https://www.aitimes.com/news/articleView.html?idxno=155010){:target="_blank" .link}" 예측도 나왔습니다.<br>
{: .h4_box}

##### [Octoverse: The state of open source and rise of AI in 2023](https://github.blog/2023-11-08-the-state-of-open-source-and-ai/){:target="_blank" .link}
{: .h4_box}
- 오픈소스 생성형 AI 프로젝트가 2023년 기여자 수 기준 가장 인기 있는 오픈소스 프로젝트 상위 10위 안에 진입
- 대부분의 개발자(92%)가 사용하거나 실험중, . AI 코딩 도구를 통해 오픈 소스 개발자가 GitHub에서 차세대 AI 혁신을 주도할 것으로 기대
{: .h4_box}

#####  [The best open source software of 2023](https://www.infoworld.com/article/3709196/the-best-open-source-software-of-2023.html){:target="_blank" .link}
- 프로그래밍 언어, 런타임, 앱 프레임워크, 데이터베이스, 분석 엔진, 기계 학습 라이브러리, LLM(대형 언어 모델), LLM 배포 도구 포함
{: .h4_box}

##### (23년 12월) EU, 'AI 법' 잠정 합의 : 오픈 소스 예외 인정
{: .h4_box}

- [EU 'AI 법' 합의 돌파구는 오픈 소스 모델 규제 면제](https://www.aitimes.com/news/articleView.html?idxno=155752){:target="_blank" .link}, 2023년12월8일 
  - 유럽연합(EU)이 세계 최초의 인공지능(AI) 규제 프레임워크인 'AI 법'에 대해 오픈소스 인공지능(AI) 모델에 대하여서는 규제 면제 안으로 잠정 합의에 도달하였습니다. '챗GPT'나 '바드'와 같은 GPAI를 다른 일반 모델과 달리 강력하게 규제하되, 오픈 소스의 경우는 제외한다는 내용입니다.
- 내년 초 발효 예정, 실제 적용은 2년 정도 소요될 듯
- EU의 AI 법이 최종 합의될 경우 글로벌 AI 규제의 기준이 될 가능성이 높다는 분석
- [EU, 'AI 법' 잠정 합의...오픈 소스 이어 생체 인식도 예외 인정](https://www.aitimes.com/news/articleView.html?idxno=155765){:target="_blank" .link}
- [EU AI 법, 美빅테크 겨냥… AI 생태계 놓고 ‘글로벌 대전’](https://www.lawtimes.co.kr/news/194074){:target="_blank" .link}
{: .h4_box}

#### 기업의 오픈소스 라이선스 정책 변화
클라우드, AI 등 IT서비스 시장이 급변하고 오픈소스 기업간의 경쟁이 심화됨에 따라 Red Hat, HashiCorp, Meta 등의 기업들이 오픈소스 라이선스 정책 변경을 통해 방어 가능한 경제 모델 유지 및 지속 가능한 성장을 추구하고 있습니다.<br>
참고) [기업은 왜 오픈소스 라이선스 정책을 변경하는가?](https://www.oss.kr/index.php/oss_guide/show/0591b468-522c-4170-943d-8a1df5af81c9){:target="_blank" .link} - OpenUp-<br>
{: .h4_box}

##### [Furthering the evolution of CentOS Stream](https://www.redhat.com/en/blog/furthering-evolution-centos-stream){:target="_blank" .link}, 2023년6월21일
- Red Hat Enterprise Linux(RHEL) 과 관련된 공개 코드는 CentOS Stream 저장소에만 공유
  “가치를 추가하거나 어떤 식으로든 변경하지 않고 단순히 코드를 다시 빌드하는 것은 모든 오픈 소스 회사에 실질적인 위협이 됩니다.” - 마이크 맥그라스 부사장
- 오라클·수세·CIQ, 反레드햇 협회 결성, 2023년8월11일
{: .h4_box}

##### [HashiCorp adopts Business Source License](https://www.hashicorp.com/blog/hashicorp-adopts-business-source-license){:target="_blank" .link} , 2023년8월10일
- Terraform, Vault의 라이선스가 MPL-2.0 에서 BUSL-1.1 로 변경
  - “하시코프의 기술을 상업적 목적으로 활용하면서 실질적인 기여를 제공하지 않는 다른 공급업체 때문에 라이선스를 변경합니다.” -  아르몬 다드가 CTO(하시코프 공동설립자)
{: .h4_box}

 
##### OSI blog: [Meta's LLaMa 2 license is not Open Source](https://blog.opensource.org/metas-llama-2-license-is-not-open-source/){:target="_blank" .link}
- Meta도 AI 언어모델인 LLAMA 를 공개하면서 오픈소스라고 하고 있지만, [LLAMA 2 라이선스](https://github.com/facebookresearch/llama/blob/main/LICENSE){:target="_blank" .link}에서 다른 언어모델을 개선하기 위해서는 사용 불가, 액티브 사용자가 7억(700 million)이상이면 메타에 라이선스 획득 필요 와 같은 제한 조건을 두고 있어서 오픈소스로 인정되지 않았습니다.
{: .h4_box}

##### 참고
- [[기술블로그] 오픈소스 라이선스 변화의 흐름](https://tech.kakao.com/2021/09/08/opensource-license/){:target="_blank" .link}: Free Software -> Open Source Software -> Shared Source Software
- [오픈소스, 라이선스, 분쟁... 그리고 포크 파티(?)](https://skkuding.dev/post/opensource-license/){:target="_blank" .link}
{: .fs-3 .h4_box }

#### 2024년 AI와 오픈소스 전망
2024년에도 AI와 함께 오픈소스의 성장이 함께할 것으로 전망되고 있습니다.
{: .h4_box}

##### [올해 출시될 프론티어급 LLM 10여개..."라마 3, GPT-4 능가할 수도"](https://www.aitimes.com/news/articleView.html?idxno=156300){:target="_blank" .link}
- 구글 '제미나이'는 헌법적 AI로 주목받을 것
- 메타 '라마 3'는 GPT-4의 성능을 따라잡고, 능가할 수도 있을듯
{: .h4_box}


##### [엔비디아, 2024년 AI 산업 전망 발표…“모든 것의 중심에는 LLM이 있다”](https://www.itworld.co.kr/news/317153#csidx11c193277e97932927669fb6599649d){:target="_blank" .link}
- 엔비디아 엔터프라이즈 컴퓨팅 부문 부사장인 마누비르 다스는 2024년 AI의 전반적인 산업 전망으로 ▲맞춤형 솔루션 필요 ▲오픈소스 소프트웨어 주도 ▲상용 AI와 마이크로서비스를 꼽았습니다.
{: .h4_box}

##### [2023년 AI시장 달군 ‘LLM’…2024년은 ‘활용’이 핵심](https://www.ejanews.co.kr/news/articleView.html?idxno=320170){:target="_blank" .link}
- 대화형 AI 기술기업인 스켈터랩스는 “올해는 ‘AI실용주의’라는 키워드가 더욱 중요시되는 해가 될 것”이라며 “2020년에는 GPT를 비롯한 LLM 개발의 서막이 오르고 지난해는 LLM의 다양화 및 고도화, 생성형 AI 출시 및 서비스 도입이 시작된 한 해라면 올해는 생성형AI 서비스가 산업 전반은 물론 실생활에서 본격적으로 널리 ‘활용’되는 시대가 열리게 될 것”이라 전망했습니다.
{: .h4_box}

##### [오픈 소스, 반년 새 폐쇄형 LLM 턱밑까지 성능 추격](https://www.aitimes.com/news/articleView.html?idxno=155196){:target="_blank" .link}
- 오픈 소스 모델의 정확도는 아직 프라이빗에 못 미치지만 정확도 증가 추세는 프라이빗보다 훨씬 빠름 
- 메타의 경우 지난 3월 '라마 65B'의 정확도 63.4%를 불과 4개월 만에 5.5%나 끌어 올렸으며 아랍에미리트(UAE)의 LLM '팰컨 180B'는 70.4%로 라마 2를 능가하는 등 다양한 개발자 그룹의 기여로 성장
{: .h4_box}

#### 참고
* {:target="_blank" .link}
  {: .fs-3 .h4_box }
