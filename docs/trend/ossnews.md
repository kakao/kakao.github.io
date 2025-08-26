---
layout: default
title: 오픈소스 뉴스
parent: 오픈소스 동향
#has_children: true
nav_order: 1
---
# {{ page.title }}
<div class="summary">
이 가이드에서는 오픈소스의 최신 동향을 알아봅니다.
</div>
• [EU Cyber Resilience Act(CRA) 발효]({{page.url}}#eu-cyber-resilience-actcra-발효) <i>2025-07-15</i><br>
• [“오픈소스가 AI 오케스트레이션의 핵심” 마이크로소프트 CEO]({{page.url}}#오픈소스가-ai-오케스트레이션의-핵심-마이크로소프트-ceo) <i>2025.05.02</i><br>
• [AI 모델을 위한 OpenMDW 라이선스]({{page.url}}#ai-모델을-위한-openmdw-라이선스) <i>2025.04.20</i><br>
• [생성형 AI와 오픈소스: 주요 모델의 OSAID 1.0 기준 분석]({{page.url}}#생성형-ai와-오픈소스-주요-모델의-osaid-10-기준-분석) <i>2025-02-24</i><br>
• [미국 법원 “AI 학습에 콘텐트 무단 이용, 저작권법 위반"]({{page.url}}#미국-법원-ai-학습에-콘텐트-무단-이용-저작권법-위반) <i>2025.02.14</i><br>
• [Google, 소프트웨어 구성 분석을 위한 오픈소스 라이브러리 출시]({{page.url}}#google-소프트웨어-구성-분석을-위한-오픈소스-라이브러리-출시) <i>2025.01.17</i><br>
• [SPDX 3.0의 주요 변화 소개]({{page.url}}#spdx-30의-주요-변화-소개) <i>24.10.04</i><br>
• [ElasticSearch, 3년 반만에 오픈소스로 복귀]({{page.url}}#elasticsearch-3년-반만에-오픈소스로-복귀) <i>2024.09.05</i><br>
• [리눅스 재단의 오픈소스 AI 모델의 가능성]({{page.url}}#리눅스-재단의-오픈소스-ai-모델의-가능성) <i>2024.08.14</i><br>
• [깃허브 코파일럿 소송, 미국 법원에서 기각]({{page.url}}#깃허브-코파일럿-소송-미국-법원에서-기각) <i>2024.07.10</i><br>
• [오픈소스 인공지능 인프라 Ollama에서 확인된 취약점: Probllama]({{page.url}}#오픈소스-인공지능-인프라-ollama에서-확인된-취약점-probllama) <i>2024-05-31</i><br>
• [국내외 오픈소스 소송 동향 분석]({{page.url}}#국내외-오픈소스-소송-동향-분석) <i>2024-07-24</i><br>
• [정부, 소프트웨어 공급망 보안 지침(가이드라인) 1.0 발표 (2024.05.12)]({{page.url}}#정부-소프트웨어-공급망-보안-지침가이드라인-10-발표-20240512) <i>2024.05.12</i><br>
• [XZ Open Source Attack : 오픈소스 커뮤니티의 신뢰를 이용한 최초의 공급망 공격 사례]({{page.url}}#xz-오픈소스-공격-최초의-공급망-공격-사례) <i>2024-03-28</i><br>
• [2023년 오픈소스 동향 그리고, 2024년]({{page.url}}#2023년-오픈소스-동향-그리고-2024년)<br>

----

## EU Cyber Resilience Act(CRA) 발효
[https://openssf.org/blog/2025/07/15/new-cyber-resilience-act-cra-brief-guide-for-oss-developers/](https://openssf.org/blog/2025/07/15/new-cyber-resilience-act-cra-brief-guide-for-oss-developers/){:target="_blank"}

## 요약
최근 EU에서 디지털 요소를 포함한 제품의 보안 수준을 법적으로 요구하는 Cyber Resilience Act(CRA)가 공식 발효되었습니다. CRA는 디지털 요소가 포함된 대부분의 하드웨어 및 소프트웨어 제품(Product with Digital Elements, PDE)에 대해 Secure by Design and by Default 원칙을 요구하며, 전체 제품 수명주기 동안 사이버보안 요구사항을 부여하는 규제입니다.

## 내용

CRA는 유럽 내 유통되는 EU 시장에  판매·배포되는 모든 디지털 제품·소프트웨어를 대상으로 하며, 이를 위반할 경우 최대 €15M 또는 전년도 전세계 매출의 2.5% 중 더 높은 금액의 과징금이 부과될 수 있습니다.
* 2026년 9월 11일부터: CRA의 보안 사고 보고, 취약점 공개 체계 등 일부 의무사항 적용
* 2027년 12월 11일부터: 전체 적용 시작

비영리 목적의 오픈소스 소프트웨어는 원칙적으로 CRA 적용 대상에서 제외되지만, 다음과 같은 경우 규제 대상이 될 수 있습니다.
* 상업적으로 배포되거나,
* 제품(PDE)에 통합되어 유통되는 경우

CRA의 주요 요구사항은 다음과 같습니다.
* SBOM(Software Bill of Materials) 작성 및 유지 의무화 (형식은 SPDX 3.0 / CycloneDX 권장)
* 제품 내 보안 취약점 관리 및 EU 보안기관 보고 체계 구축 
* 제품 출시 이후 최소 5년간 보안 업데이트 무상 제공 (이보다 짧은 기간을 적용하려면 명확히 사전 고지)
* 전체 공급망에 걸친 보안 책임 및 통제 체계 문서화

CRA 전체 조문 및 시행 세부 내용은 [EU 공식 문서](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A32024R2847){:target="_blank"}에서 확인할 수 있습니다.<br>
그리고 디지털 제품 라이프사이클 전반에 걸쳐 사이버보안을 법적 의무로 강제하고, 보안 설계·업데이트·취약점 보고까지 포괄하는 포괄형 규제는 글로벌 최초라고 합니다.

----

## “오픈소스가 AI 오케스트레이션의 핵심” 마이크로소프트 CEO
[https://www.itworld.co.kr/article/3975922/오픈소스가-ai-오케스트레이션의-핵심-마이크로.html](https://www.itworld.co.kr/article/3975922/오픈소스가-ai-오케스트레이션의-핵심-마이크로.html){:target="_blank"}

## 요약
최근 메타의 라마콘 개발자 행사에서 MS 나델라와 메타의 마크주커버그와의 대담에서 아래와 같은 내용이 논의되었다고 합니다.<br>
AI 성능 개선 속도가 매우 빠르게 향상되고, 코드의 30%이상이 AI로 작성되고 있다고 합니다.

## 내용
마이크로소프트 CEO 나델라는 AI 오케스트레이션 기술이 충분히 발전했으며, 오픈소스가 이 발전의 핵심 요소라고 강조했습니다.<br>
현재 AI 성능은 6-12개월마다 10배씩 향상되고 있으며, 지식 증류 기술을 통해 대형 모델의 90-95% 지능을 훨씬 효율적으로 구현할 수 있게 되었습니다.<br>
나델라는 마이크로소프트 코드의 최대 30%가 AI로 작성되었다고 밝혔고, 주커버그는 1년 내 소프트웨어 개발의 절반이 AI로 이뤄질 것이라고 전망했습니다.<br>
데이터브릭스 CEO는 장기적으로 모든 것이 오픈소스로 이동할 것이라고 예측했으며, 오픈소스가 AI 발전을 가속화하는 핵심 동력이라고 설명했습니다.<br>
업계 리더들은 현재를 AI 시대의 시작점으로 보며, 앞으로 더욱 흥미진진한 혁신이 이어질 것이라고 전망했습니다.<br>

----

## AI 모델을 위한 OpenMDW 라이선스
[https://github.com/OpenMDW/OpenMDW/blob/main/1.0/LICENSE.openmdw](https://github.com/OpenMDW/OpenMDW/blob/main/1.0/LICENSE.openmdw){:target="_blank"}

### 요약
AI 모델을 위한 OpenMDW 라이선스 (A permissive license specifically crafted for machine‑learning models)

OpenMDW(Open Model Definition and Weights License)는 2025년 5월, Linux Foundation에서 발표되었으며,
머신러닝 모델과 관련된 다양한 구성 요소(Model Materials)를 포괄적으로 다루는 허용적(permissive) 오픈소스 라이선스입니다.

### 내용
- AI 모델 전체를 포괄 : 모델 구조, 가중치, 관련 데이터, 문서, 소프트웨어 등 다양한 요소(Model Materials)에 대해 적용 가능 
- 재배포 시 출처 명시 의무:원 저작자 및 OpenMDW 라이선스 고지 필수 
- 출력물 자유 : 모델이 생성한 출력물(output)은 라이선스 적용 대상이 아니며 자유롭게 사용 가능 
- 사용자 책임 명시: 데이터셋 등 포함된 구성 요소의 법적 권리는 사용자가 직접 확인하고 책임져야 함 
- 특허 소송 시 라이선스 종료: 수혜자가 모델에 대해 특허 소송을 제기할 경우, 해당 라이선스는 자동 종료됨

AI 모델을 안전하고 투명하게 공유할 수 있도록 설계된 허용적인 라이선스입니다.<br>
다만,  학습 데이터가 포함된 경우, 해당 데이터에 제3자의 저작권, 개인정보, 계약 제한이 있을 수 있습니다.<br>
→ 라이선스 적용 여부와 무관하게 사용자가 별도로 확인해야 합니다.<br>
{: .h4_box}

#### 기존 오픈소스 라이선스와의 차이점
기존 오픈소스 라이선스는 "소스코드 중심"으로 설계되어 AI 모델의 비코드 요소(데이터, 가중치, 출력물 등)에 대해 라이선스 효력의 불확실성 이 있었습니다. <br>
OpenMDW 라이선스는 모든 구성 요소를 공개해야 한다는 의무 없이 코드, 데이터, 가중치, 메타데이터 및 문서를 포괄하여 라이선스 적용 대상으로 하여, AI 모델 공유의 법적 명확성을 확보 합니다.

>  **참고하기**
>
> * [penMDW 공식 웹사이트](https://openmdw.ai/){:target="_blank"}
> * [FAQ](https://openmdw.ai/faq){:target="_blank"}  
{: .h5_box}


----

## 생성형 AI와 오픈소스: 주요 모델의 OSAID 1.0 기준 분석
[생성형 AI와 오픈소스 : 주요 모델의 OSAID 1.0 기준 분석](https://www.oss.kr/oss_guide/show/c183d6f6-7530-4097-bc23-cc1c43d5a3fe){:target="_blank"}

### 요약
생성형 AI 기술의 접근성과 활용성을 높이는 오픈소스 AI 생태계에 대해 다루고 있습니다.
또한, 앞으로 오픈소스 AI 생태계가 생성형 AI 기술 발전에 중요한 역할을 하고 있으며, 더 많은 기업들이 이러한 흐름에 동참할 가능성이 높아지고 있다고 예측하고 있습니다.

### 내용

- 오픈소스 AI 모델의 부상 
  - 중국 스타트업 딥시크(DeepSeek)가 DeepSeek-R1 모델을 오픈소스로 공개함에 따라, 기업들의 오픈소스 전략 채택 가능성 증가
{: .h3_box}
- 주요 생성형 AI 모델 분석 (OSAID 1.0 기준)
  - Mixtral 8x7과 DeepSeek-R1 모델이 가장 많은 오픈소스 조건을 충족 
  - Stable Diffusion 3.5와 Llama 3.1 모델은 일부 요건만 충족
{: .h3_box}

- 기업의 오픈소스 전략 채택 이유 
  - 개발 비용 절감 
  - 연구 효율성 향상 
  - 다양한 연구 커뮤니티 및 개발자 참여를 통한 기술 발전 가속화
{: .h3_box}

- 오픈소스 AI 정의 1.0의 주요 기준 및 필수 요소 
  - 자유: 사용, 연구, 수정 및 개선, 공유의 자유 
  - 공개 정보: 데이터, 코드, 매개변수 정보
{: .h3_box}

----
## 미국 법원 “AI 학습에 콘텐트 무단 이용, 저작권법 위반”
[https://www.joongang.co.kr/article/25313874](https://www.joongang.co.kr/article/25313874){:target="_blank"}

### 요약
미국 법원이 AI 개발을 위한 무단 저작물 활용이 저작권법 위반이라는 판결을 내렸습니다.

Thomson Reuters vs. Ross Intelligence
- **쟁점**: AI가 법률 콘텐츠를 학습하는 것이 저작권법 위반인지 여부
- **사건 개요**: 법률 연구 AI 스타트업 **Ross Intelligence**가 Thomson Reuters의 법률 데이터베이스 **Westla**w의 콘텐츠를 무단으로 사용해 AI를 학습시켰다는 이유로 소송을 당함.
- **결과**: 미국 법원은 AI 학습을 위한 무단 사용이 저작권법 위반이라고 판결.(공정이용 아님)

### 내용
- **사건 개요** 
  - 톰슨 로이터(Thomson Reuters)는 AI 법률 검색 스타트업 로스 인텔리전스(Ross Intelligence)가 **자사의 법률 데이터(Westlaw)를 동의 없이 AI 학습에 사용했다**며 소송을 제기. 
  - **로스 인텔리전스의 반박**: Westlaw의 판결문 요약(헤드노트)을 AI 훈련 데이터로 사용했으므로 **공정 이용(fair use)**에 해당한다고 주장. 
- **법원 판결** 
  - 법원은 로스 인텔리전스의 AI 서비스가 Westlaw와 **직접 경쟁**하며, **대량의 데이터를 변형 없이 사용**했기 때문에 공정 이용에 해당하지 않는다고 판단. 
  - 이는 **AI 학습과 저작권법 사이의 공정 이용 원칙을 다룬 최초의 주요 판례**로 평가됨. 
- **향후 영향** 
  - AI 모델은 그동안 책, 기사, 웹사이트 등 저작권이 있는 콘텐츠를 학습해왔으며, AI 기업들은 이를 공정 이용이라고 주장해왔음. 
  - 하지만 이번 판결이 다른 유사 소송에서도 인용될 경우, AI 기업들이 저작권 문제로 불리한 상황에 처할 가능성이 커짐. 
  - 로스 인텔리전스가 항소할 가능성이 높으며, 결과에 따라 향후 생성 AI 관련 소송에도 영향을 미칠 것으로 예상. 
- **관련 소송 사례** 
  - 뉴욕타임스(NYT)는 오픈AI에, 미국의 주요 일간지 8곳은 마이크로소프트(MS)에 관련 소송 
    - [오픈AI, 미국 8개 신문사로부터 저작권 소송...변호사 30여명 ... ](https://www.aitimes.com/news/articleView.html?idxno=159263){:target="_blank"}
  - 국내에서도 지난달 지상파 3사가 “네이버가 생성 AI 하이퍼클로바X에 학습에 기사를 무단으로 썼다”며 소송 제기 
    - [지상파 3사, 네이버에 뉴스데이터 저작권 침해 소송](https://www.etnews.com/20250113000399){:target="_blank"}

AI 모델의 학습을 위한 저작권 자료 사용에 대한 법적 논쟁은 계속되고 있으며, 이러한 판결들은 향후 AI 개발과 저작권 보호 간의 균형을 어떻게 맞출 것인지에 대한 중요한 선례가 될 것으로 보입니다.

----

## Google, 소프트웨어 구성 분석을 위한 오픈소스 라이브러리 출시
[https://www.securityweek.com/google-releases-open-source-library-for-software-composition-analysis/](https://www.securityweek.com/google-releases-open-source-library-for-software-composition-analysis/){:target="_blank"}

### 요약
구글은 OSV-SCALIBR(Software Composition Analysis LIBRary)라는 오픈소스 소프트웨어 구성 분석(SCA) 라이브러리를 발표했습니다. 이 도구는 Go 언어로 작성된 파일 시스템 스캐너로, 소프트웨어 구성 정보 추출과 취약점 식별을 지원합니다.

**주요 기능**
- 취약점 스캐닝 기능 제공
- SPDX 및 CycloneDX 형식의 SBOM(소프트웨어 자재 명세서) 생성
- 독립 실행형 바이너리로 사용하거나 Go 프로젝트에 라이브러리로 통합 가능
- Linux, Windows, macOS에서 패키지, 바이너리, 소스 코드 스캔 가능
- 다양한 프로그래밍 언어의 아티팩트 및 잠금 파일(lockfile) 스캔 지원

### 내용
OSV-SCALIBR는 소프트웨어 추출 및 취약점 탐지를 위한 플러그인 기반 아키텍처를 사용하며, 기본 제공 플러그인은 독립 실행형 바이너리로 실행될 때 자동으로 활성화됩니다. 또한 사용자 정의 플러그인도 지원합니다.

**구글 내 활용 및 통합 계획**
- 내부 활용: 구글에서 라이브 호스트, 코드 저장소, 컨테이너를 대상으로 SCA 작업에 사용되며, SBOM 생성 및 취약점 탐지를 통해 데이터 보호에 기여.
- 통합 및 확장: OSV-Scanner와 통합 중이며, 향후 설치된 패키지 추출, SBOM 생성, 약한 자격 증명 스캔 기능 추가 예정.
- **OSV-Scanner V2 발표 예정**: OSV-SCALIBR가 주요 인터페이스로 발전하며, 기존 사용자도 하위 호환성을 유지하면서 계속 사용할 수 있음.

참고 : [OSV-Scanner 발표 (2022년 12월 13일)](https://security.googleblog.com/2022/12/announcing-osv-scanner-vulnerability.html){:target="_blank"}



----

## SPDX 3.0의 주요 변화 소개

### 요약
SPDX(Software Package Data Exchange)는 소프트웨어와 오픈소스 구성 요소의 라이선스 및 보안 정보를 표준화하여 관리할 수 있게 해주는 스펙입니다. 이번에 발표된 3.0 버전은 오픈소스 및 라이선스 관리에서 더 효과적이고 유연하며, 폭넓은 활용을 가능하게 하는 주요 변화를 포함하고 있습니다.
1. **JSON-LD 형식 지원**: SPDX 3.0은 JSON-LD 형식을 도입해 데이터의 문맥(@context)을 명확히 정의하고 링크 데이터를 통해 다른 시스템과 자동으로 연결하여 상호 운용성을 강화했습니다.
2. **확장된 데이터 모델**: 새로운 데이터 유형을 정의할 수 있는 SuperClasses를 추가해, 기존 버전보다 특정 요구에 맞는 맞춤형 데이터 관리가 가능해졌습니다.
3. **다양한 프로필 지원**: 라이선스, 보안, AI/ML, 소프트웨어 등 특정 목적에 맞는 프로필을 통해 필요한 데이터만 포함하는 효율적인 SBOM 구성이 가능해졌습니다.
4. **AI/ML 프로필**: 3번에서 언급한 프로필 중 하나로, AI 모델의 학습 데이터, 파라미터, 종속성 등을 체계적으로 관리하여 AI 프로젝트에 특화된 법적 준수성과 보안 강화를 지원합니다.

### 내용

#### JSON-LD 형식 지원
JSON-LD는 3.0 버전의 권장 포맷으로, 기존 JSON과 유사하지만, 데이터의 문맥(@context)을 정의하고 링크 데이터를 통해 다른 리소스와 연결할 수 있는 구조입니다. @context 필드는 JSON 데이터의 각 항목이 의미하는 바를 URL로 명확히 설명해 주며, 이를 통해 다양한 시스템과 통합 시 데이터 해석 오류를 줄일 수 있습니다.

아래 예시에서 name은 schema.org의 이름 속성을 가리키고, license는 SPDX에서 정의된 라이선스 링크를 참조합니다. 이를 통해 다른 시스템에서도 이 데이터가 프로젝트 이름과 라이선스를 의미하는 것으로 해석될 수 있으며, SPDX 라이선스 데이터와 자동으로 연결될 수 있습니다.
```
{
    "@context": {
        "name": "http://schema.org/name",
        "license": "https://spdx.org/licenses/"
    },
    "name": "SampleProject",
    "license": "MIT"
}
```

#### 확장된 데이터 모델
   기존 2.3 버전에서는 새로운 데이터 유형을 정의할 수 없어, 스펙에 맞지 않는 정보들을 형식에 맞춰 끼워 넣어야 했지만, 이제는 SuperClasses를 통해 특정 요구사항에 맞는 새로운 데이터 유형을 자유롭게 추가할 수 있습니다.

예를 들어, 의료 분야 소프트웨어의 SBOM을 작성할 때 HealthRecord라는 클래스를 추가할 수 있습니다. HealthRecord는 File 클래스를 상속하여 의료 데이터 파일을 정의하고, compliance와 같은 추가 필드를 통해 해당 데이터의 규정 준수 상태를 명시할 수 있습니다.
```
{
    "@type": "spdx:HealthRecord",
    "name": "PatientDataFile",
    "source": "https://healthdata.org/patient-data",
    "compliance": "HIPAA"
}
```

#### 다양한 프로필 지원
   SPDX 3.0은 프로필 개념을 도입하였습니다. 프로필은 특정 목적을 위한 데이터 모델의 집합으로, 자바의 패키지처럼 연관된 클래스들을 그룹화하여 필요한 정보를 간결하게 관리할 수 있게 해줍니다.

주요 프로필에는 소프트웨어 프로필, 라이선스 프로필, 보안 프로필, AI/ML 프로필 등이 있으며 이를 활용하여 프로젝트 요구사항에 맞는 데이터만 효율적으로 문서화할 수 있습니다.
* 보안 프로필을 활용하면 종속성 정보와 패키지 간 의존성 중심으로 SBOM을 구성해 보안 점검을 용이하게 만들 수 있습니다.
* AI/ML 프로젝트는 AI/ML 프로필을 통해 데이터세트 출처와 모델 파라미터를 문서화함으로써 AI 모델의 재현성 및 투명성을 높일 수 있습니다.

#### AI/ML 프로필
   SPDX 3.0은 AI와 머신러닝 프로젝트를 위한 AI/ML 프로필을 새롭게 도입하여, AI 시스템의 라이프사이클 전반에서 요구되는 정보들을 체계적으로 관리할 수 있게 했습니다.

아래 예시는 JSON-LD 형식으로 구성된 간단한 AI/ML 프로필 예시입니다. dataset 필드로 모델 학습에 사용된 데이터세트와 그 출처, 라이선스를 기록하며, model 필드로 모델 구조와 학습 파라미터를 포함합니다. 이로써 AI 모델의 데이터 출처와 학습 환경을 문서화하고, 법적 준수와 보안 관리에 도움을 줍니다.
```
{
  "@context": {
      "spdx": "https://spdx.dev/schema#",
      "name": "http://schema.org/name",
      "version": "http://schema.org/version",
      "dataset": "http://schema.org/Dataset",
      "model": "https://spdx.dev/schema#Model",
      "parameter": "https://spdx.dev/schema#Parameter"
  },
  "spdx:Profile": "AI/ML Profile",
  "name": "AI Model for Image Classification",
  "version": "1.0.0",
  "dataset": {
      "@type": "spdx:Dataset",
      "name": "ImageNet",
      "source": "https://www.image-net.org/",
      "license": "MIT"
   },
  "model": {
      "@type": "spdx:Model",
      "name": "ResNet-50",
      "framework": "TensorFlow",
      "parameter": [
        {
            "@type": "spdx:Parameter",
            "name": "learning_rate",
            "value": "0.001"
        },
        {
            "@type": "spdx:Parameter",
            "name": "batch_size",
            "value": "32"
        }
      ]
  }
}
```

----
## ElasticSearch, 3년 반만에 오픈소스로 복귀
[https://www.elastic.co/kr/blog/elasticsearch-is-open-source-again](https://www.elastic.co/kr/blog/elasticsearch-is-open-source-again){:target="_blank"}

### 요약
ElasticSearch가 오픈소스로 복귀합니다. 이에 향후 몇 주 내에 AGPLv3 라이선스가 추가로 적용될 예정입니다.
이는 지난 2021년에 AWS와 시작된 시작된 상표권 분쟁이 일단락되었기 때문입니다. <br><br>

양사 간 분쟁이 발생한 이유는 2015년 AWS가 ElasticSearch의 코드를 이용해 자체 매니지드 서비스 'AWS ElasticSearch 서비스'를 만든 후 유료 서비스로 제공해 왔기 때문입니다. 공개된 소스코드를 그대로 사용해 수익화할 뿐 아니라 엘라스틱의 제품명을 그대로 사용하면서 사용자들에게 혼선을 줬다는 지적입니다.

### 내용
[ElasticSearch: AGPL 3.0, Elastic License 2.0, SSPL 멀티 라이선스 적용]({{page.baseurl}}docs/license/revision/elasticSearch/){:target="_blank"}

Elastic 8.16 릴리즈부터는 ElasticSearch와 Kibana에 AGPL3.0이 추가된 AGPL 3.0, Elastic License 2.0, SSPL의 멀티 라이선스가 적용됩니다.

```
Source code in this repository is covered by (i) a triple license under the "GNU
Affero General Public License v3.0 only", "the Server Side Public License, v 1",
and the "Elastic License 2.0", or (ii) an "Apache License 2.0" compatible
license or (iii) solely under the "Elastic License 2.0", in each case, as noted
in the applicable header. The default throughout the repository is a triple
license under the "GNU Affero General Public License v3.0 only", "the Server
Side Public License, v 1", and the "Elastic License 2.0", unless the header
specifies another license. Code that is licensed solely under the "Elastic
License 2.0" is found only in the x-pack folder.
```

----

## 리눅스 재단의 오픈소스 AI 모델의 가능성
[오픈소스 AI 업계 판도 바꿀까?··· 애널리스트가 본 리눅스재단 AI 모델의 가능성](https://www.ciokorea.com/news/347512){:target="_blank"}

### 요약
기존 AI 모델은 소스 코드를 공개하거나 비공개하는 과정에서 대부분의 경우 AI 모델의 사용 정책에 제한을 두고 있습니다.<br>

리눅스 재단이 계획 중인 OMI(Open Model Initiative)는 이러한 제한 없이 자유롭게 사용할 수 있는 AI 모델을 만드는 것을 목표로 하고 있습니다.<br>
OMI는 기존 빅테크 모델보다 경쟁력이 낮을 수 있지만, [SLM\(Small Language Model\)](https://zapier.com/blog/small-language-models/?utm_source=google&utm_medium=cpc&utm_campaign=gaw-row-nua-evr-search_nb_desktop_blog_prospecting_developing1_developing2-ads&utm_term=&utm_content=9197295&utm_ads_campaign_id=19622168382&utm_ads_adset_id=157760468828&utm_ads_ad_id=659058345728&gad_source=1&gclid=CjwKCAjwl6-3BhBWEiwApN6_khfszXMIvgh6nIxnSrM1TrjytGd-UG7XTfMtCnrtCiFxScVADelB6hoCLhoQAvD_BwE){:target="_blank"} 분야에서 활용 가능성이 높을 것으로 예상됩니다.<br>


### 내용
지난 12일, 리눅스 재단이 OMI 지원 계획을 발표한 이후, 이 프로젝트가 윤리적인 LLM 개발을 주도할 것이라는 분석이 제기되고 있습니다.<br>
OMI는 기존 상용 모델과 동등하거나 더 나은 품질을 제공하면서도 사용 제한이 없는 커뮤니티 기반 LLM을 만드는 것을 목표로 합니다.<br>
>  **OMI(Open Model Initiative)란?**
>
>  OMI는 인보크(Invoke), 시비타이(Civitai) 및 컴피 오르그(Comfy Org)라는 세 개의 스타트업이 6월에 시작한 프로젝트로, 개발자, 연구자와 기업이 함께 개방적이고 허용적인 라이선스를 가진 AI 모델 기술을 만들기 위해 협력하고 있습니다.<br>  
>  리눅스 재단에 따르면, 허용적인 라이선스는 커뮤니티 구성원이 부담 없이 기여할 수 있는 환경을 조성하여, 더 많은 기업과 사람들의 참여를 유도할 수 있습니다. 이러한 접근 방식은 오픈소스를 기반으로 하는 상용 소프트웨어 개발에도 매우 유용합니다.<br>  
>  OMI 프로젝트에 대한 보다 자세한 내용은 [OMI Github Project](https://github.com/Open-Model-Initiative){:target="_blank"}를 참고합니다.
{: .div_box}


----

## 깃허브 코파일럿 소송, 미국 법원에서 기각
[깃허브 코파일럿 vs. 오픈소스 개발자 집단 소송, 개발자 측 패소](https://www.itworld.co.kr/news/343788#csidxac69a879cc30827a9dd6433f988397a){:target="_blank"}

### 요약
2022년 11월 제기된 GitHub 코파일럿 관련 소송이 샌프란시스코 지방법원에 의해 대부분 기각되었습니다.<br>
따라서, 향후 오픈소스 개발자들이 어떤 대응을 할지 지켜볼 필요가 있습니다.<br>


### 내용
6월 24일에 처음 발표되었지만, 7월 5일에야 일반 공개된 판결문에서 캘리포니아 북부 지방법원 판사 존 타이가는 **"원고의 주장은 구제책을 뒷받침하지 못했으며, 부당이득 배상에 대한 법적 근거를 입증하지 못했다"**라고 판결했습니다.<br><br>

타이가는 이어 **"법원은 원고의 1202(b) 조항 청구를 재소 불가 조건으로 기각하며, 모든 피고를 대상으로 한 오픈소스 라이선스 위반 청구도 기각한다. 또한, 부당이득금 및 징벌적 손해배상 요청도 모두 기각한다"**라고 덧붙였습니다.<br><br>


>  **참고하기 : 집단 소송 관련 뉴스**
> 
> 추가적인 집단 소송 관련 뉴스 및 동향은 아래를 참고합니다.
>* [“오픈소스로 AI 학습시키지 마” 깃허브 코파일럿, 美서 집단소송 직면](https://www.itworld.co.kr/news/264316){:target="_blank" .fs-3}
>* [한국저작권위원회의 저작권동향: 마이크로소프트 사의 GitHub Copilot, 오픈소스 관련 첫 번째 저작권 분쟁 시작](https://www.copyright.or.kr/information-materials/trend/the-copyright/viewPress.do?brdctsno=51490){:target="_blank" .fs-3}


----

## 오픈소스 인공지능 인프라 Ollama에서 확인된 취약점: Probllama
- [Ollama의 CVE-2024-37032 RCE 취약점과 관련된 리소스 및 변경 사항](https://nvd.nist.gov/vuln/detail/CVE-2024-37032){:target="_blank"}
- [Ollama의 다이제스트 검증 취약점(CVE-2024-37032) GitHub](https://github.com/advisories/GHSA-8hqg-whrw-pv92){:target="_blank"}


### 요약
지난 6월, Ollama에서 CVE-2024-37032 취약점이 발견되었습니다. 보안 업체 위즈(Wiz)가 이 취약점을 발견하고 **Probllama**로 명명해 추적 중입니다.<br>

이 취약점은 모델 경로를 가져올 때 sha256 다이제스트 형식의 유효성 검사를 하지 않아 발생하며, 0.1.34 이후 버전에서는 해당 문제가 해결되었습니다.

>  **Ollama 원격 코드 실행 취약점 해결**
>
>  위즈(Wiz)에서 작성한 [Probllama: Ollama 원격 코드 실행 취약점(CVE-2024-37032) 개요 및 해결책](https://www.wiz.io/blog/probllama-ollama-vulnerability-cve-2024-37032){:target="_blank"} 블로그 포스팅에 이번 취약점에 대한 상세 설명과 타임라인에 대한 내용이 포함되어 있습니다.
{: .div_box}

### 원문
Ollama before 0.1.34 does not validate the format of the digest (sha256 with 64 hex digits) when getting the model path, and thus mishandles the TestGetBlobsPath test cases such as fewer than 64 hex digits, more than 64 hex digits, or an initial ../ substring.


>  **참고하기**
>
>  추가적인 취약점 관련 정보는 아래를 확인합니다.  
> 
> * [오픈소스 인공지능 플랫폼 올라마에서 초고위험도 취약점 발견돼](https://www.boannews.com/media/view.asp?idx=130827){:target="_blank" .fs-3}   
> * [Ollama RCE 취약성\(CVE-2024-37032\) 심층 분석](https://ethicalhacking.uk/a-deep-dive-into-cve-2024-37032-ollama-rce-vulnerability/#gsc.tab=0){:target="_blank" .fs-3} 

----

## 국내외 오픈소스 소송 동향 분석
[정보통신기획평가원 원문](https://www.iitp.kr/kr/1/knowledge/periodicalViewA.it?masterCode=publication&searClassCode=B_ITA_01&identifier=1327){:target="_blank"}

### 요약
2000년대 이후 오픈소스 사용과 관련된 소송이 지속적으로 발생했습니다.<br>

내용을 연도로 정리하면 아래와 같습니다.

- 2000년대 초기: FSF 및 Gpl-violations.org와 같은 비영리 기관들이 상업적 이용에서 오픈소스 라이선스를 준수하지 않은 사례들에 대한 소송을 제기
- 2010년대: 오픈소스가 확산됨에 따라 소송 건수가 증가하고, 위반된 라이선스 종류도 다양화됨
- 2020년대: AI 기술과 오픈소스가 결합되면서 AI 모델 관련 분쟁 발생, 오픈소스의 특성상 제삼자에 의한 저작권 침해 소송도 증가

### 내용
2000년대 이후 발생한 주요 오픈소스 관련한 **국내 사례**는 아래와 같습니다.
{: .h3_box}

- 엘림넷 vs 하이온넷: 라이선스 위반이 아닌 영업비밀 보호 위반으로 결론
- 삼성 vs BusyBox: 삼성이 패소하였고 손해배상을 지불
- 한글과컴퓨터 vs Artifex: 당사자 간 합의로 종결, 한글과컴퓨터는 GS 사용을 중지했으며 약 23억 원을 손해배상함


----

## 정부, 소프트웨어 공급망 보안 지침(가이드라인) 1.0 발표 (2024.05.12)
[부제 : 소프트웨어 공급망 보안 국제동향 및 소프트웨어 구성명세서(SBOM) 활용사례](https://www.msit.go.kr/bbs/view.do;jsessionid=mQdTP8pS7R_JdfMcMj1x2rIT63MtNYOusm7Zs2a2.AP_msit_2?sCode=user&mPid=238&mId=113&bbsSeqNo=94&nttSeqNo=3184474){:target="_blank"}


### 요약

정부는 증가하는 소프트웨어(SW) 공급망 위협에 대응하기 위해 SBOM(SW Bill of Materials)을 활용한 보안 관리 체계를 구축하고, 기업 지원을 확대하고 있습니다. 이를 통해 SW 구성요소, 라이선스, 보안 취약점을 안전하게 관리하며, 주요국 제도화 동향에 맞춰 점진적으로 제도화를 추진할 계획입니다.<br>

또한, 올해 하반기에는 범정부 합동 TF를 구성하여 SW 공급망 보안 로드맵을 마련할 예정입니다.

### 내용
#### 추진배경
정부 차원에서 소프트웨어 공급망 보안 가이드라인을 제작 및 발표한 배경은 아래와 같습니다.<br>

* 공개 소프트웨어(SW)에 대한 사이버 위협 증가(특히 악성코드 및 보안 취약점 전파가 용이)
  * Log4j 2 보안 취약점 사태 (Log4Shell)
  * 2024 XZ 오픈소스 공격
* 공급망에 대한 공격은 피해가 광범위하고 장기적인 특성을 가져 정부 차원에서 대응 필요
* 미국, 유럽 등은 **SW 구성요소 명세서(SBOM, SW Bill of Materials)** 도입을 제도화 중


#### SW 공급망 위 험관리 방안
SW 개발, 공급(유통) 및 운영 등 각 단계에서 SBOM을 활용하여 SW 구성요소를 안전하게 관리할 수 있으며, 이를 통해 SW 자산 관리, 공개 SW 라이선스 및 보안 취약점 관리가 가능합니다.

#### SBOM 기반 SW 공급망 보안 실증 사례
SBOM의 유효성 검증, SW 구성요소 관리 방법, 그리고 SBOM을 활용한 SW 공급망 보안 관리 방안을 상세히 수록했습니다.


#### SBOM 기반 SW 공급망 보안 활성화 지원
정부는 기업들의 어려움을 해결하기 위해 SBOM 기반 SW 공급망 보안 관리 체계를 구축하고 다양한 기업 지원 서비스를 제공하고 있습니다.

* 기업지원허브, 판교: 사이버보안 위협 시연 및 보안 취약점 점검 지원
* 디지털헬스케어 보안 리빙랩, 원주: 사이버보안 위협 시연, 보안 취약점 점검 지원 및 의료기기 인허가 지원
* 국가사이버안보협력센터 기술공유실, 판교: 공급망 보안 테스트베드 시범 운영


#### 향후 계획
정부는 기업들에 SBOM 적용을 지원하며 SW 공급망 보안을 강화하고, 주요국 제도화 동향 및 국내 산업 성숙도를 고려하여 점진적으로 제도화를 추진할 예정입니다.

2024년 하반기에는 산·학·연 전문가들이 참여하는 범정부 합동 TF를 구성해, 세부적인 정부 지원 방안 및 제도화 방향에 대한 논의를 진행하고 **SW 공급망 보안 로드맵**을 마련할 계획입니다.

----

## XZ 오픈소스 공격: 최초의 공급망 공격 사례
[XZ Utils 백도어 악성코드, 2021년부터 공들여 준비해 온 공급망 공격이었다](https://www.boannews.com/media/view.asp?idx=128372){:target="_blank"}

### 요약
CVE-2024-3094는 XZ 오픈소스 프로젝트에 오랜 기간 기여한 공격자가 관리자 권한을 이용해 백도어를 설치한 사건입니다. 이 공격은 Debian, Ubuntu 및 Fedora 등의 systemd 기반 Linux 시스템에서 발견되었습니다.<br>

이 사건을 통해, 오픈소스 프로젝트의 관리 및 보안 감사의 중요성이 다시금 강조되었다고 할 수 있겠습니다.

### 내용
2024년 3월 28일, NVD에서 공개된 [CVE-2024-3094 취약점](https://nvd.nist.gov/vuln/detail/CVE-2024-3094){:target="_blank"}에 따르면, **Jia Tan**이라는 공격자가 2년 넘게 XZ 오픈소스 프로젝트에 성실하게 기여하여 커밋 및 관리자 권한을 부여받았습니다.<br>

이후 공격자는 이 권한을 이용해 Debian, Ubuntu 및 Fedora 등 systemd 기반 Linux 시스템에서 OpenSSH sshd의 종속성인 XZ의 일부인 liblzma에 백도어를 설치했습니다. 이 백도어는 XZ Utils 5.6.0 및 5.6.1 버전에서 발견되었습니다.

#### 공격 타임라인
공격자의 공격 타임라인이 정리된 문서는 아래를 참고합니다.
* [원문: Timeline of the xz open source attack](https://research.swtch.com/xz-timelinehttps://research.swtch.com/xz-timeline){:target="_blank"}
* [국문: XZ 오픈소스 공격 전체 타임라인 정리](https://news.hada.io/topic?id=14122){:target="_blank"}

#### 시사점
XZ 오픈소스 공격이 오픈소스 보안에 주는 교훈은 아래와 같습니다.<br>

* 오픈소스 프로젝트 거버넌스 및 관리 방식의 재고하여 악의적인 기여를 방지하는 방법 구축
* 보안 감사 및 코드 리뷰의 중요성 강조

----

## 2023년 오픈소스 동향 그리고, 2024년

### 요약
2023년 오픈소스는 [GitHub에 등록한 개발자가 1억 명, 기여 건수가 3억 건을 돌파하며](https://github.blog/2023-01-25-100-million-developers-and-counting/){:target="_blank"} 지속적인 성장을 보여주었습니다.<br>

2023년, 오픈소스의 주요 이슈로는 **생성형 AI의 폭발적 성장**과 **기업들의 오픈소스 라이선스 정책 변화**를 꼽을 수 있겠습니다.


### 내용
#### 생성형 AI의 폭발적인 성장

ChatGPT(OpenAI)를 시작으로 LLaMa(Meta), Bard(Google) 및 Ferret(Apple) 등의 생성형 AI 모델이 출시되며 오픈소스 프로젝트가 빠르게 발전하고 있습니다.<br>
이에 따라, [생성 AI 글로벌 시장](https://www.aitimes.com/news/articleView.html?idxno=155010){:target="_blank" .line}은 5년 안에 77조 원 규모로 성장할 것으로 전망됩니다.

##### [Octoverse: The state of open source and rise of AI in 2023](https://github.blog/2023-11-08-the-state-of-open-source-and-ai/){:target="_blank"}
- 오픈소스 생성형 AI 프로젝트는 2023년 기여자 수 기준으로 상위 10위 안에 들며 가장 인기 있는 프로젝트로 부상하였습니다.
- 개발자의 92%가 생성형 AI를 사용하거나 실험 중이며, AI 코딩 도구 영역에서 GitHub이 차세대 AI 혁신을 주도할 것으로 기대되고 있습니다.
{: .h5_box}

##### [The best open source software of 2023](https://www.infoworld.com/article/3709196/the-best-open-source-software-of-2023.html){:target="_blank"}
- 프로그래밍 언어, 런타임, 앱 프레임워크, 데이터베이스, 분석 엔진, 기계 학습 라이브러리, LLM(대형 언어 모델) 및 LLM 배포 도구 등이 2023년 최고의 오픈소스에 포함되었습니다.
{: .h5_box}

##### EU, 'AI 법' 잠정 합의: 오픈소스 예외 인정(23년 12월)
- [EU 'AI 법' 합의 돌파구는 오픈소스 모델 규제 면제](https://www.aitimes.com/news/articleView.html?idxno=155752){:target="_blank"}, 2023년 12월 8일  
  유럽연합(EU)은 세계 최초의 인공지능(AI) 규제 프레임워크인 **AI 법**에 대해 잠정 합의에 도달하였으며, 오픈소스 인공지능(AI) 모델에 대해서는 규제를 면제하기로 결정했습니다. ChatGPT나 Bard와 같은 [GPAI](https://gpai.ai/){:target="_blank"}는 강력하게 규제하지만, 오픈소스 모델은 규제 대상에서 제외됩니다.  
  해당 법은 내년 초 발효될 예정이며, 실제 적용에는 약 2년 정도가 소요될 것으로 예상됩니다. 이 법이 최종 합의될 경우, 글로벌 AI 규제의 기준이 될 가능성이 높다는 분석이 나오고 있습니다.
- 관련 기사
  - [EU, 'AI 법' 잠정 합의...오픈소스 이어 생체 인식도 예외 인정](https://www.aitimes.com/news/articleView.html?idxno=155765){:target="_blank"}
  - [EU AI 법, 美빅테크 겨냥… AI 생태계 놓고 ‘글로벌 대전’](https://www.lawtimes.co.kr/news/194074){:target="_blank"}
{: .h5_box}



#### 기업의 오픈소스 라이선스 정책 변화
클라우드와 AI 시장의 급격한 변화로 인해 Red Hat, HashiCorp 및 Meta 등은 오픈소스 라이선스 정책을 변경하여 방어 가능한 경제 모델과 지속 가능한 성장을 추구하고 있습니다.


>  **참고하기**
>
>  유명 기업들이 오픈소스 라이선스 정책을 변경하는 이유에 대한 자세한 분석은 [기업은 왜 오픈소스 라이선스 정책을 변경하는가?: OpenUp](https://www.oss.kr/index.php/oss_guide/show/0591b468-522c-4170-943d-8a1df5af81c9){:target="_blank"}을 참고합니다.

##### [Furthering the evolution of CentOS Stream](https://www.redhat.com/en/blog/furthering-evolution-centos-stream){:target="_blank"}, 2023년 6월 21일
Red Hat Enterprise Linux(RHEL) 관련 코드는 CentOS Stream 저장소에서만 공유되며, 오라클, 수세, CIQ는 반(反) Red Hat 연합을 결성하였습니다.
{: .h5_box}

> “가치를 추가하거나 어떤 식으로든 변경하지 않고 단순히 코드를 다시 빌드하는 것은 모든 오픈소스 회사에 실질적인 위협이 됩니다.”  
> \- 마이크 맥그라스 부사장
{: .div_box .h5_box}


##### [HashiCorp adopts Business Source License](https://www.hashicorp.com/blog/hashicorp-adopts-business-source-license){:target="_blank"}, 2023년 8월 10일
HashiCorp의 Terraform과 Vault는 MPL-2.0에서 BUSL-1.1 라이선스로 변경되었습니다.
{: .h5_box}

> “HashiCorp의 기술을 상업적 목적으로 활용하면서 실질적인 기여를 제공하지 않는 다른 공급업체 때문에 라이선스를 변경하게 되었습니다.”  
> \- 아르몬 다드가 CTO(하시코프 공동설립자)
{: .div_box .h5_box}

##### OSI blog: [Meta's LLaMa 2 license is not Open Source](https://blog.opensource.org/metas-llama-2-license-is-not-open-source/){:target="_blank"}
Meta는 AI 언어모델인 LLaMa를 공개하면서 이를 오픈소스라고 주장했지만, [LLaMa 2 라이선스](https://github.com/facebookresearch/llama/blob/main/LICENSE){:target="_blank"}에는 다른 언어모델을 개선하는 데 사용할 수 없고, 액티브 사용자가 7억 명 이상일 경우 Meta로부터 라이선스를 획득해야 하는 등의 제한 조건이 있어 오픈소스로 인정되지 않았습니다.
{: .h5_box}


>  **참고하기**
>
> * [[기술블로그] 오픈소스 라이선스 변화의 흐름](https://tech.kakao.com/2021/09/08/opensource-license/){:target="_blank"}: Free Software → Open Source Software → Shared Source Software
> * [오픈소스, 라이선스, 분쟁... 그리고 포크 파티(?)](https://skkuding.dev/post/opensource-license/){:target="_blank"}  
{: .h5_box}


#### 2024년 AI와 오픈소스 전망
2024년에는 여러 프론티어급 LLM이 출시될 예정이며, 오픈소스 모델은 상용 AI와의 성능 격차를 빠르게 좁혀가며 성장이 기대되고 있습니다.


##### [올해 출시될 프론티어급 LLM 10여개..."라마 3, GPT-4 능가할 수도"](https://www.aitimes.com/news/articleView.html?idxno=156300){:target="_blank"}
구글 **제미나이**는 헌법적 AI로 주목받을 것으로 예상됩니다.
구글의 **제미나이** Meta의 **LLaMa 3** 등이 GPT-4와 경쟁할 것으로 전망되고 있습니다.
{: .h5_box}

##### [엔비디아, 2024년 AI 산업 전망 발표…“모든 것의 중심에는 LLM이 있다”](https://www.itworld.co.kr/news/317153#csidx11c193277e97932927669fb6599649d){:target="_blank"}
엔비디아 엔터프라이즈 컴퓨팅 부문 부사장 마누비르 다스는 2024년 AI 산업 전망에서 아래 내용들을 강조했습니다.
{: .h5_box}

- 맞춤형 솔루션의 필요성
  - 오픈소스 소프트웨어의 주도 
  - 상용 AI와 마이크로서비스
{: .h5_box}

##### [2023년 AI시장 달군 ‘LLM’…2024년은 ‘활용’이 핵심](https://www.ejanews.co.kr/news/articleView.html?idxno=320170){:target="_blank"}
대화형 AI 기술 기업 스켈터랩스는 **“2024년은 ‘AI 실용주의’가 더욱 강조되는 해가 될 것"**이라며, **"2020년 GPT를 비롯한 LLM 개발의 시작을 알렸다면, 지난해는 LLM의 다양화 및 고도화, 생성형 AI 출시와 서비스 도입이 활발했던 해"**라고 밝혔습니다.
{: .h5_box}
또한, **"올해는 생성형 AI 서비스가 산업 전반은 물론 일상생활에서 본격적으로 널리 활용되는 시대가 될 것”**이라고 전망했습니다.
{: .h5_box}

##### [오픈 소스, 반년 새 폐쇄형 LLM 턱밑까지 성능 추격](https://www.aitimes.com/news/articleView.html?idxno=155196){:target="_blank"}
오픈소스 모델의 정확도는 여전히 프라이빗 모델에 미치지 못하지만, 정확도 증가 속도는 프라이빗 모델보다 훨씬 빠릅니다.
{: .h5_box}

Meta는 지난 3월 **LLaMa 65B**의 정확도를 63.4%에서 4개월 만에 5.5%나 끌어올렸으며, 아랍에미리트(UAE)의 LLM **팰컨 180B**는 70.4%의 정확도로 **LLaMa 2**를 능가하는 등 다양한 개발자들의 기여로 성장을 이루었습니다
{: .h5_box}
