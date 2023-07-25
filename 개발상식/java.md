## JAVA FileWrite 인코딩 에러 해결 (23'07'04)
한양대 도시생태계 과제중에 GEOJSON으로 파일을 저장할 경우 한글 인코딩이 깨지는 현상이 발생하여서

오랜시간 그 원인에 대하여 찾아보았다.

결론은 JAVA의 기본 ENCODE 형식이 UTF-16이기 때문에 생기는 에러였다.

프론트 HTML부터 시작해서, 백엔드(JAVA)시스템을 거쳐서 다시 프론트로 사용자에게 LAYER를 찍어줄 때까지 전부 UTF-8로 인코딩을 진행하였는데 오류가 나서 
내가 진행하지도 않았고, 주석한줄 없는 프로젝트의 모든 코드를 다시 확인하게 되어 쓸데없는 시간이 많이 낭비되었다.

결국 찾은 것이 바로 FILEWRITE할 때 JAVA의 기본 인코딩 형식때문에 UTF-8 형식에서 16으로 바뀌게 되어버린 것이었다.

JSON을 STRING으로 받아 FILEWRITE를 BUFFERED READER 객체 안에 넣고 UTF-8로 재변환 하여 파일을 저장하여서 해결하였다.


## SpringFramework Message (23'07'18)
회사에서 만들어 서비스하는 서울시청 웹 표준화 사업 back에서 통신을 spring의 message로 하기에 찾아보았다.
핵심은 payload를 내부에서 들고 전달할 수 있게해주는 Container같은 역할을 한다는 것을 기억하면 될 것이다.


## String + * (23'07'25)
java에 String에 null을 더하거나 ""을 더하면 String으로 붙어서 나온다.
쉽지만 까먹기 쉬운 것
