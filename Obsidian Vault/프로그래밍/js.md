# js로 뭘 할까?

## 웹 요소 제어

- 웹 요소를 가져와서 필요에 따라 스타일을변경하거나 움직이게 할 수 있음
- UI에 많이 활용

## 웹 애플리케이션 개발

- 실시간 애플리케이션 처럼 동작

## 다양한 라이브러리 사용 가능

- 웹을 중심으로 하는 서비스가 늘어나면서 브라우저에서 처리해야 할 일이 늘어남 → 라이브러리와 프레임워크가 계속 등장

## 서버를 구성하고 서버용 프로그램 개발 가능

- **node.js**: 프론트엔드 개발에 사용하던 자바스크립트를 백엔드 개발에서 사용 할 수 있게 만든 프레임워크

# 웹 브라우저가 자바스크립트를 만났을 때
## 웹 문서 안에 자바스크립트 작성하기

- \<script> 태그와 \</script> 태그 사이에 자바스크립트 소스 생성
- 웹 문서 어디든 위치할 수 있지만 주로 \</body> 태그 앞에 작성
- 자바스크립트 소스가 있는 위치에서 실행됨

## 외부 스크립트 파일 연결해서 작성하기

- 자바스크립트 소스를 별도의 파일(\*.js)로 저장한 후 웹 문서에 연결

## 자바스크립트 용어와 기본 입출력 방법

### 식과 문

#### 식

- 값을 만들어낼 수 있다면 모두 식이 될 수 있다
- 식은 변수에 저장된다

#### 문
- 문의 끝에는 세미콜론을 붙여서 구분
- 조건문, 제어문이 그 예

### 간단한 입출력 방법

#### 알림 창 출력

- '확인' 버튼이 있는 메시지 창 표시

- `alert(메시지)`

#### 확인 창 출력

- '확인' 과 '취소' 버튼이 있는 창 표시
- 클릭하는 버튼에 따라 프로그램 동작
- `comfirm(메시지)`

#### 프롬프트 창에서 입력받기

- 텍스트 필드가 있는 창 표시
- 사용자 입력 값을 가져와 프로그램에서 사용
- `prompt(메시지) 또는 prompt(메시지, 기본값)`

# 자바스크립트 기본 문법
## 변수 선언하기

- js에서 변수 선언은 var라는 예약어 뒤에 변수 이름을 적으면 된다
`기본형 var 변수명`
- 나이 계산 예제
```js
var currentYear = 2021;
var birthYear;
var age;

birthYear = prompt ("태어난 연도를 입력하세요. (YYYY)", "");
age = currentYear - birthYear + 1;
document.write(currentYear + "년 현재<br>")
document.write(birthYear + "년에 태어난 사람의 나이는" + age + "세입니다.")
```

## 자료형

### 숫자형
- 자바스크립트는 숫자형<sup>number</sup>라는 Int가 아닌 자료형을 사용한다
- 정수와 실수로 구분된다
### 문자열
- 문자열<sup>string</sup>은 작은 따옴표(' ')나 큰 따옴표 (" ")로 묶은 데이터를 의미한다
- 숫자도 감싸면 문자열로 인식된다
### 논리형
- 논리형은 불린<sup>boolean</sup>유형이라고도 한다
- 참<sup>true</sup>과 거짓<sup>false</sup>으로 나뉜다
### undefined 유형과 null 유형
- undefined 유형은 자료형이 정의되지 않았을 때의 데이터 상태를 나타낸다
- null은 데이터 값이 유효하지 않을 때를 의미한다
- undefined는 변수를 선언 한 상태로 값이 할당 되지 않은 것이고, null은 변수에 할당 된 값이 유효하지 않다는 것을 의미한다
### 배열
- 배열<sup>array</sup>는 하나의 변수에 여러 개 저장 할 수 있다
- 아래와 같이 데이터 값을 쉼표로 구분해서 대괄호로 묶으면 배열을 선언 할 수 있다
```js
배열명["값1", "값2", .....]
배열명[]
```
#### 사용하는 이유
```js
var spring = "봄";
var summer = "여름";
var fall = "가을";
var winter = "겨울";
```
배열로 작성하면
```js
var season = ["봄", "여름", "가을", "겨울"]
```

## 연산자
### 산술 연산자
- 수학 계산 할때 사용하는 연산자
- `-`, `+`, `*`, `/`등이 있다
- 다른 언어와 다른 점은 없다
### 할당 연산자
- 할당 연산자<sup>assignment aperator</sup>는 연산자(또는 연산식) 오른쪽의 실행 결과를 왼쪽 변수에 할당하는 연산자로 대입 연산자라고도 한다
- 할당 연산자와 산술 연산자를 합쳐 하나의 할당 연산자로 표시 가능
- `+=`, `*=`. `=`, `/=` 등이 있다
### 연결 연산자
- 연결 연산자는 둘 이상의 문자열을 합쳐서 하나의 문자열로 만드는 연산자
- 사칙연산의 더하기 연산자와 같은 `+` 기호를 사용한다
```js
document.write (birthYear + "년에 태어난 사람의 나이는 " + age + "세입니다.")
```
### 비교 연산자
- 비교연산자<sup>comparison operators</sup>는 두 값을 비교하는 연산자다
- `==`, `===`[^1], `!=`등이 있다

