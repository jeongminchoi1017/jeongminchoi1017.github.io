---
layout: single
title:  "복잡도"
categories: algorithms
tags: [data_structure, complexity, algorithms]
author_profile: false
sidebar:
  nav: "counts"
---
# 시간 복잡도
```
문제를 해결하는 데 걸리는 시간과 입력의 함수 관계. 
어떠한 알고리즘의 로직이 '얼마나 오랜 시간'이 걸리는지를 나타내는 데 쓰이며,
보통 빅오 표기법으로 나타냄. 
```
## 빅오 표기법

입력 범위 n을 기준으로 해서 로직이 몇 번 반복되는지 나타내는 것.
'가장 영향을 많이 끼치는' 항의 상수 인자를 빼고 나머지 항을 없앤 것. 
입력 크기가 커질수록 연산량이 가장 많이 커지는 항은 n의 제곱항이고, 
다른 것은 그에 비해 미미하기 때문에 이것만 신경 쓰면 된다는 이론. 

## 시간복잡도의 존재 이유
**효율적인 코드로 개선하는 데 쓰이는 척도가 됨.**

![Pasted image 20240131114351.png]({{site.url}}/images/2024-04-01-complexity/Pasted image 20240131114351.png)

O(1)과 O(n)은 입력 크기가 커질수록 차이가 많이 나는 것을 볼 수 있음. 
즉, O(n<sup>2</sup>)보다는 O(n), O(n)보다는 0(1)을 지향해야 함.

# 공간 복잡도
```
프로그램을 실행시켰을 때 필요로 하는 자원 공간의 양. 
정적 변수로 선언된 것 말고도 동적으로 재귀적인 함수로 인해 공간을 계속해서 필요로 할 경우도 포함. 
```

# 자료구조에서의 시간 복잡도

지료 구조를 쓸 때는 이러한 시간 복잡도를 잘 생각해야 함.
보통 시간 복잡도를 생각할 때 **평균**, 그리고 **최악의 시간 복잡도**를 고려하면서 씀.

![Pasted image 20240131120001.png]({{site.url}}/images/2024-04-01-complexity/Pasted image 20240131120001.png)
![Pasted image 20240131120002.png]({{site.url}}/images/2024-04-01-complexity/Pasted image 20240131120022.png)