### JVM
OS 관련없이 java 실행

### GC
JVM에 있는 기능. 불필요한 heap의 데이터 지워짐

### Collection
list, Map, set, Stack(LIFO) and Queue(FIFO)

### Annotation 
인터페이스 기반문법. @로 호출하여 사용. 클래스에 특별한 기능을 넣을 수 있다.

### Generic 
타입을 안정하고 return할수 있어서 input 데이터에 별도의 데이터형식가공을 안해도됨

### final 
변경불가

### Overriding vs Overloading
오버 로딩이 생성자임
생성자, 상속받기

### Access Modifier
public
protected :같은 패키지, 상속받은 외부 패키지
default : 해당 패키지 안에서만
private : 그 객체 내에서만

### Wrapper class
Integer, Float, Boolean 등등
기본 타입 int, float, bool등을 객체화해서 전달하고 싶을 때 사용

### Multi-Thread 환경에서의 개발
Field member : 필드에서 직접값을 입력(x) parmeter형태로 주고받아야 오류가 없다
동기화(Synchronized) : 스레드간 동기화를 하면 순차적으로 실행된다.
ThreadLocal : 스레드 간섭이 없어야하는 데이터에 사용