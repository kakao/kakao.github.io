---
layout: default
title: 오픈소스 공개하기
parent: 오픈소스 기여하기
nav_order: 3
---
# {{ page.title }}
이 가이드에서 오픈소스를 공개하는 데 필요한 파일과 그 의미를 알아보고, 참고할 만한 가이드와 샘플을 소개합니다.
{: .summary }

## 오픈소스에 필요한 파일
오픈소스를 공개하는데 필요한 파일은 아래와 같습니다.<br>
<img src="https://t1.kakaocdn.net/olive/assets/images/menu-license.svg" class="check_img">[Open Source license](https://help.github.com/articles/open-source-licensing/#where-does-the-license-live-on-my-repository){:target="_blank" .line .fs-5}<br>
<img src="https://t1.kakaocdn.net/olive/assets/images/menu-license.svg" class="check_img">[README](https://help.github.com/articles/create-a-repo/#commit-your-first-change){:target="_blank" .line .fs-5}<br>
<img src="https://t1.kakaocdn.net/olive/assets/images/menu-license.svg" class="check_img">[Contributing guidelines](https://help.github.com/articles/setting-guidelines-for-repository-contributors/){:target="_blank" .line .fs-5}<br>
<img src="https://t1.kakaocdn.net/olive/assets/images/menu-license.svg" class="check_img">[Code of Conduct](https://opensource.guide/code-of-conduct/){:target="_blank" .line .fs-5}<br>

## 오픈소스 라이선스 선택하기
MIT, Apache 2.0, 그리고 GPLv3가 가장 인기있는 오픈소스 라이선스입니다. 이 외에도 사용할 수 있는 오픈소스 라이선스가 많습니다.<br>
[choosealicense.com](https://choosealicense.com/){:target="_blank" .link}에서 이러한 라이선스의 전체 텍스트 및 사용 방법에 대한 지침을 찾을 수 있습니다.<br>
혹은, GitHub와 같은 저장소는 새로운 프로젝트를 생성할 때, 템플릿(Template)을 사용해 라이선스를 추가할 것인지 물어봅니다.<br>

> **참고하기**<br>
> * [오픈소스의 법적 측면](https://opensource.guide/ko/legal/){:target="_blank" .line}
{: .fs-3 .h3_box }

## README 작성하기

README 파일을 작성할 때 아래 사항을 참고해 작성합니다.

* 이 프로젝트는 무슨 일을 하나요?
* 이 프로젝트가 유용한 이유는 무엇인가요?
* 어떻게 시작해야 하나요?
* 필요하다면 어디에서 더 많은 도움을 받을 수 있을까요?

> **참고하기**<br>
* @18F의 “[Making READMEs Readable](https://pages.18f.gov/open-source-guide/making-readmes-readable/){:target="_blank" .line}”  
* @PurpleBooth의 [README template](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2){:target="_blank" .line}
* Google Guava [README.md](https://github.com/google/guava/blob/master/README.md){:target="_blank" .line}
{: .fs-3 .h3_box}

## 기여(Contributing) 가이드라인 작성하기


기여 가이드라인을 작성할 때 아래 사항을 참고해 작성합니다.
 
* 기여자가 버그 보고서를 제출하는 방법(일반적으로 이슈와 PR 템플릿 사용을 추천합니다)
* 기여자가 새로운 기능을 제안하는 방법
* 기여자가 환경 설정 및 테스트 실행 방법
* 기술적 세부 사항과 더불어 여러분이 어떤 기여를 기대하는지 전달할 수 있습니다.
* 원하는 기여 유형
* 프로젝트 로드맵 또는 비전
* 기여자가 여러분과 연락하는 데 사용할(혹은 사용하지 말아야 할) 방법

> **참고하기**<br>
* @nayafia의 [contributing guide template](https://github.com/nayafia/contributing-template/blob/HEAD/CONTRIBUTING-template.md){:target="_blank" .line} 
* @mozilla의 “[How to Build a CONTRIBUTING.md](http://mozillascience.github.io/working-open-workshop/contributing/){:target="_blank" .line}”  
* Spring framework [CONTRIBUTING.md](https://github.com/spring-projects/spring-framework/blob/main/CONTRIBUTING.md){:target="_blank" .line}  
{: .fs-3 .h3_box}

### CLA(Contributor Licensing Agreement) 동의
CLA 동의는 오픈소스 프로젝트에 대한 기여자들로부터 오픈소스 프로젝트에 대한 관리 권한을 위임받는 것입니다. <br>
이는 저작권 및 지적재산권 소송이나 라이선스 변경 등, 주요 이슈 발생 시 대응을 위해 필요한 절차입니다.<br>
{: .h3_box}

[CLA Assistant](https://cla-assistant.io/){:target="_blank" .line}를 활용하여 CLA 동의를 받을 수 있습니다. CLA Assistant를 사용하는 방법은 아래와 같습니다.
{: .h3_box}

1. [GIST](https://gist.github.com/){:target="_blank" .line}에 CLA 생성
2. [CLA Assistant](https://cla-assistant.io/){:target="_blank" .line}에서 **Configure CLA** 버튼을 클릭 후, 적용할 저장소 및 CLA 선택 
   - CLA에 서명하지 않은 PR을 보내는 사람은 PR(Pull Request) 에 다음과 같이 메시지가 표시됩니다.
   - 컨트리뷰터(Contributor)는 **Contributor License Agreement** 링크를 클릭하면 서명할 실제 CLA로 이동할 수 있습니다. 이때, **GitHub 인증 후 동의** 절차를 진행하게 됩니다.<br>
     <img src="{{ site.baseurl }}/assets/images/cla-unsigned.png" class="my-6" width="850">
{: .h3_box}

> **참고하기**<br>
> * [카카오 오픈소스 Khaiii CLA 동의](https://cla-assistant.io/kakao/khaiii){:target="_blank" .line} 링크에서 CLA 동의 예시를 확인할 수 있습니다.
{: .fs-3 .h4_box }

## 행동 강령(Code of conduct) 수립

행동 강령을 수립할 때 아래 사항을 참고합니다.

* 건강하고 건설적인 커뮤니티를 위한 행동강령
* 참여자가 어떻게 행동하기를 기대하는지 전달하는 것 외에, 이러한 기대가 누구에게 적용되는지, 언제 적용되는지 그리고 위반할 경우 어떻게 처리되는지 등을 포함
* 행동 강령 작성 시 [오픈소스 가이드의 행동 강령](https://opensource.guide/ko/code-of-conduct/){:target="_blank"}을 참고해 작성합니다.  



> **참고하기**
> 
>* [Contributor Covenant](https://www.contributor-covenant.org/){:target="_blank" .link} - Kubernetes, Rails 및 Swift를 포함한 40,000개 이상의 오픈소스 프로젝트에서 사용되는 행동 강령
> * [Google: Code of conduct](https://github.com/google/.github/blob/master/CODE_OF_CONDUCT.md){:target="_blank" .link}
{: .fs-3 .h4_box }
