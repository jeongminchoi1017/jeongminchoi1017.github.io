---
layout: single
title:  "순위함수(RANK Function)"
categories: SQLD
tags: [database, SQLD]
author_profile: false
sidebar:
  nav: "counts"
---
- 윈도우 함수는 특정 항목과 파티션에 대해서 순위를 계산할 수 있는 함수를 제공한다.
- 순위 함수는 RANK, DENSE_RANK, ROW_NUMBER 함수가 있다.


### 순위(RANK)관련 윈도우 함수

| 순위함수       | 설명                                                 |
| ---------- | -------------------------------------------------- |
| RANK       | - 특정항목 및 파티션에 대해서 순위를 계산한다. - 동일한 순위는 동일한 값이 부여된다. |
| DENSE_RANK | 동일한 순위를 하나의 수로 계산한다.                               |
| ROW_NUMBER | 동일한 순위에 대해서 고유의 순위를 부여한다.                          |
