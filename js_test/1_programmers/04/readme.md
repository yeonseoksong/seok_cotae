# 연산자와 함수
>```+```, ```-```, ```*```, ```/``` 등 기본적인 계산을 할 수 있는 연산자에 대해 알아보고,
> 숫자 뿐만 아니라, 다양한 자료형에서 가능한 연산에 대해서도 알아보자.

### 목차
1. 산술 연산자
2. 함수 사용하기
3. 관계연산자
4. 연산자 우선순위

## 1. 산술 연산자(Arithematic operator)
- 이항 연산자(binary operator)
	- 두개의 피연산자(A, B)를 가지는 연산자.
	- 피연산자는 변수나 숫자가 될 수 있다.
	- ```+```, ```-```, ```*```, ```/```, ```%```

- 단항 연산자(unary operator)
	- 하나의 피연산자(A)를 가지는 연산자.
	- ```-``` 연산자가 있다.
		- ```-A```의 꼴로 사용하는 경우, ```-```는 이항 연산자가 아닌 단항 연산자이다.
		- 즉, -1을 곱한 효과

- 증감 연산자(```++```, ```-```);

- Math 관련 명령어
	- ```Math.pow(A, b)``` : A의 B승을 구해 준다.
	- ```Math.sqrt(A)``` : A의 제곱근을 구해 준다.
	- ```Math.random()``` : 0 ~ 1 사이의 임의의 난수를 발생시켜 준다.

## 2. 함수 사용하기
- 함수의 정의
	- 호출에 의해 여러번 실행할 수 있는 코드 블럭
		- 반복되는 코드 감소
		- 코드의 개발 및 수정 용이

- 함수 정의 구문
	
	```javascript
	function 함수이름(파라미터1, 파라미터2){
		/*
		   실행될 코드
		*/
		return 반환값;
	}
	```

	- 파라미터 : 함수의 정의부분에 나열되어 있는 변수
		- 여러 개인 경우 콤마(,)로 구분
		- 파라미터가 필요없는 경우 없어도 됨
		- **함수 안의 코드**에서 변수처럼 활용 가능

	- ```return``` 구문 :함수의 출력으로 내보낼 값
		- ```return``` 구문을 만나면 함수는 즉시 **종료됨**
		- 함수를 호출한 표현식은 **반환값**으로 대치됨

- 함수의 호출 방법 : ```함수이름(인자, ...)```의 형태로 호출

```javascript
var inp = prompt();
console.log("Hello World");
var randomValue = Math.random();
```

## 3. 관계연산자 (Relational Operator)
- 관계 연산자 : 두 표현식(A, B)의 관계를 비교하는 이항 연산자
	- 관계에 따라 boolean 타입의 true, false로 표현됨

	|관계연산자|동작|true인 예시|false인 예시|
	|```<```|A보다 B가 더 큰 경우 참|3<5|3<3|
	|```>```|A보다 B가 더 작은 경우 참|5>3|3>3|
	|```<=```|A보다 B가 크거나 같은 경우 참|3<=3|4<=3|
	|```>=```|A보다 B가 작거나 같은 경우 참|3>=3|3>=4|
	|```==```|A와 B가 같은 경우 참|3==3|4==3|
	|```!=```|A와 B가 같지 않은 경우 참|3!=4|3!=3|

- 논리연산자(Logical Operator) : 두 boolean 피연산자에 대해 연산하는 연산자
	- AND(```&&```) 연산자 : 두 피연산자가 모두 true인 경우에만 true를 나타내는 이항연산자
	- OR(```||```) 연산자 : 두 피연산자가 하나라도 true인 경우 true를 나타내는 이항연산자
	- NOT(```!```) 연산자 : 피연산자가 true인 경우 false를, false인 경우 true를 나타내는 단항 연산자
								  
## 4. 연산자 우선순위
- 우선순위 순으로 정리한 연산자
	- ```++```, ```--```
	- ```!```
	- ```*```, ```/```, ```%```
	- ```+```, ```-```
	- ```<```, ```<=```, ```>```, ```>=```
	- ```==```, ```!=```
	- ```&&```
	- ```||```

- 괄호 : 우선순위를 명시하기 위해 괄호를 사용. 괄호안의 계산식이 먼저 계산된다.
	- 부가적 효과
		- 코드의 가독성 향상
		- 연산자 우선순위 실수 방지
