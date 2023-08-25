## How flutter work (23'07'11)
Flutter & Dart engine doesnt communicate with operating system directly. Flutter framework did it.

-------------
## state (23'08'17, 23'08'25)

state란 쓰이는 데이터 라고 할 수 있겠다.

app의 state는 app에서 사용되는 데이터를 의미하는 것이고, widget에서 사용되는 state는 widget의 data를 가지고있는 데이터가 widget state이다.

stateless는 데이터가 변경되지 않는 것.




플러터의 기본인 위젯, 그 위젯이 빌드될때 sync하게 읽히는것이 state이고, widget의 life cycle이 끝나기 전까지 변경될 수 있는것이 state이다. 

처음 실습할 때 stateless widget을 만들어서 실습하였는데, stateless는 state는 가지고 있지만 data가 변경될 수 없는 상황이라고 보는게 맞겠다.

stateful widget은 constructor() -> initstate() -> build() -> dispose() 형태로 나타난다. 자세히 설명하면 좀 다르지만 맥락은 이와 같은 형태이다.

-------------
## initstate (23'08'17)

stateful widget 처음 초기화 할때 사용하는 method

-------------
## dispose (23'08'17)

stateful widget의 life cycle이 끝날때 호출하여 끝내는 method인듯.
