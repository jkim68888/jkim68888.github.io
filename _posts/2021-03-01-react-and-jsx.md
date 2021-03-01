---
layout: post
title:  "React 개발환경 구축 및 JSX 기초문법"
date:   2021-03-01 21:16:46 +0900
categories: TIL
---

오늘은 React로 개발하기 위한 환경을 구축하는 방법을 정리한 후, 기초적인 JSX 문법을 정리하려고 한다.


## React 개발환경 구축

<br>

1. node.js 를 설치한다. (node.js를 설치해야 npm이라는 툴을 사용할 수 있으며, npm으로 create-react-app 을 간편하게 설치할 수 있다.)
2. 코딩 에디터를 설치한다. (나는 vsCode를 사용하였다.) 
3. VScode에 터미널을 열어서 <span style="color:#ffffff, background-color:#000000">npx create-react-app 폴더명</span> 을 입력한다.  
4. 폴더가 생성되면 터미널에서 <span style="color:#ffffff, background-color:#000000">cd 폴더명</span> 을 입력하여 해당 폴더 내부로 들어가서 <span style="color:#ffffff, background-color:#000000">npm start</span> 를 입력한다. 이렇게 하면 미리보기가 실행될것이다.
5. 미리보기가 실행됬다면, 파일에서 코드를 작성하여 뷰를 구현한다. 이때, "App.js" 를 html처럼 사용하면 된다.

<br>

## JSX 문법

<br>

1. 리액트는 데이터 바인딩 할때에 중괄호 안에 변수명, 함수 등을 쓰면 된다. 

    - 예시
    <script src="https://gist.github.com/jkim68888/7cf536828640ba638f5e1ce388ac1ff5.js"></script>

<br>

2. 클래스를 쓰고 싶을 때에는, <span style="color:blue">__className__<span>으로 클래스를 만든다. 

3. JSX에서 style 속성을 넣을때, 속성명은 대시[-]를 사용하는것이 아닌 카멜표기법으로 사용하여야한다.

    - 예시
    <script src="https://gist.github.com/jkim68888/316da9f0b944551ae23b92c30ca4730b.js"></script>

<br>
  
4. 데이터를 보관하는 방법에는 두가지가 있다.
<br>
    1. 데이터를 변수에 넣기
    2. 데이터를 State에 넣기
<br>
데이터를 변수에 담아서 선언하는 방식은 익숙하므로, State에 대해서 자세하게 알아보도록 하겠다.
<br>
- State를 만드는 방법
<br>
<script src="https://gist.github.com/jkim68888/0545eef5b96e0d3a0f2e3ed14541192b.js"></script>
<br>
이때, a에는 데이터값이 저장되고 b에는 데이터가 변경되는 함수가 들어간다.
<br>
useStat() 안에는 *문자, 숫자, array, object* 모두 저장 가능하다. 
<br>

-State에 데이터를 저장해놓는 이유
    - state는 값이 변경될때에 HTML이 자동으로 재랜더링이 된다. 따라서 변화하는 값을 관리하기 편리하다.

<br>
예제1
- 첫번째 글제목을 출력하고, 글제목 옆의 ❤ 클릭시 좋아요 수가 올라가게 하라.
<script src="https://gist.github.com/jkim68888/7e9b64140b1c9d025e4603c03a713383.js"></script>
<br>
- 클릭이벤트를 주고 싶으면, 태그 안에 <span style="color:#ffffff, background-color:#000000">onClick={ () => {실행할내용} }</span> 또는 함수를 선언한후 태그 안에 <span style="color:#ffffff, background-color:#000000">onClick = { 함수() }</span> 이렇게 사용하면 된다. 이때 주의점은 onclick 을 카멜표기법인 onClick 으로 써야한다.  

<br>

예제2
- 첫번째 글제목을 '남자옷가게' 에서 '여자옷가게'로 바뀌어 출력되게 하라. 
<script src="https://gist.github.com/jkim68888/e5305cbf846b10da12b9d7de8122dd7f.js"></script>
<br>
- 제목바꾸기() 함수를 선언하여 기존 state를 deepCopy 하여 값을 변경해주었다.
- deepCopy 란 값 공유가 일어나지 않고 서로 독립적인 값을 가지도록 복사하는 것이다. 


5. Component 문법

- component는 HTML을 줄여서 쓸 수 있도록 해준다. 
- component의 이름은 대문자로 시작한다.
- return() 안에 있는 건 태그 하나로 묶어야 한다. 예를 들면 div 태그로 한번 감싸주거나 fragment 로 한번 감싸주어야 한다.
<br>

- 어떤 것을 component로 만드는게 좋을까?
    - 반복 출현하는 HTML
    - 자주 변경되는 HTML
    - 다른 페이지를 만들때
<br>

- component의 단점
    - state를 쓸때 복잡해진다. 상위 컴포넌트에서 만든 state를 쓰려면 props 문법을 사용해야 한다.