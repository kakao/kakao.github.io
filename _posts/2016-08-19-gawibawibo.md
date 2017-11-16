---
layout: post
title: 'CODING BATTLE 가위바위보! - 못다한 이야기'
author: iolo.fitzowen
date: 2016-08-19 18:00
tags: [coding,gawibawibo,pycon,python]
image: /files/covers/dices.jpg
cover:
  title: 'Dices'
  link: https://flic.kr/p/9izbbs
  author:
    name: 'Tuyet Yen Tang'
    link: https://www.flickr.com/photos/sytyin/
---

## 어쩌다보니 키스톤!

지난 8월 13일(토)부터 이틀간 코엑스 그랜드에서 열렸던 [PyCon 2016 APAC]에서 
카카오 부스를 지켰던 [iolo.fitzowen](https://github.com/iolo) 입니다.

**키스톤 스폰서** 자격으로 행사장에서 가장 큰 부스를 운영하게되었는데,
거대한 부스를 어떻게 활용할 것인가를 오랫동안 고민했습니다.

![카카오 부스 이모저모](/files/gawibawibo-booth.png)

## 어쩌다보니 가위바위보!

부스 이벤트로 코딩 퀴즈를 하기로 하고
사내 그룹웨어인 아지트를 통해 문제를 추천 받았는데,
**[bryan.j]()가 제안한 가위바위보 AI 대전** 아이디어을 다듬어
**CODING BATTLE 가위바위보!**라는 이름의 행사를 진행했습니다.
(이 자리를 빌어, 멋진 아이디어를 주신 bryan.j, 그리고 채택되지 않았지만 다양한 의견을 주신 여러분께 감사드립니다.)

![CODING BATTLE 가위바위보! 포스터](/files/gawibawibo-poster.png)

자세한 내용은 이벤트 페이지 [CODING BATTLE 가위바위보! in 파이콘 2016 APAC](http://tech.kakao.com/pycon2016apac)를 참고하시고,
이 글에서는 파이썬 초보(!)가 코딩 이벤트를 진행하면서 겪었던 에피소드를 인상적인 소스 코드와 함께 전해드리겠습니다.

## 1부: MAKING FILM

### Ver1. 클라우드 서비스 + 네트웍 대전

최초의 아이디어는 **서버-to-서버 HTTP 통신을 이용하는 방식**이었습니다.

1. (제가) 게임 진행 서버(host-server)를 개발하고,
1. (참가자들은) 플레이어 서버(player-server)를 개발해서 (무료) 클라우드 서비스에 올리고,
1. (제가 만든) 진행 서버가 (참가자들이 만든) 두 개의 플레어어 서버가 HTTP 통신을 하면서 게임을 진행하고,
1. 진행 서버에 브라우저로 접속해서 생방송(websocket)으로 볼 수 있는...

방식이었습니다.

<img src="http://item.kakaocdn.net/do/-26p06+UqCd0OAgiRHNZwHaq4FJCveCBKCNZV-bZscw_/235f17cb451b46cf1769668f50ae59981667fc7b08261b4c493670baa83d5cb9" class="hcenter"/>

보신 분들은 없겠지만, 이 방식으로 구현된 버전이 행사 이틀 전에 [카카오의 깃헙](https://github.com/kakao)에 잠깐 올라가 있었습니다^^;

### Ver2. 이메일 접수 + 로컬 대전 - Back to the 199x

행사 전날 오후, 회사 카페에서
[clark.kang](https://charsyam.wordpress.com)과
[henry.ha](http://www.slideshare.net/yongho)를 우연히 만나
(그렇습니다! 카카오에 입사하시면... 이런 연예인(?)들은 매일 우연히 마주칠 수 있습니다!)
파이콘 이벤트에 대해 얘기를 나누다가...
**코엑스의 열악한 네트웍 환경에서 클라우드 서버에 올리는 삽질의 무의미함**에 대한 날카로운 지적(!)을 받고,
**로컬 환경에서 개발하고 테스트하고 대결할 수 있는 방식**으로 변경하기로 전격 결정!!!

그날 밤을 꼴딱 새서 새로운 [게임 진행 서버](https://github.com/kakao/pycon2016apac-gawibawibo)를 만들었습니다.

<img src="http://item.kakaocdn.net/do/-26p06+UqCd0OAgiRHNZwHaq4FJCveCBKCNZV-bZscw_/477c52636630bc15b2890bde099cba0a1667fc7b08261b4c493670baa83d5cb9" class="hcenter"/>

1. (참가자들은) `show_me_the_hand`라는 괴상한 이름의 파이썬 함수를 작성하고,
2. (참가자들은) 작성한 코드를 **이메일**을 통해 `player.py`라는 첨부파일로 제출하면,
3. (옆에 앉아있던 [violet.blue]()와 [yally.next]()가) **수작업으로** 메일박스를 확인해서 `player.py` 파일을 모아서 정리하고,
4. (제가) 지난 밤에 발로 만든 [게임 진행 서버]를 사용해 게임을 진행하는...

흠흠... 그러니까 여러분들이 보신... (웹브라우저와 터미널을 번갈아 보여주면서 생목으로 고함을 지르는) 바로 그 방식입니다^^;;

### Day 1. of the random, by the random, for the random

방식을 급히 바꾸면서 사건사고도 많았습니다.

카카오 부스를 방문한 [JetBrains](https://www.jetbrains.com) 직원이 콧방귀를 뀔 정도로 전근대적인 방법이지만,
그만큼 확실하다고 믿었던 메일이 백본네트웍 장애라는 전대미문의 장애로 첨부파일이 손상되는 초유의 사태가 발생했습니다.
오후 4시가 되서야 참가자 9명의 첨부 파일이 모두 복구됐고... 9명을 추가해서 예선전을 다시 치렀죠. 덕분에 결과 발표도 5시로 연기.

(옆에 앉아었던 [violet.blue]()가) 웹을 뒤져서 받은 음성 파일과 손바닥 이미지 파일을, 
(바로 옆에서 [스마트스터디](http://www.smartstudy.co.kr) 부스를 지키고 있던) [outsider]님에게 넘겨주고 30분 남짓 개발한 것을,
(제가) 대충 갖다 붙여서 (수동으로 버튼을 누르면 나타나고/사라지는) **안내면술래 가위바위보! 보! 보! 보!** 애니메이션도 준비했습니다.

![안내면술래 가위바위보! 보! 보! 보!](/files/gawibawibobobobo.png)

첫 날은 참가 신청자가 100명을 넘지 않아,
메일만 제 때 도착했다면 [라이언 캐릭터 목베개](https://store.kakaofriends.com/store/kr/product/product.lime?r_ctseq=23&r_prcode=FRPBRYMBG0181)를
받을 수 있었습니다. 무더운 날씨에도 불구하고 목배게를 목에 걸고 다니시던 모습을 보며... 참 뿌듯(?) 했었죠.

시험적으로 몇판 돌려보니, 라이브로 해도 되겠다고 판단하고, 예정보다 한시간 늦은 오후 5시, 랩탑을 TV에 연결하고 **라이브**로 대본없이 진행했습니다.

![Day 1. 게임 결과 발표 라이브](/files/gawibawibo-day1-live.jpg)

결과는 아시다시피(예상대로) **random**의 완승이었습니다.

진지하게(?) 접근했던 참가자들은 그 결과에 분노(?)했고, 저도 마찬가지였습니다.
이벤트를 준비하면서 수억번의 가위바위보를 했지만, 랜덤을 이길 방법은 쉽게 보이지 않았습니다. 정말 없을까요?

그래서!

2일차는 규칙을 바꿔보기로 했습니다. 파이썬 기본으로 제공하는 `random`과 외부 모듈을 사용하지 않고, 코드로 정면 승부!!

### Day 2. algorithm strikes back

다음 날 아침, 행사장에 도착하니, 이미 참가 접수 메일이 들어오고 있었습니다.(순진한 개발자들, 이제야 선착순의 의미를 깨달았어...)
점심때 쯤엔 참가 신청 메일이 100통을 넘었습니다.(어랏 장난이 아닌데...)
접수를 중단해야 할지를 고민하다가, 경품(라이언 목베개)은 줄 수 없지만, 게임에는 참가할 수 있는 것으로 결정했습니다.

오후 2시, 참가 접수를 마감하고 시험삼아 몇 게임씩 돌리던 중,
몇몇 플레이어들의 특이한 결과를 확인하고,
코드들 뜯어보니 **파이썬 마법의 열쇠** 더블언더스코어(`__`)가 여기저기 흩어져 있더군요.
파이썬 초보인 저로써는 의도 조차 파악하기 힘들어, 파이썬 고수들을 찾아갔습니다.
자원봉사자로 참여하고 있던 [ganadist]님, 정지오님, 서승효님을 비롯한 몇몇 분들의 도움을 받아
적들의(?) 의도와 막을 수 있는 방법을 급히 확보했습니다.

<img src="http://item.kakaocdn.net/do/-26p06+UqCd0OAgiRHNZwHaq4FJCveCBKCNZV-bZscw_/09632d0f859f20907e11d3d4ec51e95b1667fc7b08261b4c493670baa83d5cb9" class="hcenter"/>

게임 결과 발표 시간이 임박해서 일부 참가자들의 코드는 확인하지 못한채 발표를 시작했는데....
아니나 다를까... 확인하지 못한 코드들이 말썽을 부렸습니다.
 175명이 풀리그를 치르려면 15,225 게임(1,522,500 번의 가위바위보)를 해야 하는데... 매번 `sleep(.1)`을 하면... ㅠㅠ
가위바위보 한 번 결정하는데 1초 이상이 걸리는 플레이어도 있었습니다. 이 플레이어도 공평하게 174 게임(17,400 번의 가위바위보)를 해야 했죠.

![Day 2. 게임 결과 발표 라이브](/files/gawibawibo-day2-live.jpg)

그래도 기다려보자!라고 버텼지만, 저의 오기를 비웃 듯 행사장의 전원이 꺼졌습니다.
CPU 사용량 100%의 상태에서 랩탑의 배터리는 2시간도 못버틸테고, 그때까지 결과가 나올 가능성은 없었습니다.
결국, 2일차 결과 발표를 연기할 수 밖에 없었습니다.
부피를 최소화하기 위해 래핑된 라이언의 표정이 슬프...

![Day 2. 게임 결과 발표 연기 때문에 귀를 잃어버린 라이언](/files/gawibawibo-day2-ryan.jpg)

참가자들의 의욕을 과소평가한... 저의 불찰입니다.
이 자리를 빌어서 기다려주신 많은 참가자 분들께 사과드리고, 또 감사드립니다.

<img src="http://item.kakaocdn.net/do/-26p06+UqCd0OAgiRHNZwHaq4FJCveCBKCNZV-bZscw_/46d01f5ff600e23a970e9ce86c02eff81667fc7b08261b4c493670baa83d5cb9" class="hcenter"/>

마무리를 짓지 못하고 찝찝한 마음과 지친 몸을 끌고 섬으로 돌아오면서,
제시한 룰을 깨트리지 않고 어뷰징을 막을 수 있는 방법을 고민했는데,
[ganadist]님께서 [선물](https://gist.github.com/ganadist/de618f92897144273586648bc07cfd7b)을 보내왔습니다.

우여곡절 끝에, 오늘에야 2일차 게임 결과를 발표합니다(두둥!):

#### Day2. 게임 결과 발표 - 예선(풀리그)

2일차 오후 2시까지 접수된 188명 중에서, 예제를 복사해서 낸 5명, `random`을 사용한 8명을 뺀
175명(1일차 참가자 32명 포함)의 코드가 접수되었고,
`input` 함수를 사용하거나(키보드 입력 대기) `show_me_the_hand` 함수가 없는 11명을 제외한
164명이 예선에 참가했습니다.

예선은 풀리그 방식으로 164명의 플레이어가 다른 163명과 게임을 진행합니다.
총 13,366(164*163/2) 게임, 1,336,60 번의 가위바위보를 하는 거죠.
이 글을 쓰고 있는 시점에 6시간째 돌아가고 있군요. 12,452 번째 게임이니까 끝이 보입니다.

<img src="http://item.kakaocdn.net/do/-26p06+UqCd0OAgiRHNZwHaq4FJCveCBKCNZV-bZscw_/9e7a61ac86c673b1e6a5bbe2cde7ff791667fc7b08261b4c493670baa83d5cb9" class="hcenter"/>

예선전 시작 동영상(**용량이 큽니다. 데이터 요금에 주의하세요**)

혼자 회의실에 앉아 대사를 읊으려니 여간 쑥스러운게 아닙니다.

<video controls="true" crossorigin="anonymous" style="width:100%;">
    <source src="https://mk.kakaocdn.net/dn/osa/pycon2016apac/day2-part1-fullleague.webm" type="video/webm" />
    <source src="https://mk.kakaocdn.net/dn/osa/pycon2016apac/day2-part1-fullleague.ogv" type="video/ogg" />
    <source src="https://mk.kakaocdn.net/dn/osa/pycon2016apac/day2-part1-fullleague.mp4" type="video/mp4" />
</video>

#### Day2. 게임 결과 발표 - 본선(토너먼트)

본선 32강전 동영상(**용량이 큽니다. 데이터 요금에 주의하세요**)

<video controls="true" crossorigin="anonymous" style="width:100%;">
    <source src="https://mk.kakaocdn.net/dn/osa/pycon2016apac/day2-part2-round32.webm" type="video/webm" />
    <source src="https://mk.kakaocdn.net/dn/osa/pycon2016apac/day2-part2-round32.ogv" type="video/ogg" />
    <source src="https://mk.kakaocdn.net/dn/osa/pycon2016apac/day2-part2-round32.mp4" type="video/mp4" />
</video>

본선 16강전 동영상(**용량이 큽니다. 데이터 요금에 주의하세요**)

<video controls="true" crossorigin="anonymous" style="width:100%;">
    <source src="https://mk.kakaocdn.net/dn/osa/pycon2016apac/day2-part3-round16.webm" type="video/webm" />
    <source src="https://mk.kakaocdn.net/dn/osa/pycon2016apac/day2-part3-round16.ogv" type="video/ogg" />
    <source src="https://mk.kakaocdn.net/dn/osa/pycon2016apac/day2-part3-round16.mp4" type="video/mp4" />
</video>

본선 8강전 &amp; 준결승 동영상(**용량이 큽니다. 데이터 요금에 주의하세요**)

<video controls="true" crossorigin="anonymous" style="width:100%;">
    <source src="https://mk.kakaocdn.net/dn/osa/pycon2016apac/day2-part4-round8to4.webm" type="video/webm" />
    <source src="https://mk.kakaocdn.net/dn/osa/pycon2016apac/day2-part4-round8to4.ogv" type="video/ogg" />
    <source src="https://mk.kakaocdn.net/dn/osa/pycon2016apac/day2-part4-round8to4.mp4" type="video/mp4" />
</video>

결승전 동영상(**용량이 큽니다. 데이터 요금에 주의하세요**)

<video controls="true" crossorigin="anonymous" style="width:100%;">
    <source src="https://mk.kakaocdn.net/dn/osa/pycon2016apac/day2-part5-final.webm" type="video/webm" />
    <source src="https://mk.kakaocdn.net/dn/osa/pycon2016apac/day2-part5-final.ogv" type="video/ogg" />
    <source src="https://mk.kakaocdn.net/dn/osa/pycon2016apac/day2-part5-final.mp4" type="video/mp4" />
</video>

## 코드 리뷰 - 그것이 알고싶다

이제부터 본론입니다.
    
### Day1. 우승, 준우승, 4강

참가하신(구경하신) 분들은 아시다시피 **random의 완승**이었습니다. 그게 가위바위보 게임의 본질이니까 이상할 건 없죠. 그래도...

#### 우승자의 코드 by k239507

차암 쉽죠? `가위`, `바위`만 내는 전략입니다.
그런데 이 전략이 (수학적인 설명은 못하지만) 대회 전에 제가 알고 있던 (상대방의 대전 기록을 분석하지 않고) **랜덤을 이기는 유일한 전략**이었습니다.

```python
from random import choice

choices = ['gawi', 'bawi', 'bo']

def show_me_the_hand(records):
    return choice(choices[:2])
```

#### 준우승자의 코드 by hulk

크게 다르지 않습니다. `가위`를 낼 확률이 좀 더 높아졌네요.

```python
from random import choice

def show_me_the_hand(records):
    return choice(['gawi', 'bawi', 'bo', 'gawi'])
```

#### 3위의 코드 by hahanbyul

역시 크게 다르지 않습니다. `가위`, `바위`를 낼 확률이 좀 더 높아졌네요.

```python
from random import choice

def show_me_the_hand(records):
    return choice(['gawi', 'bawi', 'bo', 'gawi', 'bawi'])
```

#### 또 다른 3위의 코드 by eclipse1725

아! 이번엔 뭔가 조금 다르죠?
상품을 전달할때도 참가자의 아쉬움과 분노(랜덤에 지다니!)가 느껴져서 저도 같이 분노(랜덤에 지다니!)했었죠.

<img src="http://item.kakaocdn.net/do/-26p06+UqCd0OAgiRHNZwHaq4FJCveCBKCNZV-bZscw_/d97c14883a6a6d849c7b15d68ed8c7271667fc7b08261b4c493670baa83d5cb9" class="hcenter"/>

```python
from random import choice

def show_me_the_hand(records):
	total = 0
	for i in range(len(records)):
		total += records[i][1]
	check1 = 0
	check2 = 0
	check3 = 0
	gbb = ['gawi', 'bawi', 'bo']
	if len(records) < 50:
		return 'gawi'
	elif records[0][0] == 'gawi':
		check1 += 1
		if records[1][0] == 'gawi':
			check1 += 1
		if records[2][0] == 'gawi':
			check1 += 1
		if records[3][0] == 'gawi':
			check1 += 1
		if records[4][0] == 'gawi':
			check1 += 1
		if check1 > 4:
			return 'bawi'
		else:
			return 'bo'
	elif records[0][0] == 'bo':
		check2 += 1
		if records[1][0] == 'bo':
			check2 += 1
		if records[2][0] == 'bo':
			check2 += 1
		if records[3][0] == 'bo':
			check2 += 1
		if records[4][0] == 'bo':
			check2 += 1
		if check2 > 4:
			return 'gawi'
		else:
			return 'bo'
	elif records[51][1] != 1:
		check3 += 1
		if records[52][1] != 1:
			check3 += 1
		if records[53][1] != 1:
			check3 += 1
		if records[54][1] != 1:
			check3 += 1
		if records[55][1] != 1:
			check3 += 1
		if records[56][1] != 1:
			check3 += 1
		if check3 > 4:
			return choice(gbb)
		else:
			return 'bo'
	else:
		if len(records) > 200:
			if total < 100:
				return choice(gbb)
			else:
				return 'bo'
		return 'bo'
	return choice(gbb)
```

대부분 예제 코드와 동일하거나 약간 수정한 전략이었습니다만, 몇몇 참가자들은 참신한 시도를 했습니다.
그러나, 이런 참신한 시도들은 순수한 랜덤에 허무하게 무너졌는데요,
상대의 전략을 파악했다(패턴을 읽었다)고 생각하고 대응 전략을 결정한 순간... 진거죠. 있지도 않은 패턴을 읽은... 오해영!

### Day2. 우승, 준우승, 4강

<img src="http://item.kakaocdn.net/do/-26p06+UqCd0OAgiRHNZwHaq4FJCveCBKCNZV-bZscw_/872b56c06d9ac5bc264419e187b346041667fc7b08261b4c493670baa83d5cb9" class="hcenter"/>

1일차 참가자들의 코드는 대충봐도 대부분 의도를 파악할 수 있었는데,
2일차 참가자들의 코드는 저같은 파이썬 초보에겐 어림도 없었습니다.
단 하루만에 완전히 다른 게임이 되었습니다.
개발자들이 독한 마음을 먹으면 이렇게 무섭습니다.

#### 우승자의 코드 by qkqnrpa

상대방이 직전에 냈던 손에 맞춰서 내는 전략인데요,
단순해 보이지만, 결과는 우승!!

CODING BATTLE 가위바위보는 - 이 분의 아이디처럼 -  **바부겜**이었을까요?

```python
def show_me_the_hand(records):
    gababo = ['bawi', 'bo', 'gawi']
    if len(records) == 0:
        return gababo[0]
    return gababo[records[0][1]]
```

#### 준우승자의 코드 by johnjanghochoi

상대방이 직전에 냈던 손과 같은 손을 내면 이기는 손을 내는 전략입니다.
역시나, 이유를 설명할 순 없지만, 결과는 결과는 매우 성공적!

```python
def show_me_the_hand(records):
    if len(records) == 0:
        return 'gawi'
    if records[0][0] == 'gawi':
        return 'bawi'
    elif records[0][0] == 'bawi':
        return 'bo'
    else:
        return 'gawi'
```

#### 3위의 코드 by bak723

상대방이 낸 손에 따라 승리에 4, 무승부에 2, 패배에 1의 가중치를 계산하고,
가중치가 가장 높은 - 가장 승률이 높은 손을 내는 전략입니다.(맞나요?)
안정적인 전략이지만, 이런 식의 전략이 아무생각없는 단순 랜덤에게 허무하게 패하는 경우가 많았습니다.
그래도 결과가 좋습니다.

```python
def w(winner, loser, drawn):
	return 4 * winner + 2 * drawn + loser

def w_(records, hand):
	win = 0
	lose = 0
	draw = 0
	for r in records:
		if r[0] == hand:
			if r[1] == 1:
				win += 1
			elif r[1] == 0:
				draw += 1
			else:
				lose += 1
	return w(win, lose, draw)

def show_me_the_hand(records):
	h = []
	if len(records) == 0:
		return 'bo'

	hands = {
		'gawi': 'bawi',
		'bo': 'gawi',
		'bawi': 'bo'
	}
	weights = {
		'gawi': w_(records, 'gawi'),
		'bawi': w_(records, 'bawi'),
		'bo': w_(records, 'bo')
	}

	maxValue = 0.0
	for k in weights.keys():
		if weights[k] > maxValue:
			maxValue = weights[k]
			h = hands[k]
	return h
```

#### 또 다른 3위의 코드 by bage79

대전 중에서 가장 많은 시간을 사용한 코드입니다. 동영상 녹화를 힘들게 만든 분이죠^^;
제 수준으로 의도 파악이 불가능하네요. 뭔가 어렵구나... 정도?
개인적으로는 우승하지 않을까... 기대를 했었는데...
의외로 단순한 전략에 허무하게 무너졌습니다.ㅠㅠ

<img src="http://item.kakaocdn.net/do/-26p06+UqCd0OAgiRHNZwHaq4FJCveCBKCNZV-bZscw_/ee57651cae091b135d3abf1f3d482a1d1667fc7b08261b4c493670baa83d5cb9" class="hcenter"/>

```python
def min_max_ratio(records):
    li = [a for (a, i) in records]
    ratio = {'gawi': 0, 'bawi': 0, 'bo': 0}

    for a in li:
        ratio[a] += 1

    if ratio['gawi'] == ratio['bawi'] == ratio['bo']:
        return 0, 0, None, None

    for k in ratio.keys():
        ratio[k] /= len(li)
        # print('ratio[%s]=%.1f' % (k, ratio[k]))

    min_ratio, max_ratio, min_enemy, max_enemy = 1.0, 0.0, None, None
    for k in ratio.keys():
        if ratio[k] > max_ratio:
            max_ratio, max_enemy = ratio[k], k
        if ratio[k] < min_ratio:
            min_ratio, min_enemy = ratio[k], k
    return min_ratio, max_ratio, min_enemy, max_enemy

def check_pattern(records):
    li = [a for (a, i) in records]
    for step in range((len(li) // 2), 0, -1):
        li1, li2 = li[:step], li[step:step * 2]
        if li1 == li2:
            return li[step - 1]

def show_me_the_hand(records):
    my_hand_from_enemy = {
        'gawi': 'bawi',
        'bawi': 'bo',
        'bo': 'gawi'
    }
    try:
        if len(records) == 0:
            return 'bawi'
        elif len(records) == 1:
            return 'bo'
        # elif len(records) == 2:
        #     return 'gawi'
        else:
            enemy_by_pattern = check_pattern(records)
            if enemy_by_pattern:  # 상대방의 패턴을 읽어서, 대응해보자.
                # print('by pattern -> ', my_hand_from_enemy[enemy_by_pattern])
                return my_hand_from_enemy[enemy_by_pattern]
            else:  # 패턴이 없다면..
                min_ratio, max_ratio, min_enemy, max_enemy = min_max_ratio(records)
                if max_enemy and max_ratio > 0.36:  # 많이 내는 종류가 있다면, 다시 낼 확률이 높다.
                    # print('by enemy max -> ', my_hand_from_enemy[max_enemy])
                    return my_hand_from_enemy[max_enemy]
                else:  # 많이 내는 종류가 없다면, 안 낸 것을 낼 확률이 높다.
                    # print('by enemy min -> ', my_hand_from_enemy[min_enemy])
                    return my_hand_from_enemy[min_enemy]
    except:
        return 'gawi'
```

본선 토너먼트에 오른 64명 중에서 승률 TOP 5을 보면:

1. chang12(71%)
1. blacksangi(66%)
1. etaehyun4(66%)
1. novelview9(62%)
1. bage79(62%)

가위바위보처럼 운에 의존하는 게임에서 60% 이상의 승률을 보였다는 것이 놀랍네요.
이 분들은 대진운이 안좋았거나 카운터 전략을 만났을 뿐... 너무 서운해 하지 않으셨으면... 

첫째날처럼 단순한 랜덤보다는 약간의 전략이 가미된 랜덤들이 많았고, 성적도 좋았습니다.
또한 상대방의 플레이를 교묘하게 따라 하는 전략들도 많았고, 성적도 좋았습니다.
복잡한 계산을 통해 상대방의 전략을 분석하고, 그에 따라 전략을 바꾸는 플레이어도 있었는데,
32강, 16강, 8강을 거치면서 의외로 단순한 전략을 오해해서(랜덤에서 패턴을 읽었다면... 오해영)
맥없이 무너지는 결과가 종종 있었습니다.
아직은 파악된 전략의 종류가 많지 않아서 효과적이지 않지만,
이런 대회를 계속 개최하면 어떻게 될까요?

이걸로 끝내기엔 아쉬우니, 재미있는 코드를 몇가지 살펴보겠습니다:

#### 한글로 작성한 코드 by wesky93

아... `gawi`, `bawi`, `bo`를 사용한 제 자신이 부끄러워지네요. `rock`, `scissors`, `paper`도 아니고 말이죠 ㅠㅠ

```python
from operator import itemgetter

# 하루동안 갑자기 베이지 활률을 공부해서.. 어떻게 될지는 모르겠네요..ㅋㅋ&땜방코드가 몇개 있습니다...
# pycon2016 홧팅
# p.s. 재미삼아 일부러 한글코딩 해봤습니다 ㅋ
"""
작동구조
-------
1. 게임 플레이 30회 까지는 임의로 정한 가위,바위,보 순서에 맞게 차례대로 진행됩니다.
2. 30회 이후부터는 가위,바위,보에 대한 조건확률을 구하고 가장 높은 확률을 정답을 내보냅니다.
3. 간혹 운이 나뻐 패배를 하는데 그 격차가 상당하기에 격차를 줄이기 위하여 500회 ~ 1000회의 시점에서는 매회 승률을 계산하여 적의 승률이 40%이상일경우 알고리즘을 변경합니다.
4. 변경될 알고리즘은 상대방의 기준으로 유리한 행동을 고르고 해당 행동과 반대되는 행동을 내보냅니다.
"""
# 내가 이길확률로 값을 결정
def 내전적추적(전적):
    내전적 = []
    for 기록 in 전적:
        손모양, 승부 = 기록
        if 승부 == 0:
            내전적.append((손모양, 승부))
        elif 승부 == 1:
            내전적.append((거울2(손모양), -1))
        else:
            내전적.append((거울(손모양), 1))
    return 내전적

# 내가 이길확률로 값을 결정
def 승부계수추가(승부계수,값):
    """ 승부여부 숫자값을 바탕으승부계수 딕셔너리에 값을 추가"""
    if 값 == 1:
       승부계수['승'] += 1
    elif 값 == 0:
       승부계수['무'] += 1
    else:
       승부계수['패'] += 1
    return 승부계수

def 전적분석(전적):
    """상대 전적을 분석줌하여 각 패의 활과승부계수을 알려줌"""
    # 행동계수 분석
    진행횟수 = len(전적)
    초기화 = {'gawi':0,'bawi':0,'bo':0}
    행동계수 = 초기화  # 전적에서 각 행동이 발생한 횟수
    행동확률 = 초기화  # 전적에서 각 행동이 발생한 학률
    승부행동계수 = 초기화    # 전적에서 승리 했을때의 각 행동 수
    승부행동확률 = 초기화    # 전적에서 승리 했을때의 각 행동 확률
    총승부계수 = {'승':0,'패':0,'무':0}
    for 기록 in 전적:
        손모양, 승부 = 기록
        # 승부 통계를 위한 데이터
        승부계수추가(총승부계수,승부)
        행동계수[손모양] += 1
        # 내가 이겼을 경우 (적이 졌을경우) -1 // 적이 이겼을 경우는 1
        if 승부 == 1:
            승부행동계수[손모양] += 1
        # 분석
        승률 = 총승부계수['승']/진행횟수
        for 행동 in ['gawi','bawi','bo']:
            행동확률[행동] = 행동계수[행동]/진행횟수
            if 총승부계수['승'] == 0: # 총승부 계수가 0일 경우 계산을 위해 임의로 매우 낮은 활률을 입력
                승부행동확률[행동] = 승부행동계수[행동] / 0.0000001
            else:
                승부행동확률[행동] = 승부행동계수[행동]/총승부계수['승']
    return 승률,행동확률,승부행동확률

def 거울(손모양):
    """입력값의 반대되는 값을(승리값)반환해"""
    if 손모양 == 'gawi':
        return 'bawi'
    elif 손모양 == 'bawi':
        return 'bo'
    else:
        return 'gawi'

def 거울2(손모양):
    """입력값의 반대되는 값을(패배값)반환해"""
    if 손모양 == 'gawi':
        return 'bo'
    elif 손모양 == 'bawi':
        return 'gawi'
    else:
        return 'bawi'

def show_me_the_hand(전적):
    # 30회 까지는 임의로 가위바위적
    내전적 = []
    내전적 += 내전적추적(전적)
    if len(내전적) == 0:
        print(내전적)
        return 'gawi'
    elif len(내전적) < 30:
        if len(내전적) < 15:
            print(내전적)
            if 내전적[-1][0] == 'gawi':
                return 'bawi'
            elif 내전적[-1][0] == 'bawi':
                return 'bo'
            elif 내전적[-1][0] == 'bo':
                return 'gawi'
        else:
            if 내전적[-1][0] == 'bawi':
                return 'bo'
            elif 내전적[-1][0] == 'gawi':
                return 'bawi'
            else:
                return 'gawi'
    elif 500 < len(전적) <= 1000 and 전적분석(전적)[0]>0.4:
        try:
            승률, 행동확률, 승부행동확률 = 전적분석(전적)
            행동별승률 = {'gawi':0,'bawi':0,'bo':0}
            # 베이지안 확률로 각 행동별 승률을 구한다
            for 행동 in ['gawi', 'bawi', 'bo']:
                if 행동확률[행동] == 0:
                    행동별승률[행동] = 승률 * 승부행동확률[행동] / 0.3333333
                else:
                    행동별승률[행동] = 승률*승부행동확률[행동]/행동확률[행동]
            # 적에게 승률이 제일 높은 값의 반대값으로 리턴함
            상대방예상값 = sorted(행동별승률.items(), key=itemgetter(1),reverse=True)[0][0]
            return 거울(상대방예상값)
        except:
            return 'bawi'
    else:
        try:
            승률, 행동확률, 승부행동확률 = 전적분석(내전적)
            행동별승률 = {'gawi':0,'bawi':0,'bo':0}
            # 베이지안 확률로 각 행동별 승률을 구한다
            for 행동 in ['gawi', 'bawi', 'bo']:
                if 행동확률[행동] == 0:
                    행동별승률[행동] = 승률 * 승부행동확률[행동] / 0.3333333
                else:
                    행동별승률[행동] = 승률*승부행동확률[행동]/행동확률[행동]
            # 적에게 승률이 제일 높은 값의 반대값으로 리턴함
            상대방예상값 = sorted(행동별승률.items(), key=itemgetter(1),reverse=True)[0][0]
            return 상대방예상값
        except:
            return 'bawi'
```

#### 연산자 오버로딩을 이용한 어뷰징 by 아무개

`==` 연산자를 오버로딩해서 상대의 손을 확인하고,
`__str__`(문자열 형변환) 연산자를 오버로딩해서 항상 이기는 손을 내는 **객체를 리턴**하는 어뷰징(?)입니다.
이벤트 소개 페이지의 pseudo code에서는 효과가 있었겠지만,
실제 게임 진행 서버에서는 (상대방이 정상이라면) 항상 부전패입니다^^;
이 방식의 또 다른 문제점은 내가 항상 `==` 연산자의 앞에 온다는(left-hand operand) 보장이 없다는 거죠.

심사 초반에 이 코드를 보지 않았다면, 어뷰징에 대해서 생각도 못했을텐데...
덕분에 다른 어뷰징들도 찾아보는 계기가 된 코드입니다.

```python
class Gawibawibo:
    def __init__(self, switch):
        import time
        select = ['gawi', 'bawi', 'bo']
        self.my = select[int(str(time.time())[-1]) % 3]
        self.switch = switch

    def __eq__(self, your):
        if self.switch:
            if your == 'gawi':
                self.my = 'bawi'
            elif your == 'bawi':
                self.my = 'bo'
            elif your == 'bo':
                self.my = 'gawi'

            self.switch = False

            return False
        else:
            return self.my == your

    def __repr__(self):
        return self.my

    def __str__(self):
        return self.my

def show_me_the_hand(records):
    return Gawibawibo(True)
```

#### 모듈/함수 바꿔치기 by 아무개

파이썬 모듈 로더를 활용해서,
로딩된 모듈 중에 `show_me_the_hand` 함수가 있으면 항상 `bo`만 내는 함수로 바꿔치기 합니다.
물론 플레이어 자신은 항상 `gawi`만 내죠^^;

처음 계획한 서버-to-서버 HTTP 통신 방식이었으면 효과가 없었겠지만,
바뀐 로컬에서 실행하는 방식에서는 쉽게 막을 방법이 없었습니다.
그렇다고 약속한 게임 규칙을 임의로 바꿀 수도 없어서 고민했는데,
[ganadist]님이 급히 만들어주신 **플레이어 자신의 모듈만 로딩된 격리된 프로세스에서 함수를 실행하고 파이프로 결과를 주고 받는 방식**으로
게임 규칙 변경없이 무력화할 수 있었습니다.

```python
import os
import sys
import string

def suckzoo_fantastic_symbolic_func():
    pass

def show_me_the_hand(record):
    if sticky_note_exists():
        #read_modules()
        scan_modules_and_hijack()
        remove_sticky_note()
    return 'gawi'

def scan_modules_and_hijack():
    for module in sys.modules:
        if not sys.modules.get(module):
            continue
        if sys.modules[module].__dict__.get('show_me_the_hand') and \
                not sys.modules[module].__dict__.get('suckzoo_fantastic_symbolic_func'):
            sys.modules[module].show_me_the_hand = lambda r: 'bo'

def remove_sticky_note():
    global sticky_note
    os.remove(sticky_note)

def sticky_note_exists():
    global sticky_note
    dir_ls = os.listdir(os.getcwd())
    return sticky_note in dir_ls

def leave_sticky_note():
    global sticky_note
    with open(sticky_note, 'a') as f:
        f.write('before injecting a lambda\n')

#if not read_modules():
scan_modules_and_hijack()
sticky_note = 'suckzoo_fantastic_rsp_sticky_note'
leave_sticky_note()
```

#### 모듈 사전 로딩 & 학습 by 아무개

현재 디렉토리의 모든 모듈을 `.py` 파일을 미리 로딩해서 각각 1000번의 결과를 학습하고,
학습된 결과에 기반해 자신의 손을 결정하는 방식입니다.

기발한 아이디어 였지만, 허무하게도... `random` 사용 금지 규칙에 따라... 서류 전형에서 탈락!! 참가상도 못받아가셨네요 ㅠㅠ
그냥 `time() % 3`이라도 하시지...

```python
import sys
import types
import glob
from os.path import dirname, basename, isfile
from random import choice
from collections import Counter

pyfiles = glob.glob(dirname(__file__) + '/*.py')
def loader(name):
    globals()[name] = __import__(name, globals(), locals(), [], -1)

map(loader, [basename(f)[:-3] for f in pyfiles if isfile(f)])

def opponent():
    thismodule = sys.modules[__name__]
    modulenames = set(sys.modules) & set(globals())
    allmodules = [sys.modules[name] for name in modulenames]
    print(allmodules)
    for val in allmodules:
        if isinstance(val, types.ModuleType)\
            and 'show_me_the_hand' in dir(val)\
            and val is not thismodule:
                return val

def train(player):
    occurance = ('gawi', 'bawi', 'bo')
    results = (1, 0, -1)
    records = [(choice(occurance), choice(results)) for x in range(1000)]
    return player.show_me_the_hand(records)

def show_me_the_hand(records):
    COUNTER = {'gawi': 'bawi', 'bawi': 'bo', 'bo': 'gawi'}
    try:
        # if opponent module is accessable?
        p1 = opponent()
        c = Counter([train(p1) for x in range(1000)])
        hand, priority = c.most_common().pop(0)
        return COUNTER.get(hand)
    except:
        try:
            loser = [w for (w, r) in records if f == -1]
            c = Counter(loser)
            hand, priority = c.most_common().pop(0)
            return COUNTER.get(hand)
        except:
            return choice(COUNTER.keys())
```

이 외에도, 수알못 파알못 - 수학을 전혀 모르는 파이썬 초보인 제 수준으로는
의도 파악조차 힘든 멋진 코드들이 많았지만,
깃헙에 올려둔 [게임 진행 서버]의 소스 코드로 대신하며, 코드 리뷰(구경?)를 마칩니다.

## CODING BATTLE 가위바위보!를 돌아보며...

예능으로 시작했다가 다큐로 끝난다더니, 이번 가위바위보 이벤트가 바로 그랬습니다.

부족한 이벤트에 큰 호응을 보여주신 많은 참가자 분들과 이벤트 진행과 준비에 고생한 운영자 분들께 감사드립니다.
통큰 스폰서로 개발자들에게 꿈과 희망, 그리고 좌절(?)을 선물해주신 회사 측에도 감사드립니다.
특히, 급하게 요청드렸음에도 기꺼이 코드를 만들어주신 [outsider]님과 [ganadist]님께 감사드립니다.

<img src="http://item.kakaocdn.net/do/-26p06+UqCd0OAgiRHNZwHaq4FJCveCBKCNZV-bZscw_/01a3b97731f42b4efc929ebd7fa376431667fc7b08261b4c493670baa83d5cb9" class="hcenter" />

긴 글, 끝까지 읽어주셔서 감사합니다. 이 한마디를 전하며 긴 글을 마칩니다.

> may the **PYTHON** be with you...

[PyCon 2016 APAC]:https://www.pycon.kr/2016apac/ 
[게임 진행 서버]:https://github.com/kakao/pycon2016apac-gawibawibo
[outsider]:https://blog.outsider.ne.kr
[ganadist]:https://github.com/ganadist
