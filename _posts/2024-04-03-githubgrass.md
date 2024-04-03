---
layout: single
title:  "github 잔디밭 안 심기는 현상 고치기"
categories: github_blog
tags: [gihub_blog, grass, error]
author_profile: false
sidebar:
  nav: "docs"
---

<div class="notice--warning">
  <h4>참고사항</h4>
  <ul>
    <li>
      이 글은 업로드 날짜가 어떻게 설정되는지 확인하기 위해 4월3일에 쓰고 파일은 4월4일로 만들었음.<br>
      -> 오늘 날짜가 아닌 내일 날짜로 올리니 블로그에 글이 올라가지 않는 것을 알았습니다. <br>
      그래서 다시 파일이름을 바꾸어 보았습니다. <br>
      잘 올라간 걸 확인할 수 있었지만 선형자료구조 내용보다 아래 작업된 것으로 보여지는 문제가 있었습니다.<br>
      이부분에 대해서는 좀 더 확인이 필요할 것 같습니다.
    </li>
  </ul>
</div>

# 문제

현재 github 계정을 새로 만들어서 텅빈 잔디를 가지고 있습니다.

그렇지만 저는 잔디를 잘 쌓아가고 싶단 욕심으로 **github blog를 하면 매일 잔디를 깔 수 있을 거야!**

라며 깃허브 블로그를 생성했습니다. 

하지만 이게 웬걸,

![문제점]({{site.url}}/images/2024-04-03-githubgrass/img.png)

난 열심히 커밋을 하고 블로그 글을 업로드 했는데 **없다!**

![img.png]({{site.url}}/images/2024-04-03-githubgrass/CyM0EaOVIAI4fOQ.jpg)

## 왜 잔디가 심어지지 않을까? 

먼저 블로그의 경우 github desktop을 이용했는데<br>
이게 이유일까 싶어 bash를 이용한 커밋을 해도 전혀 반영되지 않았습니다. 

이 문제를 해결하기 위해 구글링을 해보았습니다.

먼저, **이메일과 이름이 github와 로컬이 맞지 않아 생기는 경우**

이 경우에는 간단하게 github 세팅에서 이메일을 확인한 후 

```
git config "이름"
git config "이메일"

// 그리고

git config --global "이름"
git config --global "이메일"

// 이런 식으로 설정 가능하다.
// 잘 설정됐는지 확인하려면 

git config --list

```
이렇게 진행하면 됩니다. 하지만 나의 경우 이 방식이 아니었습니다.

# 원인

**fork를 이용해 레포지토리를 만든 경우** 

깃허브 블로그를 시작할 때 템플릿을 이용하기 위해 fork로 레포지토리를 만든 것이 원인이었습니다.

독립형 저장소가 아니었기 때문에 커밋을 해도 잔디가 기록이 되지 않았습니다.

# 해결방안

1. 레포지토리를 삭제 후 새 레포지토리로 옮기는 방법

이 방법을 사용하는 것이 제일 간단해 보이고 익숙한 방법이었지만 내 커밋 기록이 아예 남아있지 않을 것 같다고 판단하였습니다.<br>
잔디를 까는 것이 제일 중요한 부분이었는데 이렇게 처음부터 사라지게 하기엔 아쉬워 다른 방법을 찾아봤습니다. 

2. chatbot-virtual-assistant을 사용해서 Fork된 레포지토리 분리 Ticket 제출하기

[참고한 블로그](https://jonghoonpark.com/2023/10/02/fork%ED%95%9C-github-%EC%A0%80%EC%9E%A5%EC%86%8C-%EB%B6%84%EB%A6%AC%ED%95%98%EA%B8%B0)<br>

[chatbot-virtual-assistant](https://support.github.com/contact?tags=rr-forks&subject=Detach%20Fork&flow=detach_fork)<br>

chatbot-virtual-assistant 링크를 클릭하면 창이 뜹니다.

우리는 레포지토리를 분리하고 싶으니 Detach/Extract를 클릭해줍니다.

그리고 어떤 레포짓토리를 분리하고 싶은지 나오는데 자신의 깃허브에 포크로 생성한 분리하고 싶은 레포지토리를 적어주면 됩니다.

이후 commit을 했는지 물어보면 yes를 클릭. 

어떤 이유로 분리하고 싶은지를 물어보면 처음에 있는 항목을 눌러주면 됩니다.

그렇게 하면 ticket을 생성해주고 저희는 기다리면 됩니다.

![img_1png]({{site.url}}/images/2024-04-03-githubgrass/img_1.png)

좀 오래 기다려야 돼서 아직 잘 되었는지는 확인이 불가능합니다.

만약 잘 되었다면 다시 글을 수정해 보겠습니다.

***
**2시간 뒤 수정**

# 해결완료

2시간 가량 지난 뒤 github를 확인해보니 

![img_2.png]({{site.url}}/images/2024-04-03-githubgrass/img_2.png)

fork한 repository라는 문구가 사라지고 

![이후]({{site.url}}/images/2024-04-03-githubgrass/img_3.png)

![이전]({{site.url}}/images/2024-04-03-githubgrass/img.png)

이렇게 커밋에 따라 달라진 모습을 볼 수 있었습니다.
이전 작업도 사라지지 않고 잘 심겨있었습니다. 

이렇게 해결 완료!