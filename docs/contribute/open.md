---
layout: default
title: 오픈소스 공개하기
parent: 오픈소스 기여하기
nav_order: 3
---
# {{ page.title }}
이 가이드에서는 오픈소스를 공개하는 데 필요한 파일과 그 의미를 알아보고, 참고할 만한 가이드와 샘플을 소개합니다.
{: .summary }

## 오픈소스에 필요한 파일`
오픈소스를 공개하는데 필요한 파일은 아래와 같습니다.<br><br>
<img src="https://t1.kakaocdn.net/olive/assets/images/menu-license.svg" class="check_img">[Open Source license](https://docs.github.com/ko/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository){:target="_blank" .fs-5}<br>
<img src="https://t1.kakaocdn.net/olive/assets/images/menu-license.svg" class="check_img">[README](https://docs.github.com/ko/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes){:target="_blank"  .fs-5}<br>
<img src="https://t1.kakaocdn.net/olive/assets/images/menu-license.svg" class="check_img">[Contributing guidelines](https://docs.github.com/ko/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors){:target="_blank"  .fs-5}<br>
<img src="https://t1.kakaocdn.net/olive/assets/images/menu-license.svg" class="check_img">[Code of Conduct](https://opensource.guide/code-of-conduct/){:target="_blank"  .fs-5}<br>

----

## 오픈소스 라이선스 선택하기
MIT, Apache 2.0, 그리고 GPLv3가 가장 인기 있는 오픈소스 라이선스입니다. 이 외에도 사용할 수 있는 오픈소스 라이선스가 많습니다.<br>
[choosealicense.com](https://choosealicense.com/){:target="_blank" }에서 이러한 라이선스의 전체 텍스트 및 사용 방법에 대한 지침을 찾을 수 있습니다. 혹은, GitHub와 같은 저장소는 새로운 프로젝트를 생성할 때, 템플릿(Template)을 사용해 특정 라이선스를 추가할 수 있습니다.<br>

> **참고하기**<br>
> * 오픈소스 라이선스 선택에 대한 자세한 내용은 [오픈소스의 법적 측면](https://opensource.guide/ko/legal/){:target="_blank" }을 참고합니다.


----

## README 작성하기

README 파일을 작성할 때 아래 사항들이 잘 설명될 수 있도록 작성합니다.

* 이 프로젝트는 무슨 일을 하나요?
* 이 프로젝트가 유용한 이유는 무엇인가요?
* 어떻게 시작해야 하나요?
* 필요하다면 어디에서 더 많은 도움을 받을 수 있을까요?

> **참고하기**<br>
* @18F의 [Making READMEs Readable](https://pages.18f.gov/open-source-guide/making-readmes-readable/){:target="_blank" }
* @PurpleBooth의 [README template](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2){:target="_blank" }
* Google Guava [README.md](https://github.com/google/guava/blob/master/README.md){:target="_blank" }

----

## 기여(Contributing) 가이드라인 작성하기


기여 가이드라인을 작성할 때 아래 사항들이 잘 설명될 수 있도록 작성합니다.
 
* 기여자가 버그 보고서를 제출하는 방법(일반적으로 이슈와 PR 템플릿 사용을 추천)
* 기여자가 새로운 기능을 제안하는 방법
* 기여자가 환경 설정 및 테스트 실행 방법
* 기술적 세부 사항과 함께 기대하는 기여 내용을 전달하는 방법
* 원하는 기여 유형
* 프로젝트 로드맵 또는 비전
* 기여자가 여러분과 연락하는 데 사용할(혹은 사용하지 말아야 할) 방법

> **참고하기**<br>
* @nayafia의 [Contributing guide template](https://github.com/nayafia/contributing-template/blob/HEAD/CONTRIBUTING-template.md){:target="_blank" } 
* @mozilla의 “[How to Build a CONTRIBUTING.md](http://mozillascience.github.io/working-open-workshop/contributing/){:target="_blank" }”  
* Spring framework [CONTRIBUTING.md](https://github.com/spring-projects/spring-framework/blob/main/CONTRIBUTING.md){:target="_blank" }  


### CLA(Contributor Licensing Agreement) 동의
CLA 동의는 오픈소스 프로젝트에 기여하는 사람들로부터 해당 프로젝트에 대한 관리 권한을 위임받는 것입니다. 이는 저작권 및 지적 재산권 소송이나 라이선스 변경 등 주요한 이슈가 발생한 경우, 적절한 대응을 위해 필요한 절차입니다.


[CLA Assistant](https://cla-assistant.io/){:target="_blank" }를 활용하여 CLA 동의를 받을 수 있습니다. CLA Assistant를 사용하는 방법은 아래와 같습니다.


1. [GIST](https://gist.github.com/){:target="_blank" }에 CLA를 생성합니다.
2. [CLA Assistant](https://cla-assistant.io/){:target="_blank" }에서 **Configure CLA** 버튼을 클릭 후, 적용할 저장소 및 CLA 선택합니다. 
   - CLA에 서명하지 않은 PR을 보내는 사람은 PR(Pull Request)에 아래와 같이 메시지가 표시됩니다.
   - 컨트리뷰터(Contributor)는 **Contributor License Agreement** 링크를 클릭하면 서명할 실제 CLA 서명 페이지로 이동합니다. 이 과정에서 **GitHub 인증 후 동의** 절차를 거치게 됩니다.<br>
     <img src="https://t1.kakaocdn.net/olive/ossguide/cla.png" class="my-6" width="850">


> **참고하기**<br>
> * CLA 동의 예시에 대한 자세한 내용은 [카카오 오픈소스 Khaiii CLA 동의](https://cla-assistant.io/kakao/khaiii){:target="_blank"} 링크를 참고합니다.

----

## 행동 강령(Code of conduct) 수립

행동 강령을 수립할 때 아래 사항들이 잘 설명될 수 있도록 작성합니다.

* 건강하고 건설적인 커뮤니티를 위한 행동강령을 수립합니다.
* 참여자가 어떻게 행동하기를 기대하는지 전달하는 것 외에, 이러한 기대가 누구에게 적용되는지, 언제 적용되는지 그리고 위반할 경우 어떻게 처리되는지 등의 내용을 포함합니다.
* 행동 강령 작성 시 [오픈소스 가이드의 행동 강령](https://opensource.guide/ko/code-of-conduct/){:target="_blank"}을 참고해 작성합니다.  



> **참고하기**
> 
> 필요한 경우 아래의 추가적인 행동 강령 예시들을 참고합니다.
> 
>* [Contributor Covenant](https://www.contributor-covenant.org/){:target="_blank" } - Kubernetes, Rails 및 Swift를 포함한 40,000개 이상의 오픈소스 프로젝트에서 사용되는 행동 강령
> * [Google: Code of conduct](https://github.com/google/.github/blob/master/CODE_OF_CONDUCT.md){:target="_blank" }

