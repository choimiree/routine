[TOC]



### git

(분산)버전 관리 시스템. 

### DVCS(Distributed Version Control System)

- git이 없다면, 이 자료 간에 뭐가 바뀌었는지 차이를 알 수 없다. 

- git이 있다면, 차이가 무엇이고 수정 이유를 log로 남길 수 있다. 

ex) 뼈대 코드 구성, 메인 기능 구현, 로그인 기능 구현, 채팅 기능 구현, 디자인 적용...

현재 파일들을 안전한 상태로 과거 모습 그대로 복원 가능. 각 버전별 차이점만 저장해서 사이즈 감소.

- 리눅스: 오픈소스를 처음으로. 
- **리누스 토르발스**: 리눅스 & git 만든 아저씨

#### git 작업 흐름

- add: 커밋할 목록에 추가

- commit: 커밋 만들기

- push: 현재까지의 역사

working directory -(**add**)-> 커밋할 목록 -(**commit**)-> 쌓인 커밋들-(push)-> GitHub 

##### git의 기본

![](C:\Users\multicampus\Desktop\KakaoTalk_20200120_092528661.jpg)



##### git bash 설치

- git bash에서 pwd 치면 저장되는 위치 보여준다.
- ![](C:\Users\multicampus\Desktop\working directory.PNG)

- ls라 치면 working directory에 뭐 있는 지 알려줌

- clear = Ctrl+L : 정리됨.

- cd touch a.txt : a파일이 생성됨 / rm a.txt : a파일 지워짐

- mkdir test : test 목록이 생성됨 / rm -r test : test 목록 지워짐

- cd : root로 감 / cd ~ : home directory로 돌아갈 수 있음

  **내가 어디서 작업을 하고 있느냐가 제일 중요**

- cd .. : 상위 폴더로 이동하기

- cd - : 바로 직전의 폴더로 이동

- git config --global user.name : user name 입력

- git config --global user.email : gmail 입력

- git init은 딱 한 번만. 관리할 폴더 최상단에. git init한 폴더에 만든 것만 저장된다.

- git status: add를 했는지 확인하는 장치. 수시로 찍어봐야됨.

  **수정사항 있을 때 확인 순서**

git add -> git status(상태확인) -> git commit -m "이름" -> git status(상태확인) -> git log



##### github

: git에서 만든 것을 다른 사람들과 공유하기 위해 만들어짐

**gitignore** : 개인정보와 같은 공유하고 싶지 않은 것 설정할 때 사용.

- git add . : 현재 있는 모든 파일을 stage에 올려주는 것.
- git remote add origin/ git remote -v : github이랑 연결.



TIL - 수업 외적인 공부(public)

lectures - 수업내용 정리(private)



* * git init
  * git add . 
  * git commit -m "commit message"
  * git remote add origin <해당 깃헙 url>
  * git remote -v :remote 된 주소 확인
  * git push -u origin master

* 1. 반드시 commit 이후에 매번 push 할 필요는 없다.

  2. `git push -u origin master` 이후에 push는 명령어가 그냥 `git push`라고만 해도 된다.

     단, `git push origin master` 이렇게 하면 계속 같은 명령어를 사용해야 한다.

* 집에서 학원에서 했던 거 github에서 가져올 때는 clone을 해야하는데 그때는 init 따로 안해줘도 (master) 되어 있다.



