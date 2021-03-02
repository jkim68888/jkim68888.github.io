---
layout: post
title:  "JS es6의 변수선언 - let과 const"
date:   2021-03-02 15:50:46 +0900
categories: javascript
---

이번 포스팅에서는 Javascript es6의 변수선언 하는 방법에 대해서 정리하려고 한다.
<br>

## let과 const는 var와 무엇이 다른가?
<br>
자바스크립트는 원래 변수 선언할때 var를 사용한다. 하지만, es6 부터는 let과 const 라는 것으로 변수를 선언할 수 있다. let과 const는 왜 등장하게 되었으며, var와의 차이점이 무엇인지 알아보겠다.

- var 라는 변수 키워드가 let, 그리고 const와 다른 점은 var는 함수를 기준으로 전역변수와 지역변수가 처리된다는 것이다. 참고로 var는 재선언이 가능하다.
- let과 const는 함수가 아닌 코드블록을 기준으로 전역변수와 지역변수가 처리된다. 참고로 let과 const는 재선언이 불가능하다.
<br>

예시1)
<br>
<script src="https://gist.github.com/jkim68888/e4a105f57c0290651f768b6f5e313c3e.js"></script>
위 코드에서 알 수 있듯이 var 키워드는 변수의 재선언이 가능하다.
<br>

예시2)
<br>
<script src="https://gist.github.com/jkim68888/edf87efe9d457b5fa35cbc40facbda40.js"></script>
위 코드에서 알 수 있듯이 var 키워드는 함수를 기준으로 전역변수와 지역변수가 처리된다.
<br>

예시3)
<br>
<script src="https://gist.github.com/jkim68888/14be7db37e608a5005e96877f5525839.js"></script>
위 코드에서 알 수 있듯이 let 키워드는 코드블록을 기준으로 전역변수와 지역변수가 처리된다. (const도 let과 마찬가지 이므로, 따로 예시를 들지는 않겠다.)
<br>

## 변수 값의 재할당
<br>
let 키워드는 값을 재할당하는 것이 가능하다. 하지만, const는 불가능하다.
<br>
코드
<script src="https://gist.github.com/jkim68888/93ff9f1920746511263ba7e09a767027.js"></script>
<br>

## const 추가 설명
<br>
1. const는 let과는 달리 값을 재할당하는 것이 불가능하다. const는 상수(constant)의 의미로 쓰인다. 따라서 재할당이 필요없는 경우, const를 사용해 불필요한 변수의 재사용을 방지하고, 재할당이 필요한 경우에는 let을 사용하는 것이 좋다.  
2. const는 값 자체를 변경하는 것은 불가능하지만, const에 객체가 선언되었을때는 값의 property를 변경하는 것은 가능하다. 만약 const에 배열이 선언되었다면 배열값의 일부를 변경하는 것 또한 가능하다. 
<br>
    - 예시
    <script src="https://gist.github.com/jkim68888/138f10436330125601937e6d3bfa0812.js"></script>

