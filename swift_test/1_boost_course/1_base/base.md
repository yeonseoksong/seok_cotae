# 1. 스위프트 기초

### 목차
1. 강좌 소개
2. 명명법 / 콘솔로그 / 문자열 보간법
3. 상수와 변수
4. 기본 데이터 타입
5. Any, AnyObject, nil
6. 컬렉션 타입
7. 함수 기본
8. 함수 고급
9. 조건문
10. 반복문
11. 옵셔널
12. 옵셔널 추출

## 1. 강좌 소개
- 강의 개요
	- 기존의 프로그래머 또는 프로그래밍 개념이 있는 사람이 빠르게 스위프트 문법을 익힐 수 있도록 스위프트의 기초적인 핵심문법 제공

- 사전 숙지사항
	- 스위프트는 문법표현의 다양성이 높은 언어.
		- 그래서 스위프트 문법의 모든 형태를 알기에는 꽤 오랜 시간이 걸린다.
	
	- 최소한의 핵심 문법을 통해 무리없이 스위프트 문법을 익힐 수 있도록 간단한 예제와 함께 설명
	- 스위프트 문법의 모든 내용을 포함하지 않고, 깊은 내용보다 핵심적인 내용만을 전달한다.
	- 먼저 핵심적인 기초문법을 익힌 후, Apple **Swift Programming Language Guide** 또는 스위프트 관련 서적을 참고하면 좋다.
	- 해당 강의 : Swift 5 버전, **Swift 가이드 문서 변경 내역** 참고
	- 또한, 클래스, 함수, 변수 명은 스위프트의 **API 가이드라인**에 따라 명명하는 것이 좋다.


## 2. 명명법 / 콘솔로그 / 문자열 보간법
- 명명법
	- **Lower Camel Case** : function, method, variable, constant
		- ex : someVariableName
	- **Upper Camel Case** : type(class, struct, enum, extension, ...)
		- ex : Person, Point, Week
	- Swift는 모든 대소문자를 구분한다.

- 콘솔로그 남기기
	- ```print``` 함수 : 단순 문자열 출력
	- ```dump``` 함수 : 인스턴스의 자세한 설명(description 프로퍼티)까지 출력

- 문자열 보간법(String Interpolation) : 프로그램 실행 중 문자열 내에 변수 또는 상수의 실질적인 값을 표현하기 위해 사용
	- ```\()```
## 3. 상수와 변수
- 상수와 변수 선언
	- ```let``` : 상수 선언 키워드
	- ```var``` : 변수 선언 키워드 

- 상수 선언 후, 값 할당하기
	- 선언을 한 뒤, 나중에 값을 할당하려는 상수와 변수는 반드시 타입을 명시해야 한다.

## 4. 기본 데이터 타입
- Swift의 기본 데이터 타입
	- Bool
	- Int, UInt
	- Float, Double
	- Character, String

- Bool
	- true, falase

- Int, UInt
	- Int : 정수 타입, 현재는 기본적으로 64비트 정수형
	- UInt : 양의 정수 타입, 현재는 기본적으로 64비트 양의 정수형

- Float, Double
	- Float : 실수 타입, 32비트 부동소수형
	- Double : 실수 타입, 64비트 부동소수형

- Character, String
	- Character : 문자 타입, 유니코드 사용, 큰따옴표(" ") 사용
	- String : 문자열 타입, 유니코드 사용, 큰따옴표(" ") 사용

## 5. Any, AnyObject, nil
- Any : Swift의 모든 타입을 지칭하는 키워드
	- Any 타입에 Double 자료를 넣어두었더라도 Any는 Double 타입이 아니기 때문에 할당할 수 없다.
	- 만약 Double 타입을 사용해야 한다면, 명시적으로 타입을 변환해 주어야 한다. 

- AnyObject : 모든 클래스 타입을 지칭하는 프로토콜
	- AnyObject는 클래스의 인스턴스만 수용 가능하기 때문에 클래스의 인스턴스가 아니면 할당할 수 없다.

- nil : '없음'을 의미하는 키워드
	- 다른 언어의 NULL, Null, null 등과 유사한 표현
	- someAny는 Any 타입이고, someAnyObject는 AnyObject 타입이기 때문에 nil을 할당할 수 없다.
	- nil를 다루는 방법은 옵셔널 파트에서 다룬다.


## 6. 컬렉션 타입

## 7. 함수 기본

## 8. 함수 고급

## 9. 조건문

## 10. 반복문

## 11. 옵셔널

## 12. 옵셔널 추출

