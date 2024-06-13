---
sticker: lucide//skull
---
# 스타일과 스타일 시트

## 스타일 시트
- 스타일 규칙을 한눈에 확인하고 필요할 때마다 수정하기 쉽도록 한군데 모아놓은 것
![[css Style]]

## 사용자 스타일
- 사이트 제작자가 만든 것

## 브라우저 기본 스타일
- 웹 브라우저에 기본으로 만들어져 있는 것

### 인라인 스타일
- 스타일 시트를 사용하지 않고 스타일을 적용할 대상에 직접 표시 한 것
```html
<h1>레드향</h1>
<p style="color: blue;"> 껍질에 붉은 빛이 돌아 레드향이라 불린다.</p>
<p>레드향은 한라봉과 귤을 교배한 것으로.....<p>
<p>비타민 C와 비타민 P가 풍부해 .....</p>
```

### 내부 스타일 시트
```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <title>상품 소개 페이지</title>
    <style>
      h1 {

        padding: 10px;
        margin: background-color: #222;
        color: #fff;
      }
    </style>
  </head>
  <body>
    <h1>레드향</h1>
    <p>껍질에 붉은 빛이 돌아 레드향이라 불린다</p>
    <p>레드향은 한라봉과 귤을 교배한 것으로 ..... </p>
    <p>비타민 C와 비타민 P가 풍부해 ..... </p>
  </body>
</html>
```

### 외부 스타일 시트
- 별도 파일로 저장해 필요할 때 가져오는 것

기본형: ```
```html
<link rel="stylesheet" href="외부 스타일 시트 파일 경로"
```
```html
<style>
h1 {
	padding: 10px;
	background-color: #222;
	color: #fff;
}
</style>
```
```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <title>상품 소개 페이지</title>
	<link rel="stylesheet" href="css/style.css">
  </head>
  <body>
    <h1>레드향</h1>
    <p>껍질에 붉은 빛이 돌아 레드향이라 불린다</p>
    <p>레드향은 한라봉과 귤을 교배한 것으로 ..... </p>
    <p>비타민 C와 비타민 P가 풍부해 ..... </p>
  </body>
</html>
```

# 기본 선택자
## 전체 선택자
- 페이지에 있는 모든 요소를 대상으로 적용할 때 사용
- 웹 브라우저의 기본 스타일을 초기화 할때 자주 사용

기본형 : ``  * { 속성: 값; ...} ``
```html
<style>![[css style.canvas]]
 *{
	 margin: 0;
 }
 </style>
```

## 타입 선택자
- 문서에서 특정 태그를 사용한 모든 요소에 스타일이 적용됨

기본형 : ``태그형 { 스타일 규칙 }``
`
```html
<style>
	p {
		font-style: italic; /* 이텔릭 체 */
	}
</style>

<div>
	<h1>레드향</h1>
	<p>껍질에 붉은 빛이 돌아 레드향이라 불린다</p>
	<p>레드향은 한라봉과 귤을 교배한 것으로</p>
	<p>비타민 C와 비타민 P가 풍부해</p>
</div>
```
## class 선택자
- 요소의 특정 부분에만 스타일 적용
- 마침표( . )다음에 클래스 이름 지정
- 문서 안에서 여러 번 반복할 스타일이라면 클래스 선택자로 정의
기본형 : ``.클래스명 { 스타일 규칙 }``
```html
	<style>
		p {
			font-style: italic; /* 이텔릭체 */
		}
		.accent {
			border: 1px solid #000 /* 테두리 */
			padding: 5px /* 테두리와 내용 사이의 여백 */
		}
		.bg {
			background-color: #ddd /* 배경색 */
		}
</style>
</head>
<body>
	<div>
		<h1 class="accent bg">레드향</h1>
		<p>껍질에 붉은 빛이 돌아 <span class="accent"> 레드향이</span>라 불린
		다
		</p>
		<p>레드향은 한라봉과 귤을 교배한 것으로</p>
		<p>비타민 C와 비타민 P가 풍부해</p>
	</div>
```

