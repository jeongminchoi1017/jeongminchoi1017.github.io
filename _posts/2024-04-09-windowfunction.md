---
layout: single
title:  "윈도우함수"
categories: SQLD
tags: [database, SQLD]
author_profile: false
sidebar:
  nav: "counts"
---
- 윈도우 함수는 행과 행 간의 관계를 정의하기 위해서 제공되는 함수이다.
- 윈도우 함수를 사용해서 순위, 합계, 평균, 행 위치 등을 조작할 수 있다.

```oracle
SELECT WINDOW_FUNCTION(ARGUMENTS)
	OVER(PARTICION BY 칼럼
		ORDER BY WINDOWING절)
```

### 윈도우 함수 구조

| 구조            | 설명                                                            |
| ------------- | ------------------------------------------------------------- |
| ARGUMENTS(인수) | 윈도우 함수에 따라서 0~N개의 인수를 설정한다.                                   |
| PARTITION BY  | 전체 집합을 기준에 의해 소그룹으로 나눈다.                                      |
| ORDER BY      | 어떤 항목에 대해서 정렬한다.                                              |
| [[WINDOWING]] | -행 기준의 범위를 정한다. - ROWS는 물리적 결과의 행 수이고 RANGE는 논리적인 값에 의한 범위이다. |
