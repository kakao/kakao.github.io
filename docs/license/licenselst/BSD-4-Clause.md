---
layout: default
title: BSD-4-Clause
parent: 라이선스별 의무사항
grand_parent: 오픈소스 라이선스
---
# {{ page.title }}

## 라이선스 개요

### 라이선스 요약

BSD-4-Clause 라이선스는 기본적으로 고지에 대한 의무가 주를 이루고 있으며, <span>광고에 대한 조항(Advertising clause)</span>{: .text-red-400 }이 존재합니다.


{: .div_box}
> #### 소스 형태로 재배포
>
> - **고지 의무 + <span>광고 조항(Advertising clause)</span>{: .text-red-400 }**
>   - 소스 코드 내 명시된 저작권과 라이선스 정보를 그대로 유지한 상태로 재배포합니다.
>   - BSD-4-Clause 라이선스 하에 <span>오픈소스의 기능과 활용을 언급하는 모든 광고</span>{: .text-red-400 }에 아래 문구를 포함시킵니다. 
>   - <i>“This product includes software developed by the \<organization\>.”</i>
>
> #### 바이너리 형태로 재배포
>
> - **고지 의무**
>   - 오픈소스 고지문을 생성하여 바이너리 재배포 시 동봉합니다.
>   - BSD-4-Clause 라이선스 하에 <span>오픈소스의 기능과 활용을 언급하는 모든 광고</span>{: .text-red-400 }에 아래 문구를 포함시킵니다.
>   - <i>“This product includes software developed by the \<organization\>.”</i>
> 

>  **참고하기**
>
>  광고에 대한 조항이 자유로운 사용을 막을 수 있는 보다 자세한 이유는 [The BSD License Problem](https://www.gnu.org/licenses/bsd.html){:target="_blank"} 페이지에서 확인할 수 있습니다.



### 라이선스 설명

[BSD-4-Clause](http://directory.fsf.org/wiki/License:BSD_4Clause){:target="_blank"}는 BSD 4-Clause "Original BSD License" 또는 "Old BSD License" 라고도 불리며 소스 코드 공개를 요구하지는 않는 퍼미시브(Permissive) 형태의 라이선스입니다.<br>

다만, 라이선스가 **광고 조항(Advertising clause)**을 포함하고 있어, 자유롭게 사용하는데 문제가 될 수 있습니다.


>  **참고하기**
>
>  BSD-4-Clause 라이선스에 관한 보다 자세한 내용은 [라이선스 전문 설명](http://directory.fsf.org/wiki/License:BSD_4Clause){:target="_blank"}을 참고합니다.


### 소스 코드 내 라이선스 문구
BSD-4-Clause 라이선스 하에 오픈소스는 일반적으로 소스 코드 상단에 아래와 같은 문구가 존재합니다.  


```
Copyright (c) <year>, <copyright holder>
All rights reserved.
  
Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:
  
1. Redistributions of source code must retain the above copyright
notice, this list of conditions and the following disclaimer.
2. Redistributions in binary form must reproduce the above copyright
notice, this list of conditions and the following disclaimer in the
documentation and/or other materials provided with the distribution.
3. All advertising materials mentioning features or use of this software
must display the following acknowledgement:
This product includes software developed by the <organization>.
4. Neither the name of the <organization> nor the
names of its contributors may be used to endorse or promote products
derived from this software without specific prior written permission.
  
THIS SOFTWARE IS PROVIDED BY <COPYRIGHT HOLDER> ''AS IS'' AND ANY
EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL <COPYRIGHT HOLDER> BE LIABLE FOR ANY
DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
```

----

## 배포 형태별 의무사항
### Case 1: 소스 형태로 재배포
BSD-4-Clause 라이선스 하에 오픈소스를 소스 형태로 재배포 시, 아래 사항들을 준수합니다.

#### 고지 의무
소스 코드 내 명시된 저작권 및 라이선스 정보를 그대로 유지한 상태로 재배포합니다.

- 저작권 고지
- 라이선스 사본 제공
- 보증 부인 고지
- BSD-4-Clause 라이선스 하에 <span>오픈소스의 기능과 활용을 언급하는 모든 광고</span>{: .text-red-400 }에 아래 문구를 포함시킵니다.  
  <span>“This product includes software developed by the \<organization\>.”</span>{: .text-green-200 }


### Case 2: 바이너리 형태로 재배포
BSD-4-Clause 라이선스 하에 오픈소스를 빌드하여 바이너리 형태로만 재배포 시, 아래 사항들을 준수합니다.  

#### 고지 의무
아래의 내용을 포함하는 오픈소스 고지문을 생성하여 바이너리 재배포 시 동봉합니다.

- 저작권 고지
- 라이선스 사본 제공
- 보증 부인 고지
- BSD-4-Clause 라이선스 하에 <span>오픈소스의 기능과 활용을 언급하는 모든 광고</span>{: .text-red-400 }에 아래 문구를 포함시킵니다.  
  <span>“This product includes software developed by the \<organization\>.”</span>{: .text-green-200 }


### 광고 조항 문제

FreeBSD, NetBSD, BSD 등의 오픈소스는 원래 BSD-4-Clause를 적용하였으나, **광고 조항(Advertising clause)**의 문제를 인식하여 BSD-3-Clause, BSD-2-Clauese 등으로 라이선스를 변경하였습니다.

- FreeBSD: [BSD-2-Clause로 변경](http://www.gnu.org/licenses/bsd.html){:target="_blank"}
- NetBSD: [BSD-2-Clause로 변경](http://www.netbsd.org/about/redistribution.html#why2clause){:target="_blank"}
- BSD: [BSD-3-Clause로 변경](http://www.netbsd.org/about/redistribution.html#why2clause){:target="_blank"}


>  **참고하기**
>
> ✔︎ [OSADL](https://www.osadl.org/){:target="_blank" .line} 체크리스트: [https://www.osadl.org/fileadmin/checklists/unreflicenses/BSD-4-Clause.txt](https://www.osadl.org/fileadmin/checklists/unreflicenses/BSD-4-Clause.txt){:target="_blank"}
