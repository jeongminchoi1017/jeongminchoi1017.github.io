---
layout: single
title:  "Nested Loop"
categories: SQLD
tags: [database, SQLD]
author_profile: false
sidebar:
  nav: "counts"
---
2개 이상의 테이블에서 하나의 집합을 기준으로 순차적으로 상대방 Row를 결합하여 원하는 결과를 조합하는 조인방식.
조인해야 할 데이터가 많지 않은 경우에 유용하게 사용.
드라이빙 테이블로 한 테이블을 선정하고 이 테이블로부터 where 절에 정의된 검색 조건을 만족하는 데이터들을 걸러낸 후 이 값을 가지고 조인 대상 테이블을 반복적으로 검색하면서 조인 조건을 만족하는 최종 결과값을 얻어냄.

- 장단점
  인덱스에 의한 랜덤 엑세스에 기반하고 있기 때문에 대량의 데이터 처리 시 적합하지 않음
  Driving Table로는 데이터가 적거나 where절 조건으로 row의 숫자를 줄일 수 있는 테이블이어야 함.
  Driven Table에는 조인을 위한 적절한 인텍스가 생성되어 있어야 함.
  선행 테이블의 결과를 통해 후행 테이블을 엑세스 할 때 랜덤 I/O가 발생.

for(i = 0; i < N; i = i+1)
for(j = 0; j < M; j=j+1)
if(직원_부서코드[i] == 부서_부서코드[j]){  }