---
layout: post
title:  "JS es6 화살표함수와 this키워드"
date:   2021-03-02 17:30:46 +0900
categories: javascript
---

이번 포스팅에서는 Javascript es6의 새로운 함수문법인 화살표함수와 Javascript 문법에서의 this에 대해 알아보겠다.
<br>

## 화살표함수란?
<br>
화살표 함수는 기존 자바스크립트의 function을 간단하게 만든 것이다. 따라서 코드 길이가 짧으며 문법이 매우 간단하다. 
<br>

## 화살표함수와 기존함수의 문법 차이
<script src="https://gist.github.com/jkim68888/aa5d90c0b9feb1a8ace474b32bc893cc.js"></script>
<br>

## this 키워드
<br>
this는 자기 자신을 호출할 때 사용하는 키워드이다. 첫째, 전역에 this가 있다면 이때의 this는 전역객체 window를 의미한다. 이때, 일반 함수에 this키워드가 있다는 것은 함수를 호출하는 객체를 의미한다. 즉 여기서의 this는 window, document, 문서객체일 수도 있다. 하지만 화살표함수에서의 this는 무조건 전역객체 window로 처리된다. 둘째, 함수 내에서의 this는 함수를 호출하는 객체를 의미한다. 셋째, 메소드 내부에 this가 있다면 this는 메서드 내부에서 작성한 키워드이다. 넷째, 객체의 메서드에서 호출한 this는 메서드를 소유한 해당 객체를 의미한다. 마지막으로, 이벤트 내부에서의 this는 이벤트를 받는 객체를 의미한다. 
<br>