[^1]: =\==는 피 연산자가 같고, 자료형도 같으면 true를 반환한다
- 비교 연산자는 숫자 뿐만이 안니 문자열도 비교 할 수 있다
### 논리 연산자
- 논리연산자는 불리언<sup>boolean</sup> 연산자로고도 하며 true, false를 처리하는 연산자다
- true, false 자체가 피연산자인 연산자다
- `||`, `&&`. `!`등이 있다
## 조건문
### if문과 if~else문
- 피연산자 2개의 값을 비교해서 true나 false로 결괏값 반환
- 하나의 if~else문 안에 다른 if~else문을 넣을 수 있다
```js
if (조건) {
	결괏값이 true일때 실행할 명령
}
```
```js
if (조건) {
	결괏값이 true일때 실행할 명령
}
else {
	결괏값이 false일때 실행할 명령
}
```
### 조건 연산자로 조건 체크하기
- 조건이 하나이고 true일 때와 false일 때 실행할 명령이 각각 하나뿐일 때 간단하게 사용할 수 있음
`기본형` : `조건 ? true일 때 실행할 명령: false일 때 실행할 명령`
### 논리 연산자로 조건 체크하기
- 조건을 2개 이상 체크하려면 조건 연산자를 사용해 조건을 만듦
- 두 조건이 true일 경우, 조건 1개만 true일 경우 처럼 여러 경우를 따질 때 논리 연산자 사용

#### And 연산자
- 피연산자 2개 중에서 false가 하나라도 있으면 결괏값은 false
#### or 연산자
- 피연산자 2개 중에서 true가 하나라도 있으면 결괏값은 true
#### Not 연산자
- 결괏값을 반대로
### switch문
- 처리할 명령이 많을 경우 switch문이 편리
```js
switch(변수){
	case 조건:
		break;
}
```
### for문
```js
for(조건문, 조건, 증감식) {
	실행할 명령
}
```
#### 중첩된 for문
```js
for(조건문, 조건, 증감식){
	for(조건문, 조건, 증감식){
		실행할 명
	}
}
```

### while문
```js
while(조건){
	조건이 false일 때 실행
}
```
### do while문
```js
do{
	조건이 false일 때 실행 
}while(조건)
```
- 실행을 무조건 한 번 한다

- 4의 배수인지 판단하는 예제
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <h1 id="heading">자바스크립트</h1>
    <p id="text">위 텍스트를 클릭해 보세요</p>
    <script>
      var userNumber = parseInt("숫자를 입력하시오.");
  
      if (userNumber != null) {
        if (userNumber % 4 === 0)
          document.write(userNumber + "는 4의 배수입니다");
        else document.write(userNumber + "는 4의 배수가 아닙니다");
      }
    </script>
  </body>