## id 선택자
- 요소의 특정 부분에만 스타일 적용
- 파운드(#) 다음에 id 이름 지정
- 문서 안에서 한번만 사용한다면 id 선택자로 정의
기본형 : ``#아이디명 { 스타일 규칙 }``
```html
(... 생략 ...)
<style>
	#container {
		width: 500px;           /* 너비 */
		margin: 10px auto;      /* 중앙 배치 */
		padding: 10px;          /* 테두리와 내용 사이 여백 */
		border: 1px solid #000; /*테두리 굵기와 색깔 */
	}
</style>
.....
<div id="container">
	 <h1>레드향</h1>
(... 생략 ...)
```
## 그룹 선택자
-  같은 스타일을 사용하는 선택자를 한꺼번에 정의
- 쉼표( , )로 구분해 여러 선택자를 나열
기본형 ``선택자1, 선택자2 { 스타일 규칙 }``
```html
<style>
	h1 {
		text-align: center; /*중앙 정렬*/
	}
	p {
		text-align: center;
	}
</style>
```
# 캐스케이딩 스타일 시트
## 캐스케이딩의 의미
- 캐스캐이딩(Cascading) : '위에서 아래로 흐른다'는 뜻. 즉 계단식으로 적용된다는 의미로 사용
- 선택자에 여러 스타일이 적용될 때 스타일 충돌을 막기 위해 우선순위에 따라 적용할 스타일을 결정함
## 스타일 충돌을 막는(캐스캐이딩)의 원칙
1. **스타일 우선순위** - 스타일 규칙의 중요도와 적용 범위에 따라 우선순위가 적용되고 그 우선 순위에 따라 위에서 아래로 스타일 적용
2. **스타일 상속** - 태그들의 포함 관계에 따라 부모 요소의 스타일을 자식요소로, 위에서 아래로 전달
>[!warning] 스타일 시트에서 '캐스캐이딩'은 가장 기본적인 개념이기 때문에 일반적으로 '스타일 시트'는 '캐스캐이딩 스타일 시트(CSS)'와 같은 의미로 사용됨

### **<span style="color: red;">원칙 1. 스타일 우선 순위</span>**

1. 얼마나 중요한가에 따라
![[Cascading style sheet 1|250]]

2. 얼마나 한정지을 수 있는가에 따라
![[Cascading style sheet 2|350]]

3. 소스 순서에 따라
	-  중요도와 명시도가 같다면 소스 순서에 따라 결정
	-  소스에서 나중에 온 스타일이 먼저 온 스타일을 덮어씀
```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <title>상품 소개 페이지</title>
	<style>
		p {
			color: black;
		}
		h1 {
			color: brown !important;
		}
		p {
			color: blue;
		}
	</style>
  </head>
  <body>
    <h1 style="color: green">레드향</h1>
    <p style="color: red">껍질에 붉은 빛이 돌아 레드향이라 불린다</p>
    <p>레드향은 한라봉과 귤을 교배한 것으로 ..... </p>
    <p>비타민 C와 비타민 P가 풍부해 ..... </p>
  </body>
</html>
```
### **<span style="color: red">원칙 2: 스타일 상속</span>**
- 자식요소에서 별도로 스타일을 지정하지 않으면 부모 요소의 스타일이 자식 요소로 전달 된다.
>[!warning] 배경색과 배경이미지는 스타일 상속이 되지 않는다. 그리고 상속만으로 모든 스타일의 충돌을 해결할 수 있는 것은 아니다.

# 스타일
## 글꼴 관련 스타일

___
### font-style 속성
- 글자를 이텔릭체 로 표시하는 속셩
### font-family 속성
- 웹 문서에서 사용할 글꼴 지정
- \<body> 태그를 비롯해 \<p> 태그나 \<hn>태그처럼 텍스트를 사용하는 요소들에서 사용
- 지정한 글꼴이 없을 경우를 대비해 두 번째, 세 번째 글꼴 까지 지정
- 둘 이상의 글꼴 이름을 지정 할 때는 쉼표( , )로 글꼴 구분
- \<body> 태그 스타일에서 한 번 정의 하면 문서 전체 적용에 적용되고 문서 안의 모든 자식요에 계속 같은 글꼴이 사용됨

### font-size 속성
- 폰트의 크기를 지정하는 속성
기본형: `font-size: <절대 크기> | <상대 크기> | <크기> | <백분율>`
#### 키워드를 이용한 글자 크기 지정하기
- `xx-smaill < x-smaill < small < medium < large < x-large < xx-large`

### font-weight
- 글자 굵기를 조절하는 속성
기본형: `font-weight: normal | bold | bolder | lighter | 100 | 200 | ... | 800 | 900`

## 웹 폰트 사용하기
### **웹 폰트란**
- 웹 문서 안에 글꼴 정보도 함께 저장했다가 사용자가 웹 문서에 접속하면 글꼴을 사용자 시스템으로 다운로드 시켜 사용하는 글꼴
- 사용자 시스템에 없는 글꼴이더라도 웹 제작자가 의도한 대로 텍스트를 표시 할 수 있다.
- @font-face 속성 사용
### **직접 웹 폰트 업로드해 사용하기**
1. 웹 폰트
## 텍스트 관련 스타일
### color 속성
- 글자 색 지정
- 16진수 값이나 rgb값, hsi 값, 색상 이름 중에서 사용
![[css pyogibub|1000]]
# 연결 서택자
- 연결 선택자: 선택자와 선택자를 연결해 적용 대상을 제한하는 선택자.
- **컴미네이션 선택자**<sup>combination selector</sup> 또는 '조합 선택자'라고도 함
## 하위 선택자<sup>descendant selector</sup>
- 부모 요소에 포함된<span style="color: darkred">모든 하위 요소에</span> 스타일이 적용된다.
- 자식 요소뿐만 아니라 손자 요소, 손자의 손자 요소 등 모든 하위 요소까지 적용
- 하위선택자를 정의할 때는 사