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


# 3] 부동 소수점

큰 수르 표현할 수 있고, 소수는 이진수로 표현하기 힘들다.

double d1 = 0.1, d2 = 0.2;

System.out.println(d1+d2); // 0.300000004가 나온다.


# 4] 문자열

기본 자료형이 아니라 참조형이다.(기본형이랑 절대 형 변환이 안된다)

char ch = 'A';

int num = 2;

System.out.println(ch+num); // 67

char ch2 = ch + num; // [x] char+int = int

char ch2 = ch + (char)num; // [x] char + char = int


# 5] boolean

자바에선 산술연산, 비교연산 불가능

논리연산만 가능

# 6] 문자열

기본 자료형이 아니라 참조형이다.

기본자료형이랑 참조형은 절대 형 변환이 안된다.

# operator02

# 1] 비트 연산자

두 항이 반드시 정수여야한다.

정수 << 비트수 : 왼쪽으로 비트 수만큼 이동하고 오른쪽에 남은 비트는 0으로 채운다.

정수 >> 비트수 : 오른쪽으로 비트 수만큼 이동하고 왼쪽에 남은 비트는 부호비트로 채운다.

&, && : 양쪽 항이 boolean이면 논리 연산자, 양쪽항이 정수면 비트연산자, 양쪽 항이 같으면 참

| : 양쪽 항중 하나만 참이면 참

^ : 두 항이 다르면 참

# method05

객체에서 행동을 의미

class안에 호출 해야한다.

method안에서 method를 만들 수 없다.

정의시 반드시 반환타입이 있어야 한다.

소문자로 시작하며 동사로 명명한다.

동일한 클래스안에서 메소드명은 중복 불가.

괄호열고 닫고 있으면 무조건 메소드다.

# abstraction06

# 1] 클래스

클래스명은 항상 대문자로 시작한다.

클래스명은 객체 설명도다

클래스는 여러 타입의 값을 저장 할 수 있는 자료형이다.(자료구조다.)

객체에서 속성과 행동을 뽑아내서 속성은 변수나 상수로, 행동을 메소드로 뽑아내 클래스를 정의하는것을 추상화라고 한다.

# 2] 속성(멤버 변수)

멤버변수는 해당 클래스와 has a 관계가 존재해야 한다.

멤버변수는 초기화를 하지 않으면 해당 자료형으로 초기화 된다.

멤버변수는 해당 클래스안의 모든 메소드에서 사용이 가능하다.

모든 데이터 타입을 사용할 수 있다.

멤버변수 선언

# accessmodifier07

클래스와 클래스 사이 or 각 클래스간의 멤버간 접근을 제어한다.

클래스, 멤버 변수, 멤버 메소드 앞에 붙어 있다.

private : 같은 클래스 내에서만

pacakage(생략형) : 같은 패키지 내에서만

protected : 상속 받으면 다른 패키지 가능

public : 다른 패키지 import하면 사용 가능

# globalnlocalvar08

# 1] 멤버 변수

클래스안에서 만든 변수

멤버변수는 해당 클래스안의 모든 메서드에서 사용 가능하다.

전역변수와 같다.

# 2] 지역 변수

메소드안에서 만든 변수

특정 지역 안에서 선언되어 그 지역에서만 사용되는 변수

메서드 안에서 선언된 변수 혹은 Block안에서 선언된 변수를 지역변수라 한다.

final이외 접근지정자를 붙일 수 없다.

(배열은 지역 변수든 멤버 변수든 모두 해당 자료형으로 초기화 된다.)

# modifier09

# 1] static (정적 변수)

메서드랑 멤버변수만 붙일 수 있다. (클래스, 지역변수 앞에 붙일 수 없다.)

static O -> class로드할 때

static x -> 인터프리터 할 때

static 안붙은 변수, 메소드는 클래스를 인스턴스화 해야 접근할 수 있다.

정적메소드 안에서 인스턴스 변수 사용할 수 없다.

# 2] static 블락

동일 클래스안 Main보다 먼저 실행됨 즉 main에 실행코드가 없어도 static 블락안에 있는 내용이 실행됨

다른 클래스에 main이 있는 경우 main이 순차적으로 실행되다 static블락이 있는 클래스를 인스턴스화 할 때 그때 생성자보다 먼저 static블락이 실행된다.

static 블락안에서는 정적 멤버만 사용 가능

wrapperclass10
많은 메소드 사용 가능하다.

자바의 모든 클래스들은 Object라는 최상위 클래스로부터 상속을 받는다.

Wrapper클래스들은 Obcject로부터 상속받은 toString() 메소드를 오버라이딩하여 인스턴스 변수 출력시 주소가 아니라 실제 값이 반환되도록 오버라이딩 되었다.

