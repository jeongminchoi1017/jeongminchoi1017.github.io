---
layout: single
title:  "WINDOWING"
categories: SQLD
tags: [database, SQLD]
author_profile: false
sidebar:
  nav: "counts"
---

| 구조                  | 설명                                 |
| ------------------- | ---------------------------------- |
| ROWS                | 부분집합인 윈도우 크기를 물리적 단위로 행의 집합을 지정한다. |
| RANGE               | 논리적인 주소에 의해 행 집합을 지정한다.            |
| BETWEEN~AND         | 윈도우의 시작과 끝의 위치를 지정한다.              |
| UNBOUNDED PRECEDING | 윈도우의 시작 위치가 첫 번째 행임을 의미한다.         |
| UNBOUNDED FOLLOWING | 윈도우 마지막 위치가 마지막 행임을 의미한다.          |
| CURRENT ROW         | 윈도우 시작 위치가 현재 행임을 의미한다.            |

```
ROWS BETWEEN UNBOUNDED PRECENDING
	AND UNBOUNDED FOLLOWING
```
=>전체 조회
```
ROWS BETWEEN UNBOUNDED PRECEDING
	AND CURRENT ROW
```
처음부터 CURRENT ROW까지의 합계 계산
