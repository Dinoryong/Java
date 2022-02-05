# ㅜ Introduction to Java

----

> [toc]



## 개요

> 사전 setting

### 자바소스와 컴파일

- `javac` , `java` 명령어
- `exe` 파일이 아닌 `class` 파일 생성
- `main` 메소드

### Simple multiplication

- 클래스 생성 -> main 메소드 -> 변수 -> 메소드 -> 객체 -> 

---------

## 1. 메인 메서드 main 

- `main()` 만약 다르게 작성하면 기본 메서드를 찾을 수 없다라고 에러 발생 , 기본 메서드 (main) 작성하라고 함

- 자바 프로그램이 실행되면 제일 먼저 메인 메서드를 찾아서 실행

- 길게 작성된 소스에서 그 프로그램의 시작이 어딘지 알 수 없으면 안되므로 시작점을 알려주는 용도 , entry point , `main ()`

  

## 2. 파라미터스 Parameters

- 메서드(함수) 호출시 하나 or 둘 이상의 파라미터 값을 넣어서 호출할 수 있음
-  그러한 인수(파라미터) 들의 값을 저장할 변수 (바구니) 들을 명시
- `String` : 문자열 , `[]`: 배열 , `args` : 인수, 독립 변수
- `args`는 하나의 변수명일 뿐이므로 임의의 이름을 지정해도 무방



```java
접근제한자 클래스선언 클래스이름 {
  접근제어자 static 반환타입 메인메서드(문자열 배열 변수명) {
    // 구현할 코드 작성
  }
}
```



## 3. 반환할타입

- return type -> 반환할 값이 있냐? 없냐? -> 없으면 void(빈 공간,공허함,empty)
-  이 메서드(함수)는 호출하면 결과로써 특별히 반환되는 값은 없이 수행되는 메서드



----------

# static

> static 키워드 역할

## 1. `static` 으로 선언된 함수(메서드)나 변수는 자바 버추얼 머신에서 인스턴스 객체의 생성 없이 호출을 할 수 있다

- aka 객체 생성없이 해당 함수(메서드)를 호출해서 사용할 수 있다
- 자바 프로그램을 실행하면 `static`으로 지정된 메서드를 찾아서 먼저 메모리에 할당시킨다
- `static`으로 지정된 메서드가 여러개인 경우에는 객체를 생성하는 것과 상관없이 모두 메모리에 할당시킨다.
- 그런 후에, `"main"` 으로 이름이 만들어진 메서드가 있는지를 찾아서 그 메서드를 가장 먼저 시작점의 메서드로써 호출을 하게 되는 것이다.



--------------

#  변수

> 변수란, 변수 선언이란, 변수의 용도와 왜 필요한지

## 1. 변수란 무엇인가

- aka 바구니 -> 데이터를 저장하는 메모리 공간이다 -> 변하는 수



## 2. 변수 선언이란 무엇인가

- 변수를 사용하기 위해서는 먼저 변수의 타입에 맞는 선언을 해줘야 한다
- 정수형의 변수르 ㄹ사용하고자 한다면 -> 먼저 정수형 타입의 자료형을 선언해주고 사용해야 한다 -> 데이터타입(자료형) 에 대해서는 뒤에...



## 3. 변수의 용도

- 저장
- 어떤 연산을 수행할 때 값들을 저장해놓아야 하는데 그떄 변수(바구니)를 활용한다



## 4. 변수가 왜 필요한가 

- "

```java
publc class Java100_variable_001 {
  public static void main(String[] args) {
    
    int a;     // 정수가 저장될 변수 이름을 a로 만들어라
   	int b;
    int sum;
    
    a = 3;
    b = 4;
    
    sum = a + b;
    System.out.println(a);
    System.out.println(b);
    System.out.println(sum);    // 7
    
    sum = a + b + a;
    System.out.println(sum);   // 10
    
  }
}
```



-------

# 데이터 타입

> 타입 , 사이즈, 



## 1. 크게 봤을 때 : 기본형 타입, 참조형 타입







## 2. 기본형 타입(Primitive Daa Type) 8개

- 정수형 : byte (1 byte), short (2), int (4), long (8)



- 실수형 : float (4), double (8)



