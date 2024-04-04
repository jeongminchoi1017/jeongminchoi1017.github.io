---
layout: single
title:  "업데이트 내역 실시간 확인"
categories: github_blog
tags: [blog, live_update]
toc: true
author_profile: false
sidebar:
  nav: "counts"
---

[실시간 업데이트 참고](https://www.youtube.com/watch?v=0TeHUqSAb6Q&list=PLIMb_GuNnFwfQBZQwD-vCZENL5YLDZekr&index=4)

### 아래 프로그램 설치

![img.png]({{site.url}}/images/2024-03-17-liveUpdate/img.png)

[루비 다운로드](https://www.ruby-lang.org/en/downloads/)


On Windows machines, you can use RubyInstaller.에 **RubyInstaller**클릭

![img.png]({{site.url}}/images/2024-03-17-liveUpdate/rubyinstall.png)
=>클릭 후 with devkit 아래 Ruby+Devkit(x64) 클릭

=> 설치 완료 후 창이 뜨면 MSYS2 and MINGW development toolchain (3)선택

### gem install 하기

=> 창을 끄고 cmd 실행(window + r(실행창 단축키), cmd 검색)

=>gem install jekyll

=>gem install bundler

=>프로잭트 폴더(나의 경우 jeongminchoi1017.github.io)에서 커맨드 창 열기<br/>
  shift+우클릭, 여기에 PowerShell 창 열기 클릭

=> bundle install

### 실행

=> bundle exec jekyll serve<br/>
  ※ webrick이 없다는 에러가 뜨면 bundle add webrick 명령어 입력 후 위 명령어 다시 실행

=> localhost:4000이 뜨면 실시간 업데이트 확인 가능!

### 실시간 반영을 확인할 수 있는 이유

로컬 서버를 이용하기 때문에 실시간 반영을 확인할 수 있다. 