# Chapter 5. 표현식 & 문



## 5.1 값


- 값 value : **표현식(expression)이 평가(evaluate)되어 생성**된 결과 
- 평가 evaluate : 표현식을 해석하여 **값을 생성 or 참조**하는 것



## 5.2 리터럴 literal

@ 사전 : 문자 그대로의, 직역의
ex) The **literal** meaning of ‘petrify’ is ‘turn to stone’ 
    == petrify의 **문자 그대로의** 뜻은 ‘돌이 되다’이다.


리터럴 literal : **사람이 이해할 수 있는 문자 or 미리 약속된 기호를 사용해 값을 생성**하는 표기법(notation)

- 사람이 이해할 수 있는 문자 : 숫자, 알파벳, 한글 등
- 미리 약속된 기호 : '', "", ., [], // 등
-> 리터럴은 **런타임에 평가**되어 값으로 생성됨
-> **변수에 꽂혀서 값으로서 기능하는 모든 것**으로 이해할 수 있음

100 / 10.5 / 'hello' / true / null / undefined / {name:'lee', age:'32'} / [1, 2, 3] / function() {} 
위 모든 것들이 리터럴 (정수 리터럴, 문자열 리터럴, null 리터럴, 객체 리터럴, 배열 리터럴, 함수 리터럴 등)



## 5.3 표현식 expression

표현식 expression : **값으로 평가될 수 있는 모든 문(statement)** -> 리터럴 그 자체도 값으로 평가되므로 그 자체로 표현식
-> 표현식이 평가되면 새로운 값을 생성하거나 기존 값을 참조하게 됨


var score = 100; <- 100 == 리터럴 == 표현식
var score = 50 + 50; <- 50+50은 (평가되어 숫자 값 100을 생성하므로) 표현식
score; <- 식별자(를 참조하면 값으로 평가되므로) 이 자체로 표현식 (선언이 이미 존재할 경우에만)


**var score;** <- 변수 선언문은 값으로 평가될 수 없으므로 **표현식이 아니다**
-> 표현식이 아닌 문 == 값으로 평가될 수 없는 문

- [ var foo = **var x;** ]는 **불가능** (**값처럼 사용할 수 있어야만 표현식**)
- [ var foo = **x = 100;** ]는 **가능** (x=100 은 100이라는 값으로 평가됨)



## 5.4 문 statement (== 명령문)


문 statement : **프로그램을 구성하는 기본 단위** & **최소 실행 단위**
- 문 <- 선언문 / 할당문 / 조건문 / 반복문
- 프로그램 : 문의 집합 
- 프로그래밍 : 문을 작성하고 순서에 맞게 나열하는 것


토큰 token : 문법적으로 더 이상 나눌 수 없는 코드의 기본 요소

var sum = 1 + 2; 
-> tokens : var / sum / = / 1 / + / 2 / **;**



## 5.5 세미콜론 & 세미콜론 자동 삽입


- 0개 이상의 문을 **중괄호로 묶은 코드 블록 뒤**에는 **세미콜론 X**
- 문의 끝에 세미콜론을 붙이지 않아도 JS가 자동으로 삽입해주나, 예상과 다른 방식으로 작동하는 경우가 잦으니 붙여주는 것을 권장



