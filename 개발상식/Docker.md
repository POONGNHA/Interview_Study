## 도커 공부!
[Docker](https://www.docker.com/)

## 도커 사용법 
1. 도커 데스크탑 설치
2. 내 이미지를 만들 도커파일을 만든다.
3. cli에서 도커 설정파일이 있는 폴더로 이동해서 [docker build -t 도커이름 .] 을 실행하여 빌드한다
4. 실행하여 포트를 설정해준다
5. cl에서 docker image ls쳐서 image list를 보고 docker tag 원래_이미지이름 내도커계정/바꿀_이미지이름 으로 이미지 이름을 바꿔준다
   내 도커계정/을 안붙여주면 권한문제가 발생한다
6. [Go로 구축해보기](https://docs.docker.com/language/golang/?uuid=EAC2BDBE-F907-49B4-BF5A-63F075D0DA35) 
  새로 GO언어를 사용해서 구축해보기로 해보았다. docker 자체가 go로 만들어져있기도하고, python과 java는 이미 알고있으니
  새로운 언어를 사용해보는것이 좋을것이라 생각하여 만들게되었다.
  조사결과는 java가 제일 좋을것이라 생각하지만 트랜드 세터가 되기위해서 새로운 언어를 채택하였다.
7. GO보다는 비동기방식에 백과 프론트 둘다 작성할 수 있는 node js 를 사용하기로 하였다. go보다 더 많이 사용하기도 하고,
   백과 프론트 둘 다 가능한 언어라는게 매력이라 생각해서 한번 배워볼려고 한다.
   노마드 코더가 사용하는 거 보면 한번쯤 사용해볼만한 언어라고 생각됨 [Node js](https://nodejs.org/ko/download)
8. (node js로 도커 구축하기)[https://docs.docker.com/language/nodejs/build-images]
9. 윈도우 파워쉘로 명령어를 쓰니 오류가 엄청 난다.![오류화면](https://github.com/POONGNHA/Interview_Study/assets/105198445/4dd2700b-7fb9-4d57-8d6e-6f79d7e4285f)
   걍 npm audit fix --force로 전부 실행시켜버렸다.
   찾아보니 vunarbility라고 해서 취약점이 발견된 소프트웨어나 버전업이 필요한 프로그램들을 audit으로 fix하라고 권장하는 듯. 그냥 설치해도 무방
10. 따라하는데 touch명령어를 못알아쳐먹는다. npm 설정이 잘못되어서 그런거같다라고는 하는데 nodejs가 환경변수에도 있는거 보면 왜 안되는지 이해가 안된다.
![1312](https://github.com/POONGNHA/Interview_Study/assets/105198445/818c57fc-d931-4aca-9170-5d68d99d64f3)
11. node js의 npm은 자동으로 repository 의 보악취약성을 검증해주고, 자격미달인 경우 업데이트를 요구한다. 그것이 npm audit fix인 것이고, audit fix가 먹지 않는 저 예제는 제작자가 보안업데이트를 
하지 않고있기 때문에 현재 에러가 발생하고 있는것으로 추정된다. 
12. 해결방법은 설치시 npm install --no-audit을 사용하거나, package.json을 확인해야 할듯하다. 
13. 도커에 내가 쓰는것도 아닌 image와 컨테이너가 잔뜩있음... 왜 그런지 모르겠다.
