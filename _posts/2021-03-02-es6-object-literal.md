---
layout: post
title:  "JS es6 향상된 객체 리터럴"
date:   2021-03-02 18:02:46 +0900
categories: javascript
---

이번 포스팅에서는 Javascript es6의 향상된 객체 리터럴(Enhanced Object Literal)에 대해서 정리할것이다. 
<br>

## 리터럴이란?
<br>
리터럴이란 소스 코드의 고정된 값을 대표하는 용어이며 변하지 않는 값(데이터)를 의미한다. 상수 또한 변하지 않는 값이지만, 리터럴은 상수와 조금 다르다. 상수는 변하지 않는 변수를 의미하며(메모리 위치) 메모리 값을 변경할 수 없다. 반면 리터럴은 변수의 값이 변하지 않는 데이터(메모리 위치안의 값)를 의미한다. 
<br>

## 향상된 객체 리터럴이란?
<br>
객체 리터럴이란 중괄호 {} 로 감싸진 하나 이상의 속성 이름과 속성 값의 리스트라고 말할 수 있다. 향상된 객체 리터럴이란 기존 자바스크립트에서 사용하던 객체 정의 방식을 개선한 문법이다. 
<br>
<script src="https://gist.github.com/jkim68888/6e28a329d331009e4a0532acb0abf67a.js"></script>
이것이 기존의 객체를 정의하는 방식이다. 
<br>

<script src="https://gist.github.com/jkim68888/5b5a75b98a3ee9bb217e6fe877e7fd69.js"></script>
향상된 객체 리터럴은 위의 코드처럼 기존 변수명과 객체의 속성명이 같으면 값을 작성하지 않아도 된다.
<br>

<script src="https://gist.github.com/jkim68888/d43f4a392d67af79af7ce4866e5f8834.js"></script>
또한 위의 코드처럼 메서드 작성시 function 생략가능하다. 





