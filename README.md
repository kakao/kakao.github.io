# 오픈소스 가이드

카카오는 <strong>'개발자들이 오픈소스를 잘 사용하고 오픈소스에 기여할 수 있도록 돕는다'</strong>를 목표로 오픈소스를 가이던스 하고 있습니다.<br>  
이 오픈소스 가이드가 오픈소스의 가치를 이해하고, 오픈소스를 올바르게 사용하고 기여하는데 도움이 되기를 바랍니다.


# 설치
## 사전 준비
[GitHub Pages](https://pages.github.com/)와 [Jekyll](https://jekyllrb.com/)에 대하여 충분히 알고
[Collaborating with pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests)의 내용에 대하여 충분히 이해합니다.

## 설치
### [kakao.github.io](https://github.com/kakao/kakao.github.io) 에 push 권한이 있다면
1. git fetch or pull or clone
2. [Jekyll](https://jekyllrb.com/) 설치 
```console
$ git clone git@github.com:kakao/kakao.github.io.git
$ cd kakao.github.io
$ bundle install
```

### [kakao.github.io](https://github.com/kakao/kakao.github.io) 에 push 권한이 없다면:
1. <https://github.com/kakao/kakao.github.io> 에서 `Fork` 버튼 클릭
2. Fork 저장소 계정 선택
3. git fetch or pull or clone
4. Fork 설정 [Configuring a remote for a fork](https://docs.github.com/ko/pull-requests/collaborating-with-pull-requests/working-with-forks/configuring-a-remote-repository-for-a-fork)
5. Fork 동기화 [Syncing a fork](https://docs.github.com/ko/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork)
6. [Jekyll](https://jekyllrb.com/) 설치
```console
$ git clone git@github.com:YOUR_GITHUB_ACCOUNT/kakao.github.io.git
$ cd kakao.github.io
$ git remote add upstream git@github.com:kakao/kakao.github.io.git
$ git fetch upstream
$ git checkout main
$ git merge upstream/main
$ bundle install
```

### 로컬 실행
```
$ bundle exec jekyll serve
$ open http://localhost:4000
```

### 배포(발행)

#### [kakao.github.io](https://github.com/kakao/kakao.github.io) 에 push 권한이 있다면:
```
$ git commit -m '...'
$ git push origin main
````

#### [kakao.github.io](https://github.com/kakao/kakao.github.io) 에 push 권한이 없다면:
1. Fork 동기화 [Syncing a fork](https://docs.github.com/ko/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork)
2. Pull Request 보내기 [Creating a pull request](https://docs.github.com/ko/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)


## 기여 ✨
카카오 오픈소스 가이드는 모든 기여를 환영합니다.<br/>
이 프로젝트에 대한 자유로운 의견이나 버그 리포팅, 기능 등을 추가하고자 한다면 [Pull Requests](https://github.com/kakao/kakao.github.io/pulls)로 제출해주세요.

## 기여 지침
다음은 카카오 오픈소스 가이드 프로젝트에 기여하기 위한 일련의 지침입니다.<br>
카카오 오픈소스 가이드 프로젝트 개선에 참여할 방법을 알아보려면 [CONTRIBUTING.md](./CONTRIBUTING.md) 를 참고해 주세요.<br>
기여나 개선은 [Pull Requests](https://github.com/kakao/kakao.github.io/pulls) 와 [GitHub Issues](https://github.com/kakao/kakao.github.io/issues)로 만들어 제출할 수 있습니다.<br/>
카카오 오픈소스 가이드 프로젝트에 참여하는 모든 사람은 [Code of Conduct](./CODE_OF_CONDUCT.md)의 적용을 받습니다.<br>

카카오 오픈소스 가이드에 [기여를 해주신 분](https://github.com/kakao/kakao.github.io/graphs/contributors)들께 미리 감사드립니다.❤️

## License
This software is licensed under the [MIT license](./LICENSE), quoted below.

Copyright 2023 Kakao Corp. [http://www.kakaocorp.com](http://www.kakaocorp.com/)

### ❕caution
>This Kakao Open Source Guide document and other content is licensed under the [Creative Commons BY 4.0 license](./CC-BY-4.0).
>카카오 오픈소스 가이드의 문서 및 기타 콘텐츠에 대하여 [Creative Commons BY 4.0](./CC-BY-4.0) 라이선스를 적용합니다.


## 테마
- Just the Docs : https://github.com/just-the-docs/just-the-docs
