## Kubenetes install

#### window named pipe를 사용한 설치방안은 폐기하였다. 대신 docker를 설치하고 그에따라 추가기능으로 사용하기로 함

named pipe란? 

Named Pipe는 Pipe의 단점을 해결한, Pipe의 확장이라고 할 수 있음
이름을 가진 PIPE 를 통해서 프로세스들 간에 단방향 통신을 지원
서로 다른 프로레스들이 PIPE 의 이름만 알면 통신이 가능함
단점으로는 읽기/쓰기가 동시에 불가능하다.
해당 단점을 해결하기 위해 보통 pipe 하나를 읽기전용, 하나를 쓰기 전용으로 열어서 사용함


### 도커 설치 관련 페이지들
(도커 설치 사이트)[https://www.docker.com/]


(도커 참조 사이트)[https://www.oss.kr/info_techtip/show/2e408efc-900d-4a09-82e9-06613db8f591]

cmd에서 wsl 명령어 사용하여 업데이트함. docker 설치 완료후 회원가입완료

wsl : 윈도우용 리눅스 하위시스템
