---
layout: post
title: 'kakao의 오픈소스 Ep6 - Cite'
author: niko.bellic
date: 2016-12-26 17:00
tags: [opensource,cite,kubernetes,github,docker,container,microservice]
---
<a id="forkme" href="https://github.com/kakao/cite"></a>

> "카카오의 오픈소스를 소개합니다" 여섯번째는 [niko.bellic](https://github.com/code0x9)이 개발한 **Cite**입니다.
>
> [Cite](https://github.com/kakao/cite)는 Container as a Service(CaaS)로서 소스코드를 빌드하고 배포하며 운영하는 일련의 과정을 자동화하는 웹 서비스입니다.


## Introduction


[Cite](https://github.com/kakao/cite)는 google kubernetes기반 CaaS(Container as a Service)입니다. 

Kubernetes는 최근 Container Orchestrator로 각광받고 있지만 설치와 운영이 복잡하기 때문에 익혀서 사용하기 위해서는 많은 시간과 노력을 필요로 합니다.

![Google Trends on Major Container Orchestrators](/files/cite-google-trends-container_orchestrators.png)

Cite는 이러한 어려움을 줄이기 위해 Kubernetes Cluster를 사전에 생성하고 실제 서비스 담당 개발자가 Kubernetes Cluster로 서비스 배포/롤백 등을 할 수 있도록 Kubernetes와 GitHub을 연동하였습니다.

## Why Cite?

 * Fast IT
   * 더 빠르게 서비스를 생성/배포/롤백합니다. 가능한 모든 부분을 자동화!
   * 빠르게 확장(horizontal/vertical scaling)할 수 있습니다.
 * Efficient IT
   * 더 적은 하드웨어로 더 많은 서비스를 수행합니다.
   * 서비스 개발자와 SE의 인프라 관리 비용을 줄입니다.
 
## Workflow

Cite에서의 서비스 배포는 아래의 흐름을 따릅니다.

![Cite Workflow](/files/cite-workflow.png)

<!-- https://www.websequencediagrams.com/ source
title Cite Workflow

participant User
participant GitHub
participant Cite
participant Kubernetes
participant LoadBalancer
participant BuildBot

User->Cite: 서비스 생성
Cite->Kubernetes: kubernetes namespace 생성
note left of Kubernetes: github org => kubernetes namespace
Cite->GitHub: github webhook 생성
Cite->GitHub: repository에 collaborator 추가
Cite->Kubernetes: kubernetes 서비스 생성
note left of Kubernetes: github branch+reponame => kubernetes service name
Kubernetes->LoadBalancer: loadbalancer 생성
note right of LoadBalancer: 새 서비스가 생성될 때 LB인스턴스 생성

User->GitHub: git push
GitHub->Cite: push 이벤트
Cite->BuildBot: docker 빌드 요청
BuildBot->BuildBot: docker build & push
BuildBot->GitHub: status 이벤트: success
GitHub->Cite: status 이벤트
Cite->Kubernetes: kubernetes replication controller생성
Cite->Cite: RC와 Pod들이 Ready상태가 될때까지 대기
Cite->Kubernetes: 서비스 selector 갱신
Kubernetes->LoadBalancer: loadbalancer 갱신
note right of LoadBalancer: 서비스의 selector가 변경될 때 LB인스턴스 갱신
-->

빌드, 배포, 롤백 등 각 서비스의 상태는 github commit status와 deployment status 이벤트를 통해 처리하며, LoadBalancer는 Kubernetes를 watch하여 각 서비스의 상태가 변경될 때 loadbalancer의 upstream을 변경합니다.

Cite에서는 Kubernetes에 내장된 rolling-upgrade 베포 방식이 아닌 A-B switching방식을 선택하였습니다. A-B switching은 배포시 새 컨테이너를 모두 구동한 후 loadbalancer에서 새 서비스의 upstream을 사용하도록 변경하는 방식인데요, 이 방식은 rolling-upgrade에 비해 배포시 리소스 사용량은 많지만 배포 이후에도 일정 기간 기존 컨테이너가 구동중이기 때문에 롤백이 빠르다는 장점이 있습니다. Cite는 주기적으로 1시간 이상 사용되지 않는 - service selector에 등록되지 않은 - 컨테이너를 종료하고 있습니다.

## 현황 (2016.12.27)

* Kubernetes Cluster
  * etcd, master : 물리장비 x 3대
  * nodes : 물리장비 x 10대
  * elasticsearch : 물리장비 x 4대 + 가상머신 3대
  * loadbalancer : Citrix NetScaler active/standby
* Kubernetes Services
  * service : 184개
  * pod : 332개

* 전체 물리장비 현황

![Cite Cluster Stats](/files/cite-cluster-stats.png)

* node 1의 24시간 현황

![Cite Node1 Stats](/files/cite-node1-stats.png)

## 적용 사례 : skraper (by [pj.vegan](mailto:pj.vegan@kakaocorp.com))

skraper는 카카오톡, 스토리 등 서비스에서 URL을 입력받고 해당 URL을 방문하여 대표 이미지를 추출한 후 반환하는 서비스입니다. skraper는 최초의 cite를 이용한 퍼블릭 서비스로 현재 cite에서 컨테이너 5 + 10개로 구동중입니다. 

## Reference

* GitHub Enterprise API : [https://developer.github.com/enterprise/2.8/v3/](https://developer.github.com/enterprise/2.8/v3/)
* Kubernetes Documents : [http://kubernetes.io/docs/](http://kubernetes.io/docs/)
* Docker Documents : [https://docs.docker.com/](https://docs.docker.com/)

## See also
* Cite Documents : [http://tech.kakao.com/docs-cite/](http://tech.kakao.com/docs-cite/)
