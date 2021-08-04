# Java 

[자바의 특징]
1) 플랫폼 독립성 (자바로 만든 프로그램을 다양한 운영체제에서 실행 가능) 
2) 객체지향언어(OOP)
3) 멀티스레드 지원 (multitasking)
4) 자동 메모리 관리(GC)
5) 풍부한 라이브러리

[자바 가상 머신(JVM)]
자바 프로그램이 실행되는 가상 컴퓨터(VM)
한번 작성하면 어디서든 실행가능(Write once, run anywhere)
운영체제에서에서 실행되는것이 아니라 JVM으로 작동하기때문에 운영체제에 독립적이다

# Data Type
 # 1] 정수형 : int형이 디폴트 자료형

 byte + byte = int

byte + short = int

byte a= 10, b=20;

c = a+b;

byte = a+b [x] 오류난다. // a+b는 int형

# 2] 실수형  : double형이 디폴트 자료형

float f1 = 3.14 [x]

float f1 = 3.14f [o]

float f1 = 200 [o] // 정수형보다는 실수형이 더 큰 그릇

실수 4byte + 정수 8byte = 실수 4byte

※ 소수점이 없는 숫자는 int형, 소수점이 있는 숫자는 double형으로 간주
※ 수치형에서는 범위를 벗어난 값을 대입하면 에러 발생 (int형을 요구함)
예) long i = 10000000000; (에러) → long i = 10000000000L; (뒤에 L을 붙인다. 대소문자 무관)

.
