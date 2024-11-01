---
layout: default
title: Grafana, Loki, Tempo
parent: 라이선스 변경 사례
grand_parent: 오픈소스 라이선스
nav_order: 1
---
# {{ page.title }}

## Grafana, Loki, Tempo: AGPL 3.0 라이선스 적용
### 변경사항
라이선스 변경사항은 아래와 같습니다.


{: .div_box}
Grafana, Loki, Tempo의 라이선스가 Apache 2.0에서 <span>AGPL 3.0</span>{: .text-red-400 }으로 변경되었습니다.<br>
Grafana <a href="https://github.com/grafana/grafana/tree/v7.5.6" target="_blank">v7.5.6</a>, Loki <a href="https://github.com/grafana/loki/tree/v2.3.0" target="_blank">v2.3.0</a>, <a href="https://github.com/grafana/tempo/releases/tag/v0.7.0" target="_blank">Tempo v0.7.0</a> 부터 <span class="text-red-300"> AGPL 3.0</span> 라이선스가 적용됩니다.<br>
기타 플러그인(Plugin), 에이전트(Agent), 일부 라이브러리들은 Apache 2.0 라이선스를 그대로 유지합니다.<br>

### 주의 사항
변경에 따른 주의사항은 아래와 같습니다.

- AGPL 3.0 라이선스는 **GPL 3.0 라이선스에 네트워크 사용 관련 의무사항이 추가**된 라이선스입니다.
- AGPL이 적용된 서비스가 네트워크(예: REST API)를 통해 클라이언트(예: 브라우저)에게 기능을 제공하는 경우에, 기능을 사용하는 모든 사용자에게 AGPL 서비스를 포함한 전체 소스를 공개하는 의무사항이 발생합니다.
- 위 의무사항은 **웹 서비스의 경우도 해당**합니다.
- 예를 들어, AGPL이 적용된 Grafana 서비스를 제 3자에게 클라이언트(브라우저) 등에서 사용할 수 있도록 제공하는 경우, Grafana 서비스의 전체 소스를 공개해야 합니다.
  
