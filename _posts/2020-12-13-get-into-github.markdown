---
layout: post
title:  "초보 github 시작하기(깃허브 사용법)"
date:   2020-12-13 21:17:46 +0900
categories: jekyll update
---
Github(깃허브) 사용법에 대하여 아주 쉽고 간단하게 설명을 하려고한다.
깃허브를 처음 접해본 사람으로써 사용방법이 쉽진 않다고 느꼈다. 그래서 최대한 쉽게 설명해 보았다.

## Step01
### git 다운로드
Github를 사용하기 위해서는 우선 git을 다운받아야한다. 다운은 <https://git-scm.com/book/ko/v2/%EC%8B%9C%EC%9E%91%ED%95%98%EA%B8%B0-Git-%EC%84%A4%EC%B9%98> 여기서 받으면 된다.

## Step02
### repository(저장소) 생성
깃허브 사이트에 접속한다. <https://github.com/> 이 링크로 들어가면 된다.
아직 github 계정이 없다면 Sign up 을 클릭하여 계정을 만든다.
이제 계정이 만들어졌다면 Repository를 들어가서 새로운 저장소를 만든다.
![이미지](https://user-images.githubusercontent.com/75922558/102015806-14a02280-3da1-11eb-9a7d-9619e9175909.JPG)
repository는 원격저장소 인데 보통 프로젝트를 올릴 공간이므로, repository name은 프로젝트명을 쓰는 것이 좋다. public에 체크되어있는 것은 그냥 놔두면 된다. public은 다른 사람들도 볼 수 있다는 뜻이다. description은 쓰고 싶으면 써도 되고, 밑에 체크 박스들은 체크 안해도 된다. create repository 를 하고 나면 저장소 생성 완료!

## Step03
### 저장소로 사용할 폴더 만들기
컴퓨터에 저장소로 사용할 폴더를 만들어 줘야한다. step02에서 만든 repository 이름으로 폴더 하나를 만드는 것 보다는, repository가 여러개 만들어질 것이므로 그 폴더들을 다 감싸고 있는 폴더를 하나 만드는 것이 좋다. 예를 들어
![이미지](https://user-images.githubusercontent.com/75922558/102016291-7a8da980-3da3-11eb-96ca-0ba3b32887be.JPG)
이렇게 git이라는 폴더를 하나 만들고,
![이미지](https://user-images.githubusercontent.com/75922558/102016303-94c78780-3da3-11eb-9c7f-1cbd24761d5b.JPG)
안에 repository이름의 폴더들을 넣어논다. 그 후, 깃허브에 올릴 파일들을 여기로 다 옮겨놓는다.

## step04
### cmd창에서 작업
윈도우 검색창에 cmd를 검색해서 cmd창을 열어준다.
여기서 step03에서 만든 폴더 위치로 들어가서 git init을 해줘야한다.
이때 위치로 찾아서 들어가때의 팁은 , cmd 창에 dir이라고 치면 현재 내 디렉터리에 있는 폴더들을 보여준다. cd는 쉽게 해석하자면 그 폴더로 들어가라는 뜻이다. ./는 현재폴더로 들어가는 것이고, ../는 이전폴더로 나가는것이다. 나는 내문서에 있는 git 폴더로 들어갔다.
![이미지](https://user-images.githubusercontent.com/75922558/102016716-972ae100-3da5-11eb-8906-4e1c173d3645.JPG)
그 후, cmd 창에 다음과 같이 따라서 써주면 된다.
1. git init
2. git add *
3. git commit -m "first commit"
4. git remote add origin (https://github.com/이라고 시작되는 자신의 https를 복사해서 붙여넣는다.)
5. git push -u origin master

### 이렇게 하면 완료!