# 1] Integer Wrapper 클래스

    [1] 숫자형식의 문자열을 숫자로 변경

    static int parseInt(String s); (int 형식으로)

    static Integer ValueOf(String s); (Integer 형식으로)

    [2] 숫자를 문자열로 변경 static String toString(int i)

# 2] Character Wrapper 클래스

    [1] 문자열에서 index에 해당하는 위치의 한 문자의 아스키 코드 값을 반환한다.

    static int codePointAt(CharSequence sep, int index)

    [2] 어느 한 문자가 숫자인지 아닌지 판단하는 메소드

    static boolean isDigit(char ch)

    static boolean isDigit(int codePointAt)

    [3] 문자인지 아닌지 판단하는 메소드 static isLetter(char ch)

    [4] 공백인지 아닌지 판단하는 메소드 static boolean isWhitespace(char ch)

    static boolean isWhitespace(int codePointAt)

# stringclass11

# 1] Stirng Wrapper 클래스

(String 클래스에서 문자열 비교 equals() 메소드 사용

    [1] 문자열의 길이 반환

    int length()

    [2] 문자열에서 index에 해당하는 하나의 문자를 반환

    char charAt(int index)

    [3] 문자열에서 index에 해당하는 하나의 아스키 코드 반환

    char codePointAt(int index)

    [4] 두 문자열 비교

    int compareTo(String anotherString)

    (첫번째 아스키 코드값이 크면 +, 작으면 -, 같으면 0)

    [5] 두 문자열을 연결 할때

    String concat(String str)

    [6] 문자열에서 특정 문자열이 포함되었는지 판단하는 메소드

    boolean contains(CharSequence s)

    [7] char배열에 저장된 문자들을 String으로 변환

    static String valueOf(char data[], int offset, int count)

    [8] 문자열을 char형 배열로 변환

    char toCharArray()

    [9] 문자열이 특정 문자열로 끝나는지

    boolean endsWith(String suffix)

    [10] 문자열이 특정 문자열로 시작하는지

    boolean startsWith(String suffix)

    [11] 출력 형식을 지정하여 문자열로 반환할 때

    System.out.println(String Format("",args)

    [12] 문자열을 byte형 배열로 반환

    getBytes

    [13] 문자열에서 특정 문자열의 시작 인덱스를 반환

    int indexOf(String str)

    [14] 문자열에서 특정 문자열의 뒤에서 인덱스를 반환

    int lastindexOf(String str)

    [15] 문자열 변경

    String replace(char oldChar, char newChar)

    [16] 문자열로 특정 구분자로 분리해서 String형 변환

    String split(String regex)

    String tel="010-1234-5678";

    String strArr[]=tel.split("-");

    [17] 문자열 시작인덱스부터 끝까지 추출하는 메소드

    String substring(int beginindex)

    [18] 시작인덱스부터 끝 인덱스-1까지 문자열 추출

    String substring(int beginindex, int endinex)

    [19] 양쪽 끝에 있는 공백 제거

    String trim()

    [20] 바이트형 배열을 문자열로 반환

    byte bArr[] = {65,66,67,69,48} String byteToString = new String(bArr);

    [21] 캐릭터형 배열을 문자열로 반환

    char chArr[] = {'H','I','!','안','녕'}; String charToString = new String(chArr);

# 2] StringBuffer 클래스

메모리 낭비를 막기 위해서 StringBuffer클래스가 사용된다.

초기화 안된다.

StringBuffer buf = "Hello" [x]

StringBuffer buf = new StringBuffer

참조형끼리 형 변환, 대입연산 불가 (상속일 때만 가능)

    [1] 문자열 연결

    StringBuffer append("문자열")

    [2] 저장된 문자열만큼 버퍼크기를 줄인다.

    trimToSize()

    [3] start인덱스부터 end-1인덱스 까지 삭제

    StringBuffer delete(int start, int end)

    [4] index위치의 문자 하나 삭제

    StringBuffer deleteCharAt(int index)

    [5] index위치 특정 문자열 삽입

    StringBuffer insert(int index, String str)

    [6] start인덱스부터 end-1인덱스까지의 문자열을 str로 바꾼다.

    StringBuffer replace(int start, int end, string str)

    [7] 문자열을 반대로 출력

    String reverse()

# ectclass12

# 1] DataClass

Date클래스의 toString()메소드도 메모리의 주소를 문자열로 반환하는 것이 아니라 지정된 날짜 데이터를 문자열로 반환되도록 오버라이딩 되어있다.

getDate() : 0 일요일 ~ 토요일

[1] 두 날짜 사이의 선후관계를 판단하는 메소드

boolean after()/before()

[2] 두 날짜가 같은지 비교

equlas()

[3] 두 날짜가 같다면 0 반환 다르다면 1, -1반환

int compareTo(date anoterDate)

# 2] Calendar class

생성자로 calendar 객체를 인스턴스화 할 수 없다. (접근지정자가 protected이기 때문)

Calendar cal = Calendar.getInstance(); 로 접근

Calendar.Day_Of_WEEK : 1 일요일 ~ 7 토요일

Calendar.MONTH : 0이 1월

# 3] SimpleDateFormat class

[1] Date타입을 String형으로 반환해주는 메소드

String format(Date d);

[2] 패턴을 바꿔주는 메소드

applyPattern

[3] 날짜형식의 문자열을 Date타입으로 반환해주는 메소드

Date parse

# encapsulation13

관련있는 데이터를 하나로 묶는 것

멤버변수를 외부에서 접근 못하도록 막는 것

지역변수와 멤버변수가 같은곳에 쓰이면 지역변수가 우선한다.

이걸 해결하기위해 this키워드를 사용한다.

this는 인스턴스형 멤버로 접근할 때 사용 (정적 메소드는 사용 불가!)

private 멤버변수를 접근하는 방법

setter(쓰기)

public void setBalance(int money){

balance = money

}

매개변수를 할당받아 값을 지정해줌

getter(읽기)

public int getBalance(){

return balance;

}

리턴값으로 값을 받아옴

# polymorphism14

# 1] Overloading

매개변수 타입이 다르면 다른 메소드다

매개변수 개수가 다르면 다른 메소드다

매개변수 개수 같지만 순서가 다르면 다른 메소드다

(반환타입과는 전 관계가 없다.)

# 2] VarArgs

매개변수 개수에 따라 따로 만들지 않고 하나로 만듬

static int getTotal(int ...param){ 보통 for문 }

# 3] OverridingApp

메소드를 재정의

메소드명이 동일해야한다.

메소드의 반환타입 매개변수 개수, 데이터 타입 및 순서가 모두 같아야한다.

접근지정자는 부모와 같거나 부모 보다 더 넓어야한다.

@Override 작성하면 아래 메소드가 오버라이딩 됐는지 알려준다.

인스턴스 변수가 부모타입이든 자식타입이든 무조건 오버라이딩한 메소드가 호출된다. 단, 오버라이딩 하지 않았다면 당연히 상속받은 부모의 메소드가 호출된다.

만약 오버라이딩한 메소드 호출 시 부모의 메소드를 사용하고자 한다면 super키워드로 접근해서 재정의 하면 된다

부모타입의 인스턴스 변수로 자식에서 새롭게 확장한 멤버에 접근하려면 형변환 해야한다.

# 4] Instanceof 연산자

두 클래스간의 형 변환이 가능한지 판단하는 연산자

해당 인스턴스 변수가 어떤 타입의 변수인지 판단하는 연산자

두 클래스간의 상속관계가 있어야 한다.

해당 인스턴스 변수가 해당 타입이면 true

형 변환 하기전에 반드시 instanceOf로 판단 후 형 변환

child instanceof Person (true) (강제적 형 변환을 할 수 있다. why? 작은 그릇에서 큰 그릇으로 가려면,,)

person instanceof Child (false)

Person a = new Person(); -> Child b = (Child) a; 강제적 형 변환 해야한다.

# 5] Object class

자바의 모든 클래스의 최상위 부모는 Object클래스이다.

Object클래스의 toString()메소드는 객체의 주소를 String으로 반환해주는 메소드다.

Object클래스의 equals()메소드는 두 객체간의 인스턴스 비교 즉 주소값 비교

6]Heterogenious
두 클래스 사이에 상속관계가 존재해야한다.

Person person = new Child();

자식에서 새롭게 정의한 멤버는 접근 불가

오버라이딩한 메소드가 먼저 호출 된다.

자식 -> 부모 접근하려면 상속

부모 -> 자시 접근하려면 이질화 후 형 변환!!!!

# constructor15

객체가 생성될 때 최초로 실행되는 메소드

생성자 이름은 클래스명과 동일해야 한다

반환타입을 가져선 안된다.

접근지정자는 주로 public 속성

멤버 변수를 초기화 한다

생성자를 구현하지 않았을 경우 컴파일러는 default생성자를 제공해준다.

인자를 받는 생성자를 만들면 기본 생성자는 제공하지 않는다.

생성자를 다양하게 오버로딩 함으로써 다양한 초기값을 부여할 수 있다.

# 1] this()

생성자 안에서 호출 (다른 메소드 안에서는 절대 불가!)

첫번째 명령어에서 써야한다. 객체 만들어질때 가장 먼저 일어나는게 생성자를 호출하기 때문

멤버 변수보다 인자가 적은 생성자 안에서

# 2] SingleToneDesing

클래스를 설계하는 디자인 패턴의 하나로 하나의 인스턴스 즉 하나의 메모리를 생성해 이를 공유하고자 할 때 사용하는 패턴

생성자의 접근 지정자를 private로 한다.

정적 메소드로 해당 클래스의 객체를 반환하도록 정의한다.

# inheritance16

코드의 재사용

추상화한 클래스에 새로운 메소드나 변수를 추가하여 새로운 클래스로 만드는 것

상속 받을 때는 extensds란 키워드 사용

자식 is a 부모

단일 상속 개념

private 접근 지정자가 붙은 부모의 멤버는 상속은 받으나 접근 불가

자식의 기본생성자 생성하면 부모의 기본생성자도 자동으로 호출된다.

# 1] super

부모 클래스를 지칭한다.

부모 클래스의 멤버에 접근할 때 사용

자식클래스와 부모클래스의 멤버명이 동일할 때 구분해주기 위한 키워드

정적 메소드안에서 사용불가(this와 같다)

# 2] super()

자식의 생성자 안에서만 호출 가능

자동으로 호출되며 this()와 같이 사용 X

인자 생성자를 만드려면 super() 호출해야한다.

# abstract17

한 개 이상의 추상 메소드를 가진다면 추상 클래스로 선언 해야한다.

추상 메소드를 갖고 있지 않더라도 인스턴스 상속을 못하게 할 목적이면 추상 클래스로 선언 할 수도 있다.

추상 메소드를 가지지 않는 클래스를 상속받은 경우 오버라이딩 강제적으로 할 필요 없다.

추상 메소드를 가진 클래스를 상속받은 경우 반드시 오버라이딩 하거나, 추상 클래스가 되어야 한다.

추상 메소드란 메소드 구현부 없는 선언만 하는 것이다.

객체를 생성할 수 없고, 인스턴스 화 할 수 없다.

접근하려면 Heterogenious해야한다.

# interface18

클래스가 객체의 설계도라면 인터페이스는 클래스의 설계도라 할 수 있다.

멤버로는 추상메소드와 상수(final 변수)로만 구성된다. (생성자가 없고 new를 할 수 없다. )

접근지정자는 public과 default 지정만 가능하다. (static, final불가)

상속이 목적이며, 상속받은 클래스는 추상 메서드를 오버라이딩 해야 하기 때문에 동일한 API(메소드)를 사용할 수 있다.

자바는 단일 상속이 원칙이나 인터페이스를 이용해서 다중 상속을 구현할 수 있다.

변수가 있다면 무조건 상수, 메서드가 있다면 무조건 추상메서드다

인터페이스 하나 당 자바파일 하나가 원칙(클래스와 동일)

클래스 <-> 클래스 extends

인터페이스 <-> 인터페이스 extends

인터페이스 -> 클래스 implements

# collection20

인스턴스화 객체를 저장하는 자료구조

메모리 기반의 작은 데이터 베이스 역할을 한다.

# 1] Set계열

데이터 저장시 중복을 허용하지 않고 순서없이 입력된다.

    [1-1] 객체 생성

    HashSet<?> set = new HashSet();

    [1-2] 객체 저장

    set.add(객체)

    [1-3] 객체 수 얻기

    set.size()

    (중복으로 저장하면 컴파일 에러는 안나지만 저장되지 않는다.)

    [1-4] 객체 꺼내오기

    for(자료형 객체를담을변수 : 배열명이나 혹은 컬렉션명{})

    [1-5] 객체 검색

    boolean contains(Object e)

    [1-6] 객체 삭제

    boolean remove(Object e)

    [1-7] 전체 삭제

    set.clear();

# 2] List계열

데이터 중복을 허용하고 순서있게 저장한다.

    [2-1] 객체 생성

    List list = new ArrayList();

    [2-2] 객체 저장

    list.add("객체")

    중복 저장 허용

    list.add(인덱스 번호, "객체")

    맨 뒤에 저장하려면 list.add(list.size(),"객체")

    [2-3] 객체 출력

    for(자료형 객체를담을변수 : 배열명이나 혹은 컬렉션명{}) System.out.println(객체를담은변수)

    [2-4] 객체 대체

    list.set(int index,"객체")

    [2-5] 객체 삭제

    list.remove("객체" or int index)

    [2-6] 전체 삭제

# 3] Map계열

키와 값의 쌍으로 저장한다.

검색이 빠르다.

    [3-1] 객체 생성

    Map<String, String> map = new HashMap<String, String>();

    Map map = new HashMap();

    [3-2] 객체 저장

    map.put("key","value");

    [3-3] 저장된 객체 수

    map.size();

    [3-4-1] 키 값을 알 때

    map.get("key");

    [3-4-2] 키 값을 모를 때

    Set<?> Keyset() 호출

    Set keys = map.keySet();

    for(Object key:keyss){

    Object value = map.get(key);

    System.out.println(String.format("%s : "%s",key,value));

    }

    [3-4-3] Value만 얻어 올 때 : values()

    Collection values = map.values();

    for(Object value:values)

    System.out.println(value);

    [3-5] 검색

    map.containKey("key" or "value");

    [3-6] 삭제

    map.remove("key")

    [3-7] 전체 삭제

    map.clear();

# 4] 배열 컬렉션 정렬하기

    [4-1] 배열 정렬하기

    Arrays.sort(배열)

    [4-2] 배열을 하나의 문자열로 변경

    Arrays.toString(배열)

    [4-3] 배열의 요소를 찾는 메소드

    Arrays.binarySearch(배열,배열값)

    -> 반환값은 배열의 인덱스

    [4-4] 배열을 List컬렉션으로 변경

    Arrays.asList();

# exception21

# 1] ExceptionBasicApp

대표적인 에러

ArrayIndexOutOfBoundsException : 배열 크기보다 더 크게 메모리를 사용했을 때

NumberFormatException : 숫자형식의 문자열을 int형으로 변환 시 해당 문자열이 숫자형식이 아닐 때,

NullPointerException : 인스턴스 변수에 해당 객체의 메모리 주소가 저장이 안된 경우

ArithmeticException : 0으로 나눌 때 발생

예외 메시지 출력 방법

사용자 임의 예외 메시지
System.out.println("0으로 나눌 수 없어요")

예외 클래스의 인스턴스 변수 이용 ("예외클래스 : 예외메시지" 형태를 문자열로 반환)
System.out.println(e.toString());

예외메시지만 출력
System.out.println(e.getMessage());

에러원인과 위치 확인 ? (개발시 주로 사용)
e.printStackTrace();

     try {

        오류 문장

       }

      catch(에러(모른다 싶으면 Exception) e) {

           System.out.println("예외가 발생했어요");

       }
       
# 2] ExceptionCatchApp

catch절을 여러개 사용할 수 있다.

여러개 사용시 자식 예외클래스부터 catch해야한다.

ex)

    catch(NumberFormatException e) {

      System.out.println("arr[0]방에는 숫자만 입력하세요");

     }

     catch(InputMismatchException e) {

      System.out.println("arr[1]방에는 숫자만 입력하세요");

     }

     catch(ArithmeticException e) {

      System.out.println("0으로 나눌 수 없어요");

     }
     
혹은

    catch(Exception e){

    System.out.println("에러가 발생했어요");

    }
    
# 3]ExceptionFinallyApp

finally절 : 예외가 발생하든 안하든 실행하고자 하는 명령문들을 기술

finally절 안에 있는 명령문은 return문을 만나더라도 실행 됨

단, System.exit(0)을 만나면 당연히 실행 안됨.

try ~ catch절 : ~예외 직접 처리

try ~ catch ~ finally절 : ~예외 직접 처리 후 반드시 실행 할 문장도 처리

try finally절 : ~예외는 던지고 (throws) 에외가 발생하든 안하든 반드시 실행할 문장 처리

# innerclass22

# 1] 내부 클래스

클래스안의 클래스로 static이 안붙음

정적 멤버는 가질 수 없다.

외부클래스의 멤버를 모두 사용 할 수 있다.

외부클래스에서 내부 클래스를 사용하려면 인스턴스화 해야한다.

외부클래스의 정적 메소드에서는 내부의 모든 멤버 사용 불가. (단, 상수는 클래스명으로 접근 가능)

다른 클래스(별개 클래스에서) 내부 클래스가 안보인다 사용하려면 외부클래스 인스턴스 후 사용 가능(당연히 내부클래스도 외부클래스에서 인스턴스 되어있어야함)

outer.inner.innerInstanceVar;

# 2] 내부 정적 클래스

클래스안의 클래스로 static을 붙일 수 있다.

정적 멤버 가질 수 있다.

외부클래스의 인스턴스형 멤버는 사용할 수 없다.

클래스 앞에는 static을 붙일 수 없으나 내부 클래스는 가능하다.

외부클래스에서 내부의 정적 멤버는 인스턴스화 필요없이 클래스명으로 접근 가능하다.

외부클래스 인스턴스 메소드에선 내부클래스 멤버 접근 불가능하다.

다른 클래스에서 내부클래스를 접근하려면 외부 클래스명. 내부클래스 인스턴스변수.정적멤버 혹은 외부 클래스명.내부클래스명 인스턴스 변수 = new 외부클래스명.내부클래스명() 으로 접근할수 있다. (내부클래스 인스턴스할때 static 붙여줘야함)

# 3] 익명클래스

이름이 없는 클래스

자식에서 새롭게 정의한 멤버 접근 불가 부모 클래스의 메서드를 오버라이딩 하는 것이 주된 용도

클래스명이 없음으로 다운캐스팅 불가

# thread23

# 1] 쓰레드 상속 X

메소드 안에서 Thread.Sleep()으로 구현 후 main에서 인스턴스 후 호출

# 2] 쓰레드 상속 O

오버라이딩 run메서드에서 실행문 작성 후 main에서 인스턴스 후 변수.start() 메서드 호출

# 3] Runable을 Implement 받은 경우

main 메서드에서 자식클래스 인스턴스 후 Thread 메모리를 인스턴스 후 인자 생성자에 자식 인스턴스 변수 대입

Solidier solidier = new Solidier();

Thread th = new Thread(solidier);

# 4] Thread 메서드

.start() : 쓰레드 시작하는 메서드

.setName() : 쓰레드 이름 지정하는 메서드

.getName() : 쓰레드 이름 받아오는 메서드

.join() : 호출 한 스레드가 다 실행이 끝나야 다른 스레드가 동작한다.

.setPriority : 우선권 할당 1~10 디폴트값은 5다.

.setDaemon : 종속 스레드

# 4-1] Thread 인스턴스 변수

Thread.sleep() : 상속받지 않은 클래스에서 Thread 생성

Thread.currenThread() : 자기 자신 지정?

Thread.activeCount() : 현재 활성화 상태 (Runnable 혹은 Running상태)에 있는 스레드 수

io24.node
image

# 1] 입력 : 키보드, 출력 : 모니터

데이터 소스 : 키보드

바이트 노드 스트림 : System.in

데이터 목적지 :모니터

바이트 노드 스트림: System.out

    InputStream is = System.in;
    PrintStream ps = System.out;
    int data;
    while((data=is.read()) != -1){
     ps.write(data);
     ps.flush():
    }

# 2] 입력 : 키보드, 출력 : 파일

데이터 소스 : 키보드 바이트 노드 스트림 : System.in

데이터 목적지 : 파일 바이트 노드 스트림 : FileOutputStram

     InputStream is = System.in;
    FileOutputStream fos = new FileOutputStream("저장할 위치");
    int data;
    while(data=is.read()) != -1){
     fos.write(data);
     fos.flush();
    }
    fos.close;

# 3] 입력 : 파일 , 출력 : 모니터

데이터 소스 : 파일 바이트 노드 스트림 : FileInputStream

데이터 목적지 : 모니터 바이트 노드 스트림 : System.out

     FileInputStream fis = new FileInputStream("저장된 위치");
    OutputStream out = System.out;
    int data;
    while((data=fis.read()) != -1){
    out.write(data);
    out.flush();
    }
    fis.close();
    
# 4] 입력 : 파일, 출력 : 파일

데이터 소스 : 파일 바이트 노드 스트림 : FileInputStream

데이터 목적지 : 파일 바이트 노드 스트림 : FileOutputStream

 <필터 효과 적용 전>

     FileInputStream fis = new FileInputStream("저장된 위치");
    FileOutputStream fos = new FileOutputStream("저장할 위치");
    int data;
    while((data=fis.read()) != -1){
    fos.write(data);
    fos.flush();
    }
    fos.close();
    fis.close();
    
<필터 효과 적용 후>

    FileInputStream fis = new FileInputStream("저장된 위치");
    FileOutputStream fos = new FileOutputStream("저장할 위치");
    byte[] b = new byte[1024];
    while((data=fis.read(b)) != -1){
    fos.write(b,0,data);
    fos.flush();
    }
    fos.close();
    fis.close();
    
# 5] 입력 : 키보드 , 출력 : 파일 (문자 단위)

데이터 소스 : 키보드 노드 스트림 : InputStreamReader

데이터 목적지 : 파일 노드 스트림 : FileWriter

<필터 효과 적용 전>

    InputStreamReader isr = InputStreamReader(System.in);
    FileWriter fw = new FileWriter("저장할 위치");
    int data;
    while((data=isr.read()) != -1){
    fw.writer(data);
    fw.flush();
    }
    fw.close();
<필터 효과 적용 후>

    InputStreamReader isr = InputStreamReader(System.in);
    FileWriter fw = new FileWriter("저장할 위치");
    int data;
    char[] c = new char[10];
    while((data=c.read(c)) != -1){
    fw.writer(c,0,data);
    fw.flush();
    }
    fw.close();
    
# 6] 입력 : 파일 , 출력 : 모니터 (문자 단위)

데이터 소스 : 파일 노드 스트림 : fileReader

데이터 목적지 : 모니터 노드 스트림 : OutputStreamWriter

    fileReader fr = new fileReader("저장된 위치");
    OutputStreamWriter osw = new OutputStreamWriter(System.out);
    int data;
    while((data=fr.read()) != -1){
    osw.writer(data);
    osw.flush();
    }
    osw.close();
    fr.close();
    io24.filter
    
# 1] 입력 : 키보드, 출력 : 모니터
데이터 소스 : 키보드 노드 스트림 : System.in

데이터 목적지 : 모니터 노드 스트림 : System.out

    BufferedInputStream bis = BufferedInputStream(System.in);
    BufferedOutputStream bos = BufferedOutputStream(System.out);
    int data;
    while((data=bis.read()) != -1){
    bos.write(data)
    bos.flush();
    }
    
# 2] 입력 : 키보드, 출력 : 파일

데이터 소스 : 키보드 노드 스트림 : System.in

데이터 목적지 : 파일 노드 스트림 : FileOutputStream

    BufferedInputStream bis = new BufferedInputStream(System.in);
    BufferedOutputStream bos = new BufferedOutputStream (new FileOutputStream("저장할 위치");
    int data;
    while((data=bis.read()) != -1){
    bos.write(data)
    bos.flush();
    }
    bos.close;

# 3] 입력 : 파일, 출력 모니터

데이터 소스 : 파일 노드스트림 : FileInputStream

데이터 목적지 : 모니터 노드스트림 : System.out

    BufferedInputStream bis = new BufferedInputStream
       (new FileInputStream("src/io24/filter/KeyboardBuffered.txt"));
    BufferedOutputStream bos = new BufferedOutputStream(System.out);
    int data;
    while((data=bis.read())!=-1) {
     bos.write(data);
     bos.flush();
     }
    bis.close();

# 4] 입력 : 키보드, 출력 : 모니터

데이터 소스 : 키보드 (문자단위로 받음) 노드 스트림 : System.in

데이터 목적지 : 모니터 노드 스트림 : System.out

[printWriter 사용 전]

    BufferedReader br = 
     new BufferedReader(
      new InputStreamReader(System.in));

    BufferedWriter bw = 
     new BufferedWriter(
      new OutputStreamWriter(System.out));
    String data;
    while((data=br.readLine()) != null) {
     bw.write(data+"\n");
     bw.flush();

     //줄바꿈 기을 하는 메소드 호출 : newLine()
     bw.write(data);
     bw.newLine(); //줄바꿈
     bw.flush();
    }
[printWriter 사용 후]

    BufferedReader br = 
     new BufferedReader(
      new InputStreamReader(System.in));

    PrintWriter pw = new PrintWriter(System.out,true);
    String data;
    while((data=br.readLine())!=null) {
     pw.println(data);
    }
    
# 5] 입력 : 파일, 출력 : 모니터

    BufferedReader br =
     new BufferedReader(new FileReader("src/io24/filter/BufferRWKeyboardToMonitor.java"));
    PrintWriter pw = new PrintWriter(System.out,true);
    String data;
    int line=1;
    while((data=br.readLine())!=null) {
     //문]라인번호 붙여서 출력하고 "java"를 한글 "자바"로 바꿔서 출력해라.
     pw.println(String.format("%-5s%s",line++,data.replace("java","자바")));
    }
    pw.close();
    
# 6] 입력 : 파일 (1 바이트), 출력 : 파일 (1 바이트)

//1]필터 끼운 입력 스트림 생성

    BufferedInputStream bis = 
     new BufferedInputStream(
      new FileInputStream("src/io24/node/FileReaderToMonitor.java"));
    BufferedOutputStream bos = 
     new BufferedOutputStream(
      new FileOutputStream("src/io24/filter/FileReaderToMonitor.txt"));
    int data;
    while((data=bis.read())!=-1) {
     bos.write(data);
     bos.flush();
    }
    bis.close();
    bos.close();
    
# 7] 입력 : 메모리 , 출력 : 파일

    byte b = 100; 
    byte[] bArray= {97,98,99,100};
    char ch = '가';
    int num = 256;
    boolean bool = false;
    String object = "안녕 자바! HELLO JAVA! 123456789";

    DataOutputStream dos =
      new DataOutputStream(
       new FileOutputStream("저장할 위치"));

    dos.writeByte(b);
    dos.write(bArray);
    dos.writeChar(ch);
    dos.writeInt(num);
    dos.writeBoolean(bool);
    dos.writeUTF(object);
    //무조건 순서대로 넣어야한다.
    dos.close();
    
# 8] 입력 : 파일 , 출력 : 모니터

    DataInputStream dis = 
     new DataInputStream(
      new FileInputStream("저장된 위치"));

    byte b = dis.readByte();
    System.out.println(b);
    byte[] barr = new byte[4];
    dis.read(barr);
    for(byte value:barr) {
     System.out.println(value);
    }
    char ch = dis.readChar();
    System.out.println(ch);
    int n = dis.readInt();
    System.out.println(n);
    boolean bool = dis.readBoolean();
    System.out.println(bool);
    String str = dis.readUTF();
    System.out.println(str);
    //무조건 순서대로 넣어야한다.
    dis.close();
    
# 9] 입력 : 메모리 , 출력 : 파일

    Person pe1 = new Person("가길동",20,"천호동");
    Person pe2 = new Person("나길동",30,"잠실동");
    Person pe3 = new Person("다길동",40,"석촌동");
    ObjectOutputStream oos = new ObjectOutputStream(
      new FileOutputStream("저장할 위치"));
    oos.writeObject(pe1);
    oos.writeObject(pe2);
    oos.writeObject(pe3);
    10] 입력 : 파일, 출력 : 메모리

    ObjectInputStream ois = 
     new ObjectInputStream(
      new FileInputStream("저장된 위치"));

    Object obj = ois.readObject();
    if(obj instanceof Person) {
     Person person1 = (Person)obj;
     System.out.println(person1);
    }
    Person pe2 = (Person)ois.readObject();
    System.out.println(pe2);
    Person pe3 = (Person)ois.readObject();
    System.out.println(pe3);

    ois.close();

# JDBC

JAVA언어로 데이터베이스에 연결에서 입력, 수정, 삭제 및 조회(CRUD)등의 작업을 할 수 있도록 해주는 기술

JDBC는 프로그램과 각각의 데이터베이스 중간에서 각 데이터베이스의 벤더에서 제공하는 API들을 사용할 수 있도록 변환해주는 기능을 수행한다.

자바와 오라클 연결하는 방법

    Connection conn = null;
    Statement stmt = null;
    ResultSet rs =null;
    int affected = 0;

    1]오라클용 JDBC드라이버 메모리에 로딩
    Class.forName("oracle.jdbc.OracleDriver");

    2]DriverManger클래스의 getConnection()메소드로 오라클에 연결시도
    conn = DriverManager.getConnection(String url="jdbc:oracle:thin:@localhost:1521:xe","oracle 계정","oracle 비밀번호")
    //conn은 주소를 담는 변수다

    3]쿼리문(SQL)전송을 위한 Statement계열의 객체 생성
    stmt = conn.createStatement();

    4]쿼리 실행
    String sql="SELECT * FROM emp ORDER BY hiredate DESC";

    5]Statement계열 클래스(stmt)의 execute계열 메소드를 
    rs=stmt.executeQuery(sql);
    int affected = stm.executeUpdate(sql);

    * 쿼리문이 DELETE/UPDATE/INSERT일때는 int executeUpdate()
    * 쿼리문이 SELECT일때는 ResultSet executeQuery()호출

# prepareCall

# 2] 프로시져

    // INSERT
    csmt = conn.prepareCall("{call SP_INS_MEMBER(?,?,?,?)}");
    /*
     * 2] 파라미터 설정
     * 2-1] 인파라미터 설정 
     */
    csmt.setString(1, getValue("아이디"));
    csmt.setString(2, getValue("비밀번호"));
    csmt.setString(3, getValue("이름"));

    //2-2] 아웃파라미터 설정
    csmt.registerOutParameter(4,Types.NVARCHAR);

    //3] 프로시저 실행
    System.out.println(csmt.execute());

    //4] 아웃파라미터에 저장된 값 읽어 오기
    System.out.println("프로시저의 아웃 파라미터 값:"+csmt.getString(4));
    //5] 자원 반납
    close();

    // UPDATE
    Connect(ORACLE_URL, "JDBC", "JDBC");
    csmt = conn.prepareCall("{call SP_UP_MEMBER(?,?,?,?)}");
    csmt.setString(1, getValue("수정할 아이디"));
    csmt.setString(2, getValue("비밀번호"));
    csmt.setString(3, getValue("이름"));
    csmt.registerOutParameter(4, Types.CHAR);
    csmt.execute();
    System.out.println(csmt.getString(4).trim());
    close();
