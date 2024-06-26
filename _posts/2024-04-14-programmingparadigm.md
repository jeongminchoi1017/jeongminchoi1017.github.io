---
layout: single
title:  "프로그래밍 패러다임"
categories: algorithms
tags: [programming paradigm]
author_profile: false
sidebar:
  nav: "counts"
---
: 프로그래머에게 프로그래밍의 관점을 갖게 해주는 역할을 하는 개발 방법론.

***

![img.png]({{site.url}}/images/2024-04-14-programmingparadigm/img.png)

## 선언형과 함수형 프로그래밍

### 선언형 프로그래밍

‘무엇을’ 풀어내는가에 집중하는 패러다임.<br>
‘프로그램은 함수로 이루어진 것이다.’라는 명제가 담겨 있는 패러다임. 

### 함수형 프로그래밍

선언형 패러다임의 일종.<br>
‘순수함수’들을 블럭처럼 쌓아 로직을 구현, ‘고차함수’를 통해 재사용성을 높인 프로그래밍 패러다임.<br>
ex) 자바스크립트

- 순수함수 : 출력이 입력에만 의존하는 것을 의미. 

```
  const pure = (a, b) => {
	  return a+b
  }
```

- 고차함수 : 함수가 함수를 값처럼 매개변수로 받아 로직을 생성할 수 있는 것.<br>
  이때 고차 함수를 쓰기 위해서는 해당언어가 일급 객체라는 특징을 가져야 하며 그 특징은 다음과 같다.

  - 변수나 메서드에 함수를 할당할 수 있음.
  - 함수 안에 함수를 매개변수로 담을 수 있음.
  - 함수가 함수를 반환할 수 있음.

## 객체지향 프로그래밍(OOP, Object-Oriented Programming)
객체들의 집합으로 프로그램의 상호 작용을 표현하며 데이터를 객체로 취급하여 객체 내부에 선언된 메서드를 활용하는 방식.<br>
설계에 많은 시간이 소요되며 처리 속도가 다른 프로그래밍 패러다임에 비해 상대적으로 느림. 

### 객체지향 프로그래밍의 특징
#### 추상화
복잡한 시스템으로부터 핵심적인 개념 또는 기능을 간추려 내는 것을 의미. 
#### 캡슐화
객체의 속성과 메서드를 하나로 묶고 일부를 외부에 감추어 은닉하는 것. 
#### 상속성
상위 클래스의 특성을 하위 클래스가 이어받아서 재사용하거나 추가, 확장하는 것.<br>
코드의 재사용 측면, 계층적인 관계 생성, 유지 보수성 측면에서 중요. 
#### 다형성
하나의 메서드나 클래스가 다양한 방법으로 동작하는 것.<br>
대표적으로 오버로딩과 오버라이딩이 있음

- 오버로딩<br>
  같은 이름을 가진 메서드를 여러 개 두는 것.<br>
  메서드의 타입, 매개변수의 유형, 개수 등으로 여러 개를 둘 수 있으며 컴파일 중에 발생하는 ‘정적’ 다형성.
```java
  class Person {
  public void eat(String a) {
    System.out.println("I eat "+a);
  }

  public void eat(String a, String b) {
    System.out.println("I eat "+a+" and " + b);
  }
}
public class CalculateArea {
  public static void main (String[] args) {
    Person a = new Person();
    a.eat("apple");
    a.eat("tomato", "phodo");
  }
}
/*
	I eat apple
	I eat tomato and phodo
*/
```
- 오버라이딩<br>
  주로 메서드 오버라이딩을 말하며 상위 클래스로부터 상속 받은 메서드를 하위 클래스가 재정의하는 것을 의미함.

```java
  class Animal {
  public void bark(){
    System.out.println("mumu! mumu!");
  }
}

class Dog extends Animal {
  @Override
  public void bark() {
    System.out.println("wal!!! wal!!!");
  }
}

public class Main {
  public static void main(String[] args) {
    Dog d = new Dog();
    d.bark();
  }
}
/*
	wal!!! wal!!!
*/
```

### 설계원칙
객체지향 프로그래밍을 설계할 때 SOLID 원칙을 지켜야함. 
#### 단일 책임 원칙(SRP, Single Responsibility Principle)
모든 클래스는 각각 하나의 책임만 가져야 한다. 
#### 개방-폐쇄 원칙(OCP. Open Closed Principle)
유지 보수 사항이 생긴다면 코드를 쉽게 확장할 수 있도록 하고 수정할 때는 닫혀 있어야 하는 원칙
#### 리스코프 치환 원칙(LSP, Liskov Substitution Principle)
프로그램의 객체는 프로그램의 정확성을 깨뜨리지 않으면서 하위 타입의 인스턴스로 바꿀 수 있어야 하는 것을 의미. 
#### 인터페이스 분리 원칙(ISP, Interface Segregation Principle)
하나의 일반적인 인터페이스보다 구체적인 여러 개의 인터페이스를 만들어야 하는 원칙. 
#### 의존 역전 원칙(DIP. Dependency Inversion Principle)
자신보다 변하기 쉬운 것에 의존하던 것을 추상화된 인터페이스나 상위 클래스를 두어 변하기 쉬운 것의 변화에 영향 받지 않게 하는 원칙. 

## 절차형 프로그래밍
로직이 수행되어야 할 연속적인 계산 과정으로 이루어져 있음. 일이 진행되는 방식으로 코드를 구현하기만 하면 되기 때문에 코드의 가독성이 좋으며 실행 속도가 빠름. → 계산이 많은 작업 등에 사용.

대표적으로 포트란을 이용한 대기 과학 관련 연산 작업, 머신 러닝의 배치 작업.

단점으로는 모듈화가 하기 어렵고 유지 보수성이 떨어진다는 점.

## 패러다임의 혼합

하나의 패러다임을 기반으로 통일하여 서비스를 구축하는 것도 좋은 생각이지만 여러 패러다임을 조합하여 상황과 맥락에 따라
패러다임 간의 장점만 취해 개발하는 것이 좋습니다. 