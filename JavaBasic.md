# Java Fundamental
## day1

<strong>system 개발</strong>

1. 모델링 => system 구축 시 구현 전 결정하는 모든 활동
2. 구축할 system 정의
3. 요구사항 정의
4. 계획(분석,설계)
5. 결과물 => 모델
6. 표기법(Notation) : UML (Unified Modeling Language) // UML Notation 으로 모델 생성

<strong>구현</strong>
1. 시스템 실제 구현
2. 소스코드, 컴파일, 디버깅
3. 결과물 => 코드를 포함한 system
4. 프로그래밍 언어: Java

<strong>system 개발 절차</strong>
1. 요구사항 정의
2. 분석
3. 설계
4. 구현

<strong>*Java 개발환경 구축 => JDK(java development kit)</strong>
<strong>Java 특징</strong>
* OOPL (Object Oriented Programming Language)
* 플랫폼 독립적 (JDK = JAVA 플랫폼 = J2SE 플랫폼 : JAVA 플랫폼은 O/S에 독립적이다. O/S와 ~.class중간에 JDK를 이용
* JDK = 개발 툴과 JRE(Java Runtime Environment)를 포함하고 있다. JAVA 컴파일러 보유 ( .java -> .class(자바 바이트 코드))
* JRE 안의 JVM의 자바 인터프리터가 실행
* JDK > JRE > JVM
 
//용어 정리
* 플랫폼 : O/S의 플랫폼 = H/W , APP의 플랫폼 = O/S, ~.hwp의 플랫폼 = HWP
* End User = 사용자
* url = Uniform Resource Locator : 리소스의 위치를 가리키는 문자열
          
 ## day2
 //용어정리
 * csv = 구분자 : command seperated value
 * snake case : csv = _ (언더바)
 * camel case : csv = 대문자
 * cmd = command = console
 * utf-8 : Unicode Transformation Format - 8bit
 * ANSI : American National Standards Institute : 8bit 문자표현 방식
 * console 명령어 : %~% : 변수로 해석합니다. :
 * IDE : Integrated Development Environment
<strong>환경변수설정</strong>
* 컴퓨터가 자바가 설치된 경로를 자동으로 찾지 못하기 때문에 path로 자바 응용프로그램(ex.jdk,jre)가 환경변수 설정 path 를 통해 설치된 폴더 위치를 가리켜야한다.

 JAVA_HOME = C:\Program Files\Java\jdk1.8.0_181
 
 path : %JAVA_HOME%\bin
 
 echo %path%
 
<strong>헷갈리는 내용정리</strong>
* casting
묵시적(implicit): 자동형변환 
명시적(explicit): 프로그래머가 형변환

```java
byte 1 = 100;
byte b2 = 20;

//byte b3 = b1+b2 (error) ->b1과 b2는 int로 연산 후 int 값을 byte 넣기 불가능 
byte b4 = (byte)(b1+b2); //명시적 형변환
byte b5 = (byte)(b1+b4); // 쓰레기값 출력 byte보다 큰값 대입

int i1 = b1+b2; // 묵시적 형변환
double test01 = 100 + 0.5; //=> data type 이 큰쪽으로 묵시적 형변환

//int test02 = 100 + 0.5; compile error double to int

int i3 = 201/2; // 100
double d1 = 201/2; // 100.0
double d2 = (double)201/2; // 100.5
double d3 = (double)(201/2); // 100.0


```

## day3
//용어 정리

suffix = ++a

prefix = a++

refactoring =  '결과의 변경 없이 코드의 구조를 재조정함' / 주로 가독성을 높이고 유지보수를 편하게 한다.

debugging = 시스템의 논리적인 오류나 비정상적 연산(버그)을 찾아내고 그 원인을 밝히고 수정하는 작업 과정을 뜻한다. 

initialization = (defalut : 숫자 = 0, boolean=false)

api =  Application Programming Interface

new 키워드

* 배열 생성방법
* <strong>int array 변수 a 에는 배열의 참조값이 저장됨</strong>
* int[] a = new int[3];
* a[0]=1; (default 값은 0) 
* int a[] = {1,2,3,4,5};
* int a[] = new int[]{1,2,3,4,5};

객체 3요소
* 상태 행위 식별성

## day4

<Strong>1. 객체지향의 기본 원리</Strong>
- 추상화(Abstraction)
- 캡슐화(Encapsulation)
- 모듈화(Modularity)
- 계층화(Hierarchy)

<Strong>2. 객체지향의 기본개념 </Strong>
- 객 체(Object)
- 클래스(Class)
- 다형성(Polymorphism)
- 관 계(RelationShips)

<em><strong>객 체(Object)</strong></em>

:물리적/ 개념적/ 소프트웨어적

객체 = 식별성 + 상태 + 행위

=> 식별성 : 같은 상태를 갖더라도 구분가능!

=> 상태 : 객체가 가질 수 있는 조건 (Field), 시간, 행위를 통한 변경

=> 행위 : 객체가 반응 할 수 있는 Message의 집합 (Method)

<em><strong>추상화(Abstraction)</strong></em>

=> 객체를 구분하는 핵심적인 특징으로 분류/집중

=> 문제영역(Domain)에 의존적이다. (ex/교육시스템 => 사람 <= 병원)

=> 추상화를 이용해 모델링 할 수 있다

<em><strong>클래스(Class)</strong></em>
:공통된 특성(속성), 행위, 관계, 의미를 갖는 객체의 모임

=> 객체의 공통점을 찾아서 class로 정의한다

=> 객체를 추상화해서 표현 / 정의한 것

=> 객체지향의 원리 -> 추상화


## day5
* bean : main 메소드가 없는 자바 class 파일
* app : main 메소드를 포함한 자바 class 파일
* getter
* setter
* classpath : 
* 인자, 인수, 매개변수, paramater, arguments

<em><strong>Constructor(생성자)</strong></em>
* <strong>객체지향 대명제 : 객체는 서로 다른 상태를 갖는다</strong>
* return 타입이 없다.
* 오버로딩가능
* 

## day6
///용어정리

has a :

API : Application Programming Interface

<strong>this() , super() , this. , super. </strong>

객체 생성시 this 와 super 가 같이 생성됨

<em><strong>package</strong><em>
 
 * 폴더 = 디렉토리 = 패키지(package)
 * 클래스의 묶음 단위
 * 일종의 네이밍 룰
 * opensource의 경우 도메인 이름의 역순으로 쓴다.
 * javac -d . 옵션을 써서 컴파일 가능하다.
 * package의 csv = .
 * classpath default = .; %java_home%\jre\lib\rt.jar;
 * import java.lang.* = default로 import (생략가능) // import 키워드로 다른 패키지 내의 클래스를 사용
 * java 문서는 ///Field ///Constructor ///Method ///main 순
 * <strong> java_home \ bin \ jar </strong> : jar은 자바압축기술
 * <strong> java_home \ jre \ lib \ rt.jar </strong> : 자바 클래스들을 모아놓은 jar 파일
 
<em><strong>Access Modifier(접근제어자)</strong><em>
 
 * Encapsulation(캡슐화) 
 * public / protected /_(default) / private
 
 1. public : 모든 외부에서 접근 가능
 2. protected : 동일 패키지, 상속구조에서 사용
 3. default : 같은 패키지에서 사용가능 (먼 친척보다 이웃사촌이 좋다~)
 4. private : 모든 외부에서 접근 불가
 
 <em><strong>Static</strong><em>
 
  * 클래스 이름으로 접근가능
  * static 키워드를 붙이면 static 영역에 생성됩니다. (공유의 의미를 가진다.)
  * 행동이 상태에 영향을 주지 못할 때 static 을 사용합니다.
  
  
## day7
  
  // String(immutable) , StringBuffer(mutable)

## day 8
 
 <em><strong>* Calendar</strong><em>
  * java.util.*; // util 패키지~ 
  * 시간은 항상 변하기 때문에 인스턴스 생성 불가 abstract 클래스로 만들어 두었다.
 <em><strong>* Date</strong><em>
  
 <em><strong>* DateFormat</strong><em>
  
  <em><strong>* SimpleDateFormat</strong><em>
   
  ### Wrapper 클래스  
   
   * autoBoxing &autoUnBoxing
   * 기본자료형을 레퍼런스 자료형으로 변환하여 처리
   
  ### Collection (자바의 자료구조)
   * java.util.Collection : 순서에 관계없는 객체들의 단순 모임
   * java.util.Set : 중복되지 않는 수학적 의미의 객체 , Collections를 상속
   * java.util.List : 순차적 나열에 의한 순서지정이 가능한 구조, Collections를 상속
   * SortedSet : 정렬된 Set
   * SortedMap : key가 정렬된 Map
   1. AyrrayList or Vector  List 인터페이스 구현
   2. Stack (LIFO) & Queue (FIFO)
   3. HashTable & HashMap
   
   <strong> 제네릭 기능 </strong>
   
   *  <> 추가
   * 다운캐스팅을 줄일 수 있는 구조로 변화
   
  ### Exception (처리)
   * 예외 : 프로그램 실행 중에 발생하는 예기치 않은 사건
   * 자바는 예외를 객체로 취급
   * java.lange 패키지에서 제공
   * Error, RuntimeException 클래스의 하위 클래스들을 제외한 모든 예외를 처리 (must be declared in the ....)
   * try-catch (catch는 다중으로 사용가능 가장 상위 catch는 더 하위 Exception을 작성하여야 오류가 발생하지 않는다.)
   * finally (반드시 실행)
   * throws
   * Exception 도 전부 계층구조
   * 예외를 stack구조로 보여준다.(printStackTrace)
   
   <오늘 헷갈린 부분 정리>
* API 잘보기
* static fianl을 통해 가독성 좋게 만들 수 있다 또한 runtimeError가 아닌 compilError 로 출력해서 실수를 잡을 수 있다.
* 삼항연산자 int a = (조건식) ? 참 : 거짓; 
    ```java
   String a = (i != numbers.length-1) ?",":"";
			System.out.print(a);
    ```
* 부모 데이터 타입으로 인스턴스 생성을 하여도 Overriding 된 메소드에 먼저 접근한다.
```java
//Object a = new String("이순신");
//System.out.println(a);
// >> 이순신  //이 출력되는 이유
class Test01
{
	public String toString(){
		return "test01입니다";
	}
}
class Test02 extends Test01
{
	public String toString(){
		return "test01을 상속받은 test02입니다";
	}
}

public class test
{
	public static void main(String args[]){
		/*
		Object obj = new Object();
		System.out.println(obj);
		Object obj2 = new String("이승현");
		System.out.println(obj2.toString());
		*/
		Test01 test01 = new Test01();
		System.out.println(test01.toString());

		Test02 test02 = new Test02();
		System.out.println(test02.toString());

		Test01 test03 = new Test02();
		System.out.println(test03.toString());
	}
}
```
	  
 ## day9
	  
<em><strong>Exception</strong></em>
	
* try - catch
* thorw
* thorws
* MyException extends Exception
* finally // 반드시 실행
* e.printStackTrace();
* Exception : checked (개발자가 커버 불가능) , unchecked(개발자의 실수 , RuntimeException)

//this.getClass().getName(); : 클래스의 이름 가져오는방법
