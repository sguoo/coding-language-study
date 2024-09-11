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
# Props 사용 비교
```js
class App extends Compenent {
	render() {
		const { }
	}
}
```

## LigeCycle 비교
### 클래스형 컴포넌트
- LifeCycle API 사용
- 생성(mount) > 업데이트(update) > 제거 기능 구현
#### 함수형 컴포넌트
- Hook을 사용하여 생명주기 관리
- `useEffect`등의 Hook으로 LifeCycle