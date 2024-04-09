---
layout: single
title:  "CASCADE CONSTRAINTS"
categories: SQLD
tags: [database, SQLD]
author_profile: false
sidebar:
  nav: "counts"
---
- 데이터베이스 내의 임의의 다른 테이블과 PRIMARY KEY 또는 FOREIGN KEY로서의 관계가 여전히 존재하는 경우 PRIMARY KEY가 존재하는 테이블을 마음대로 제거 및 비활성화 할 수 없다.

DROP TABLE 테이블명 CASCADE CONSTRAINTS;
-> 강제로 참조관계를 끊고 부모 테이블을 삭제.

