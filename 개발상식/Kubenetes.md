## Kubenetes install

### 1. window named pipe를 사용한 설치

named pipe란? 


Named Pipe는 Pipe의 단점을 해결한, Pipe의 확장이라고 할 수 있음
이름을 가진 PIPE 를 통해서 프로세스들 간에 단방향 통신을 지원
서로 다른 프로레스들이 PIPE 의 이름만 알면 통신이 가능함


단점으로는 읽기/쓰기가 동시에 불가능하다.
해당 단점을 해결하기 위해 보통 pipe 하나를 읽기전용, 하나를 쓰기 전용으로 열어서 사용함

npipe를 사용하여 kudeadm을 설치하기위해 컴퓨터 ip주소를 확인하였다.
(ipconfig 주소 확인)[https://change-words.tistory.com/entry/%EC%9C%88%EB%8F%84%EC%9A%B0-IPCONFIG-%EC%A0%95%EB%B3%B4%EC%9D%98-%EC%9D%98%EB%AF%B8]
