## 클래스형 컴포넌트
- `class`키워드 필요
- `Compenent`를 상속
- `render()` 메서드 필수
### 함수형 컴포넌트
- 더 간결한 코드
- `render()`메서드 불필요
- `Compenent`상속 불필요
## State 사용 비교
### 함수형 컴포넌트
-  뭔데 ㅅㅂ
## Props 사용 비교
```js
class App extends Compenent {
	render() {
		const { }
	}
}
```

### LigeCycle 비교
#### 클래스형 컴포넌트
- LifeCycle API 사용
- 생성(mount) > 업데이트(update) > 제거 기능 구현
##### 함수형 컴포넌트
- Hook을 사용하여 생명주기 관리
- `useEffect`등의 Hook으로 LifeCycle 기능 구현
## 이벤트 핸들링

## 결론
- 현재 React 공식 문서에서는 함수형 컴포넌트 사용을 권장
- Hook의 도입으로 함수형 컴포넌트의 단점 보완
- 클래
# React의 UI 구성과 컴포넌트 아키텍처
## UI 구성
### UI란?
User Interface
- 사용자가 직접 보는 화면
### 1단계:
UI 컴포넌트 계층으로 분리하기
![[rEact1]]

### 2단계:
정적인 웹페이지 만들기
##### 정적인 웹페이지란?
> 우리가 사용하는 웹 서비스는 크게 정적 웹과 동적 웹으로 나뉩니다

#### 3단계
##### 최소한의 State정의하기
###### State란?
- 애플리케이션이 기억해야하는 최서한의 변경 가능한 데이터를 의미
- DRY(Don't Repeat Yourself) 반복을 피해라
#### 4단계
##### State 위치 결정하기
#### 5단계
##### 역방향 데이터 흐름 추가하기
```JS
import {useState} from "react";
import Number from "."
```
![[React2]]
## 컴포넌트 아키텍쳐
![[rEact1]]
```js
function App() {
	return(
		<div>
			<PlusButton/>
		</div>
	)
}

export default App;
```
```js
function Other() {
	return(
		<div>
			<PlusButton/>
		</div>
	)
}
export default Other;
```
```js
function PlusButton() {
	return(
		<div onClick = {plus}>
		
		</div>
	)
}
export default PlusButton;
```

# 디자인패턴
소프트웨어 디자인 과정에서 자주 발생하는 문제들에 대한 일반적인 해결책
# MVC 패턴
- 디렉토리를 Model, View, Controller로 분리하여 사용하는 디자인 패턴