</html>
```
# 함수와 이벤트
## 함수는 왜 사용할까?

- alert() 함수처럼 자신이 필요한 명령을 만들어 사용한다
- 숫자를 더하는 함수
```js
function addNumber(a, b) {
	var sum = a + b;
	alert(sum);
}
```
## var를 사용한 변수의 특징

### 변수의 적용 범위 스코프 알아보기
- 한 함수 내에서만 사용할 수 있는걸 지역 변수 또는 로컬 변수<sup>local variable</sup>라고한다
- 스크립트 소스 전체에서 쓸 수 있는걸 전역 변수 또는 글로벌 변수<sup>global variable</sup>라고 한다
- 함수 안에 변수를 선언하면 지역변수가 된다
### var와 호이스팅
- 선언과 할당을 분리해서 선언 부분을 위쪽으로 끌어 올리는것
```js
var x = 10;
function displayNumber() {
	console.log("x is " + x); //x is 10
	console.log("y is " + y); //y is undefined
	var y = 20;
}
displayNumber()
```
- undefined가 뜨는 이유는 할당이 아닌, 선언만 가져오기 때문에
- var를 사용하지 않는 이유
### 변수의 재선언과 재할당
- var는 재선언, 재할당을 할 수 있다
- 헷갈리고 실수를 할 수 있기 때문에 사용하지 않는다
## let와 const의 등장
- var 대신 let과 const 사용 권장
### let을 사용한 변수의 특징
- 블록 변수 선언
```js
function calcSum(n) {
	let sum = 0;
	for(let i = 1; i < n + 1; i++) {
		sum += i;
	}
	console.log(sum);
}
calcSum(10);
```
- 전역 변수 선언
```js
function calcSum(n) {
	sum(0); //전역변수 선언
	for(let i = 1; i < n + 1; i++) {
		sum += i;
	}
}
calcSum(10);
console.log(sum); //전역 변수 사용
```
#### 재할당은 되지만 재선언은 되지 않는 변수
- let은 재할당은 되지만 재선언은 된다
- var처럼 같은 변수의 이름을 사용할 걱정은 없다
- 블록 변수의 재할당
```js
function calcSum(n) {
	let sum = 0;
	for(let i = 1; i < n + 1; i++) { sum += i }
	sum = 100;
	console.log(sum);
}
calcSum(10);
```
#### 호이스팅이 없는 변수
- 호이스팅이 되지 않아 선언하기 전엔 사용 할 수 없다
```js
var x = 10;
function displayNumber() {
	console.log("x is " + x);
	console.log("y is " + y); //선언되지 않은 y를 사용
	let y = 20;
}
```

### const를 사용한 변수의 특징
- const로 선언한 변수는 상수[^2] 변수<sup>constant variable</sup>이다

[^2]: 변하지 않는 값
- 변하지 않는 값을 사용 할 때는 const를 쓰는 것이 좋다
- 이름이 같다면 재선언 할 수 없다
```js
const currentYear = 2020;
console.log(currentYear);
const currentYear; //오류 발생
```
- 재할당도 할 수 없다
```js
const currentYear = 2020;
console.log(currentYear);
currentYear = 2100; //currentYear 변수 재할당, TyoeError가 뜬다
console.log(currentYear)
```

## 재사용 할 수 있는 함수 만들기
### 매개변수, 인수, return 알아보기
- 앞에서 만든 `addNumber()`함수 처럼 입력값을 바꿀 수 있는 함수의 변수를 만드는 것을 
  매개변수<sup>parameter</sup>라고 하고, 함수를 호출할 때 괄호 안에 매개변수의 이름을 넣는다
- 여러개 사용시 쉼표를 찍어 나열한다
#### 함수 선언할 때 매개변수 지정 하기
- `num1`과 `num2`를 매개변수로 두는 함수 예제
```js
function addNumber(num1, num2) {
	var sum = num1 + num2
	return sum;
}
```
- 위 예제에서 `return`을 사용하여 결괏값을 함수를 사용한 위치로 되돌려 준다
- 이러한 동작을 값을 반환한다<sup>return</sup>라고 한다
- 위 예제에서는 sum 값을 반환한다

- 매개변수가 있는 함수를 호출 할 때 실제 값 부분을 인수라고 한다
- `addNumber()`함수를 선언할 때 괄호 안에 표시한 `num1`,`num2`를 매개 변수라 하고, `addNumber(2, 3)`처럼 괄호 안에 넣어준 숫자 2와 3을 인수라고 한다
```js
function addNumber(num1, num2) {
	var sum = num1 + num2;
	return sum;
}
var return = addNumber(2, 3) //2와 3이 인수
document.wrute("두 수를 더한 값: " + result);
```

# 함수표현식
## 익명함수
- 이름이 없는 함수를 만든다
- 익명 함수를 선언할 때는 이름을 붙이지 않는다
```js
sum = function (a, b) {
	return a + b;
}

doucment.write("함수 실행 결과: " + sum(10, 20));
```

## 즉시 실행 함수
- js가 실행될때 실행
```js
(function() {
	명렬
}(인수));
```

or

```js
(function(매개변수) {
	명령
}(인수));
```

## 화살표 함수

- `=>`표기법 (화살표 표기법)을 이용해 함수 선언을 더 간단하게 할 수 있다
- 간단히 화살표 함수라고 하는데, 익명 함수에서만 사용할 수 있다
- `(매개변수) => {함수 내용}`
### 매개변수가 없을 경우

```js
const hi = function() {
	return "안녕하세요?";
}
```

<p style="text-align: center">↓</p>
```js
const hi = () => { return "안녕하세요?" };
```

- 함수 내용이 한 줄 뿐이라면 중괄호를 생략할 수 있다. (return도 생략됨)
```js
const hi = () => "안녕하세요?";
```
## 이벤트와 이벤트 처리기
### 이벤트 알아보기
- 로딩이 끝나면 배경화면이 움직이거나 메인메뉴를 클릭시 서브메뉴가 열리는 것이 이벤트<sup>event</sup>이다
- 키보드를 누르는것, 웹페이지에서 새로운 페이지를 불러오는 것도 이벤트라고 부른다
- 자바스크립트의 이벤트는 주로 마우스나 키보드를 사용 할 때, 폼<sup>form</sup>에 내용을 입력할 때 발생한다
#### 마우스 이벤트
- 마우스 이벤트는 마우스를 이용해서 버튼이나 휠 버튼을 조작할 때 발생한다
<table>
<tr>
<th>
종류
</th>
<th>
설명
</td>
</tr>
</table>