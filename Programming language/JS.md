## JS의 구조
stack, heap, Event(Task) Queue
JS는 하나의 Call stack을 사용한다.
즉 싱글스레드의 하나의 call stack만 사용한다는 것

heap에 인스턴스,

que에 이벤트 가 저장되고 call stack에 자리가 비었을때 실행된다

-----------------------------------------------------------------------------------

## 프로토타입
JS는 프로토타입 기반 언어

Prototype = Prototype Link + Prototype Object

객체는 함수로 생성되는데, 이 함수 정의 시 Prototype Object로 만들 수 있는것

링크는 오브젝트가 연결되는것

-----------------------------------------------------------------------------------

## 클로저 Closure

함수 내부에서 또다른 함수를 call 했을 때, JS는 특이하게 함수가 종료가 안되고 거기 변수를 사용할 수 있다.

-----------------------------------------------------------------------------------

## this 
JS는 java와 다르게 호출하는 경우에 따라 this가 다르다

상황 1. 객체의 메서드를 호출할 때 

상황 2. 함수를 호출할 때

상황 3. 생성자 함수를 통해 객체를 생성할 때

상황 4. call, apply, bind 를 통한 호출

서로 다른 함수에서 this값을 필요로 할때 바꿔서 사용함

call(), apply() : this를 지정함

bind() : this값을 아예 바꿈

-----------------------------------------------------------------------------------

## Promise
JS는 비동기이기때문에 콜백 중첩을 막기위해 promise 사용

Async/Await와 다르게 Error Handling 기능이 있음.

-----------------------------------------------------------------------------------

## Async/Await
비동기 코드 작성의 하나의 방법

-----------------------------------------------------------------------------------

## Arrow function
함수 작성할때 사용

-----------------------------------------------------------------------------------


