
## Transaction (23'07'31)
트랜젝션은 all or nothing이라는 말로 설명이 가능하다.

핵심내용은 DB 무결성을 위해 데이터 전송과정을 하나로 묶어서 처리하는게 Transaction이다.

중간에 끊겨도 데이터가 보존될 수 있도록 하는 것.

--------------------------------
## ACID (23'07'31)

Atomicity(원자성) all or nothing

Consistency(일관성) INTEGER 형식에 문자열 저장 안되는 것

Isolation(고립성) 비동기하면 동시데이터 변조가 일어날 수 있기때문에 그걸 막는것

Durability(영구성) 비휘발성 메모리에 DB를 보관해야함

-----------------
## NVL(args1, args2) (23'08'18)

args1이 null이라면 args1를 출력하고, not null일경우 args2을 출력한다.

---------------
## to_char() (23'08'18)
날짜를 숫자, 문자열로 바꿔주는 함수

TO_CHAR(SYSDATE, 'YYYY-MM-DD') 이런식으로 사용함
