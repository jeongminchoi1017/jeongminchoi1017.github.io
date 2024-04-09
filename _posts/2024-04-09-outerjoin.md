---
layout: single
title:  "OUTER JOIN"
categories: SQLD
tags: [database, SQLD]
author_profile: false
sidebar:
  nav: "counts"
---
OUTER JOIN은 두 개의 테이블 간에 교집합(EQUI JOIN)을 조회하고 한쪽 테이블에만 있는 데이터도 포함시켜서 조회한다.
- 예를 들어 DEPT 테이블과 EMP 테이블을 OUTER JOIN 하면 DEPTNO가 같은 것을 조회하고 DEPT테이블에만 있는 DEPTNO도 포함시킨다.
- 이때 왼쪽 테이블에만 있는 행도 포함하면 LEFT OUTER JOIN이라고 하고 오른쪽 행만 포함시키면 RIGHT OUTER JOIN이라고 한다.
- FULL OUTER JOIN은 LEFT OUTER JOIN과 RIGHT OUTER JOIN 모두를 하는 것이다.
- Oracle 데이터베이스에서는 OUTER JOIN을 할 때 (+) 기호를 사용해서 할 수 있음.

## LEFT OUTER JOIN과 RIGHT OUTER JOIN
  LEFT OUTER JOIN은 두 개의 테이블에서 같은 것을 조회하고 왼쪽 테이블에만 있는 것을 포함해서 조회된다.
  RIGHT OUTER JOIN은 두 개의 테이블에서 같은 것을 조회하고 오른쪽 테이블에만 있는 것을 포함해서 조회된다.
## CROSS JOIN
  CROSS JOIN은 조인 조건구 없이 2개의 테이블을 하나로 조인한다.
  조인구가 없기 때문에 카테시안 곱이 발생한다.
  예를 들어 행이 14개 있는 테이블과 행이 4개 있는 테이블을 조인하면 56개의 행이 조회된다.
  CROSS JOIN은 FROM 절에 "CROSS JOIN"구를 사용하면 된다.

## UNION을 사용한 합집합 구현 
### UNION

  - UNION 연산은 두 개의 테이블을 하나로 만드는 연산이다.
  - 즉, 2개의 테이블을 하나로 합치는 것이다. 주의사항은 두 개의 테이블의 칼럼 수, 칼럼의 데이터 형식 모두가 일치해야 한다. 만약 두 개의 테이블에 UNION 현산이 사용될 때 칼럼 수 혹은 데이터 형식이 다르면 오류가 발생한다.
  - UINION 연산은 두 개의 테이블을 하나로 합치면서 중복된 데이터를 제거한다.
  - 그래서 UNION은 정렬(Sort) 과정을 발생시킨다.

### UNION ALL

  - UNION ALL은 두 개의 테이블을 하나로 합치는 것이다. UNION처럼 중복을 제거하거나 정렬을 유발하지 않는다.

### 차집합을 만드는 MINUS
  - MINUS 연산은 두 개의 테이블에서 차집합을조회한다. 즉, 먼저 쓴 SELECT문에는 있고 뒤에 쓰는 SELECT문에는 없는 집합을 조회하는 것이다.
  - MS-SQL에서는 MINUS와 동일한 연산이 EXCEPT이다. 