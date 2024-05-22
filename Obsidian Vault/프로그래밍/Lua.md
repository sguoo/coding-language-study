## 장단점 
- 가볍다. 컴파일러의 용량이 수십 Kb정도, 정수도 없을 정도로 많은 데이터 형을 지원하지 않지만, 그만큼 가볍다.
- 언어의 문법이 굉장이 단순하다.
# 자료형
- 자료형으로는 `nil, boolean, number, string, function, table, userdata, thread`로 8가지가 있다.
### nil
- 널 값을 타 언어에서느 null로 적지만 Lua에서는 nil로 적는다.
## boolean
- 진리값은 boolean 타입 일때 true는 참 false는 거짓이다.
- boolean 타입이 아닐 때 경우, nil이 거짓이고 나머지는 모두 참이다. C언어와는 달리, 0도 참이다.
- false와 nil만 거짓이다.
# 연산자
- =\=의 반대 연산자로 !=혹은 <>를 적는데, Lua에서는 ~=로 적는다.
- 논리 연산자는 타 언어에서 !, &&, ||등을 