- 문자형 : char (2byte) -> 문자 1개 -> 참고로, 문자열을 다루는 타입은 없다



- 부울형(논리형 : 참 or 거짓) : boolean (1 byte) -> true, false



## 3. 참조형 타입 (Reference Data Type) - 위 기본형에 속하지 않는 데이터형들

- 클래스 (class) , 배열 (array), 인터페이스 (interface) , 문자열 (String/immutable) ...

- 참조형 변수의 특징 : 데이터가 저장된 메모리의 주소 값을 저장하는 변수이다
- Ex) 고래(데이터)가 무거우니까 고래 위치(주소) 를 저장해서 필요할 때 폰(참조형 변수)으로 그 위치를 참조해서 그 위치를 찾아가자. 고래 고기 먹고싶으면 내 핸폰을 열면 돼 . 그 위치 찾아가면 고래고기가 있엉



------------



# Primitive Data Type



## 1. Primitive Data Type 의 바이트 크기와 비트 크기를 출력

> 이 때 , 각 타입의 최댓값과 최솟값도 같이 출력

```java
public class Java100_variable_003 {
  public static void main(String[] args) {
    
    // byte, short, int, long, char
    // Byte, Short, Integer, Long, Character
    System.out.println(Byte.BYTES);    // 바이트 계산 1byte
    System.out.println(Byte.SIZE);     // 비트 계산 8 bit
    System.out.println("short:" + Short.BYTES + "(바이트)" + "-->" + Short.SIZE + "(비트)"₩t + Short.MAX_VALUE);
    
    
  }
}
```



- `char` 타입 : 범위의 최솟값 최댓값 출력은 오류가 난다. Why? `(int)Character.MIN_VALUE` 형태로 바꿔줘야한다



------

# 변수 선언 및 사용 시 주의사항

> 정수,실수,문자형 타입

## 예제

```java
public class Java100_variable_DataType1 {
  public static void main(String[] args) {
    
    // 1. 변수 선언
    int a; // 정수가 저장될 변수 이름ㅇ르 a 로 만들어라
    int b; int c = 90;
    double d;
    char e;
    
    // 2. 선언된 변수에 값을 대입
    a = 10;
    d = 10;  // 정수 10을 입력하면 10.0으로 출력
    e = "A"  // 쌍따옴표하면 에러
      
   // 3. 출력
    System.out.println(a);   // 10
    System.out.println(b);   // Err
    System.out.println(c);   // 90
    System.out.println(d);   // 10.0
    System.out.println(e);   // Err 
  }
}

// 4. 
String str1, str2, str3;
str1 = str2 = str3. = "Lemon";
System.out.println("[4-4] 여러 문자열 변수 한꺼번에 초기화" + str1 + str2 + str3);
```



-----------

 

# 기본형 타입

> 기본형 타입의 값을 초기화하는 방법
>
> 기본형 타입 8개 : 변수 선언과 동시에 값을 입력



```java
public class Java100_variable_DataType2 {
  public static void main(String[] args) {
    
    // [1] : 기본형 타입 --> 8개 --> 변수 선언과 동시에 값을 입력
    byte b = 100;
    short s = 30000;
    int i = 2100000000;
    long l = 7000000000;     // 700000000L; 소문자도 되긴 하지만 거의 대문자로 쓴다
    float f = 9.8;           // 9.8F;
    double d = 3.14;
    char c ='A';
    boolean bl = false;
    
    // [2] : 출력
    System.out.println(b + "최댓값-->" + Byte.MAX_VALUE);
    System.out.println(s + "최댓값-->" + Short.MAX_VALUE);
    System.out.println(i + "최댓값-->" + Integer.MAX_VALUE);
    System.out.println(l);
    System.out.println(f);
    System.out.println(d);
    System.out.println(c);
    System.out.println(bl);
  }
}
```



---------



# 정수형과 문자형 타입 변환

> 정수형 변수를 문자형으로 형Type 변환



```java
public clas Java100_variable_DataType3 {
  public static void main(String[] args) {
    
    // [1]
    short a = 'A';
    System.out.println(a);    // 65 (아스키코드 값을 출력)
    
    
  }
}




// [2]





// [3]
```























