---
layout: page
title: ASIC, SoC, 반도체, 설계 관련 글 모음
image: /files/covers/clock.jpg
cover:
  title: 'Clock'
  link: https://pixabay.com/photo-1274699/
  author:
    name: 'Monoar'
    link: https://pixabay.com/ko/users/Monoar-2240009/
permalink: /asic/
sitemap: yes
excerpt: ASIC, SoC, 반도체, 설계 관련 글을 모아두는 곳입니다. 계속 업데이트 됩니다.
tags: [ASIC, SoC, 반도체, 설계, Synopsys, Cadence]
---

<!-- toc orderedList:0 -->

- [HDL](#hdl)
	- [Verilog](#verilog)
	- [VHDL](#vhdl)
	- [Etc](#etc)
- [EDA Tool (Synopsys, Cadence)](#eda-tool-synopsys-cadence)
	- [Synopsys Design Compier](#synopsys-design-compier)
	- [Synopsys VCS](#synopsys-vcs)
- [반도체 일반](#반도체-일반)

<!-- tocstop -->

## HDL
### Verilog
* [http://www.testbench.in/](http://www.testbench.in/) - 테스트 벤치, SystemVerilog
* [Verilog 설계 팁](http://ts.devbj.com/226) - IDEC 2012 한글자료
* [Test bench 테스트벤치 작성 가이드](http://ts.devbj.com/210) - 카운터예제로 정리해둔 영어자료
* [VCD file](http://ts.devbj.com/209) - Value Change Dump 파일, 소스코드에서 VCD 파일을 어떻게 만드는지 호출하는 함수들에 대한 간략한 소개

### VHDL
* none

### Etc
* none

## EDA Tool (Synopsys, Cadence)
* [EDA 툴 설치가이드](http://ts.devbj.com/208) - DC, PrimeTime, NCVerilog, Formality 의 설치가이드 한글자료 모음 from IDEC
* [How the gate count of a design is determined?](http://ts.devbj.com/217) - 게이트카운트 구해보기 대략적으로 (간단하게 보통 NAND2 게이트 면적으로 나눠서 알아낸다.)

### Synopsys Design Compier
* [Design Compiler 관련글](http://ts.devbj.com/438)
  - [Design Compiler 정리](http://blog.naver.com/PostList.nhn?blogId=beahey&from=postList&categoryNo=85)
  - [Donny님 블로그](http://www.donny.co.kr/)
    * [마이크로프로세서 설계 무작정 따라하기 Part-III (1회)](http://www.donny.co.kr/simplecore/simplecore3-1.pdf)
    * [마이크로프로세서 설계 무작정 따라하기 Part-III (2회)](http://www.donny.co.kr/simplecore/simplecore3-2.pdf)
    * [마이크로프로세서 설계 무작정 따라하기 Part-III (3회)](http://www.donny.co.kr/simplecore/simplecore3-3.pdf)
    * [마이크로프로세서 설계 무작정 따라하기 Part-III (4회)](http://www.donny.co.kr/simplecore/simplecore3-4.pdf)
    * [마이크로프로세서 설계 무작정 따라하기 Part-III (최종회)](http://www.donny.co.kr/simplecore/simplecore3-5.pdf)
* [set_false_path/set_case_analysis](http://ts.devbj.com/219) - 간단한 설명, 타이밍과 관련이 있지만 합성에 중요한 변수가 된다.

### Synopsys VCS
* [Simulating verilog VHDL using Synopsys VCS - 칩 설계 검증 툴](http://ts.devbj.com/415)
* [VCS and coverage by Aviral Mittal](http://www.vlsiip.com/vcs/) - 기초적인 내용. 정리 잘되어 있음
* [Open Masca: Simulating mixed language HDL using VCS](http://salinasv.blogspot.kr/2011/05/simulating-mixed-language-hdl-using-vcs.html) - 간략하게 굿.
* [Simulation with VCS](http://documents.mx/documents/5-simulation-vcs.html) - Synopsys 자체 자료니, 좋은 자료인듯. 원본은 어디서 찾아봐야할 듯.
* [RTL Simulation using Synopsys VCS](http://www.csl.cornell.edu/courses/ece5745/handouts/ece5745-tut1-vcs.pdf) - 2016버전, 너무 간단하지만 그냥 명령어 옵션 구경할 만함.
* Gate-Level Simulation With Synopsys VCS Simulator [Synopsys VCS Support (PDF) chapter in volume 3 of the Quartus II Development Software Handbook](https://www.altera.com/content/dam/altera-www/global/en_US/pdfs/literature/hb/qts/qts_qii5v3.pdf) - 정말 좋은 자료. 방대한 양이 질리겠지만 타이밍,합성관련 정보가 짱
  - [(localcopy)Quartus II Development Software Handbook](/files/localcopy/qts_qii5v3.pdf)
* 연세대 한글자료 - [Mixed Signal Simulation](http://soc.yonsei.ac.kr/class/material/dft_class/06_abist_synopsys.pdf)

## 반도체 일반
* [ESD Test - HBM, MM, CDM](http://ts.devbj.com/425)

---
문의: [{{ site.email }}](mailto:{{ site.email }})
