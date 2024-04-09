---
layout: single
title:  "SuperType과 SubType"
categories: SQLD
tags: [database, SQLD]
author_profile: false
sidebar:
  nav: "counts"
---
- 기존 entity type에서 중복되는 attribute와 특징이 되는 attribute를 나눠 entity type을 나누는 것을 말한다.
- 상위집단, 하위집단으로 나누는 것.
- UML(Unified Modeling Language)에서 Generalization과 Specialization을 생각하면 된다.

- Supertype : 하나 이상의 entity type에서 공통적으로 뽑히는 entity type. SubType의 일반화된 버전을 생각하면 된다. 상위집단이라고 생각하면 된다.
- Subtype : 다른 하위집단들과 별개되는 attribute를 가지는 entity type으로 entity집합이다. 하위집단이라고 생각하면 된다.

- 특징
  각각의 subtype들은 supertype의 attribute들과 relation들을 상속받는다.
  Subtype들은 스스로의 유니크한 attribute를 갖는다.


### 슈퍼타입 및 서브 타입 변환 방법

| 변환방법      | 설명                                                                                                            |
| ------------- | --------------------------------------------------------------------------------------------------------------- |
| OneToOne Type | - 슈퍼타입과 서브 타입을 개별 테이블로 도출한다. - 테이블의 수가 많아서 조인이 많이 발생하고 관리가 어렵다.     |
| Plus Type     | - 슈퍼타입과 서브 타입 테이블로 도출한다. - 조인이 발생하고 관리가 어렵다.                                      |
| Single Type   | - 슈퍼 타입과 서브 타입을 하나의 테이블로 도출한다. - 조인 성능이 좋고 관리가 편리하지만, 입출력 성능이 나쁘다. |
