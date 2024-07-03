# 자료형

<table style="margin:auto; width: 100%; text-size: 50px">
<tr>
<th style="text-align: center; padding: auto">
자료형
</th>
<th style="text-align: center; padding: auto">
적는 형식
</th>
</tr>
<tr>
<td style="text-align: center; padding: auto">
숫자
</td >
<td style="text-align: center; padding: auto">
2
</td>
</tr>
<tr>
<td style="text-align: center; padding: auto">
문자열
</td>
<td style="text-align: center; padding: auto">
'Hello World'
</td>
</tr>
<tr >
<td style="text-align: center; padding: auto">
불린, nil
</td>
<td style="text-align: center; padding: auto">
true, false, nil
</td>
</tr>
<tr>
<td style="text-align: center; padding: auto">
배열
</td>
<td style="text-align: center; padding: auto">
people=['ewq', 12312. 123, nil, false]
people[0] #=> ewq
</td>
</tr>
<tr>
<td style="text-align: center; padding: auto">
해시
</td>
<td style="text-align: center; padding: auto">
colors={'red' => 'ff0000'}
colors[red] #=> ff0000
</td>
</tr>
</table>

- ruby는 따로 앞에 int나 char같은걸 붙일 필요가 없다
- Lua와 마찬가지로 null이 아닌, nil을 쓴다 

# 객체지향
루비는 진정한 객체지향 언어이다. 루비에서 프로그래머가 다루는 모든 것은 객체이고, 작업의 결과 또한 객체이다. 많은 다른 프로그래밍 언어들도 같은 주장을 하지만, 
# 메서드
- 사람 이름과 함께 인사를 건네는 메서드
```ruby
def say_goodnight(name)
	result = "Good night, " + name
	return result;

#잠잘 시간
puts say_goodnight("John-Boy") #Good night, Johon-Boy
puts say_goodnight("Mary-Ellen") #Good night, Mary-Ellen
```

^5e3afe

루비 문법은 쉽다. 세미콜론을 뒤에 꼬박꼬박 넣지 않아도 된다

- `puts`에 결과를 넘겨주었는데, `puts`라는 메서드는 매개변수를 출력 할 때 위치를 다음 줄로 옮겨주는 줄 바꿈을 붙여서 출력한다
- 다음 코드를 보자
```ruby
puts say_goodnight("John-Boy")
puts(say_goodnight("John-Boy"))
```
- 루비에선 위의 코드 두개가 같은 뜻을 가진다
- 다만, 우선순위 문제 때문에 단순한 것이 아니라면, 괄호를 쓰는것이 권장된다

## 문자열
- 앞에 있는 [[ruby#^5e3afe|코드]]에는 문자열도 잇는데, 문자열 객체를 만드는 방법은 여러가지가 있는데, 그중 가장 일반적인 것이 문자열 리터럴[^1]을 사용하는 것이다.
- 작은 따옴표와 큰 따옴표로 묶는것에 차이가 있는데, 문자열을 처리하는 방법이 다르다
- 작은 따옴표를 사용하면, 몇가지 예외를 제외하고는 문자열 리터럴에 입력한 값이 그대로 문자열의 값이된다.
- 큰 따옴표로 묶으면, 더 많은 연산을 

[^1]: 작은 따옴표나 큰 따옴표로 묶인 문자의 스퀀스를 말한다
# 연산자

<details>
<summary>접기/펼치기</summary>
<table>
  <thead>
    <tr>
      <th>연산자 종류</th>
      <th>연산자</th>
      <th>설명</th>
      <th>예제</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>산술 연산자</td>
      <td>+</td>
      <td>덧셈</td>
      <td>a + b</td>
    </tr>
    <tr>
      <td>산술 연산자</td>
      <td>-</td>
      <td>뺄셈</td>
      <td>a - b</td>
    </tr>
    <tr>
      <td>산술 연산자</td>
      <td>*</td>
      <td>곱셈</td>
      <td>a * b</td>
    </tr>
    <tr>
      <td>산술 연산자</td>
      <td>/</td>
      <td>나눗셈</td>
      <td>a / b</td>
    </tr>
    <tr>
      <td>산술 연산자</td>
      <td>%</td>
      <td>나머지</td>
      <td>a % b</td>
    </tr>
    <tr>
      <td>산술 연산자</td>
      <td>**</td>
      <td>거듭제곱</td>
      <td>a ** b</td>
    </tr>
    <tr>
      <td>비교 연산자</td>
      <td>==</td>
      <td>두 값이 같은지 비교</td>
      <td>a == b</td>
    </tr>
    <tr>
      <td>비교 연산자</td>
      <td>!=</td>
      <td>두 값이 다른지 비교</td>
      <td>a != b</td>
    </tr>
    <tr>
      <td>비교 연산자</td>
      <td>></td>
      <td>크기 비교 (왼쪽이 큰 경우 참)</td>
      <td>a > b</td>
    </tr>
    <tr>
      <td>비교 연산자</td>
      <td><</td>
      <td>크기 비교 (오른쪽이 큰 경우 참)</td>
      <td>a < b</td>
    </tr>
    <tr>
      <td>비교 연산자</td>
      <td>>=</td>
      <td>크기 비교 (왼쪽이 크거나 같은 경우 참)</td>
      <td>a >= b</td>
    </tr>
    <tr>
      <td>비교 연산자</td>
      <td><=</td>
      <td>크기 비교 (오른쪽이 크거나 같은 경우 참)</td>
      <td>a <= b</td>
    </tr>
    <tr>
      <td>비교 연산자</td>
      <td><=></td>
      <td>비교 연산자 (왼쪽이 크면 1, 같으면 0, 오른쪽이 크면 -1)</td>
      <td>a <=> b</td>
    </tr>
    <tr>
      <td>비교 연산자</td>
      <td>===</td>
      <td>case 문에서 동일한지 비교</td>
      <td>(1..10) === 5</td>
    </tr>
    <tr>
      <td>대입 연산자</td>
      <td>=</td>
      <td>대입</td>
      <td>a = b</td>
    </tr>
    <tr>
      <td>대입 연산자</td>
      <td>+=</td>
      <td>더한 값을 대입</td>
      <td>a += b</td>
    </tr>
    <tr>
      <td>대입 연산자</td>
      <td>-=</td>
      <td>뺀 값을 대입</td>
      <td>a -= b</td>
    </tr>
    <tr>
      <td>대입 연산자</td>
      <td>*=</td>
      <td>곱한 값을 대입</td>
      <td>a *= b</td>
    </tr>
    <tr>
      <td>대입 연산자</td>
      <td>/=</td>
      <td>나눈 값을 대입</td>
      <td>a /= b</td>
    </tr>
    <tr>
      <td>대입 연산자</td>
      <td>%=</td>
      <td>나머지 값을 대입</td>
      <td>a %= b</td>
    </tr>
    <tr>
      <td>대입 연산자</td>
      <td>**=</td>
      <td>거듭제곱한 값을 대입</td>
      <td>a **= b</td>
    </tr>
    <tr>
      <td>논리 연산자</td>
      <td>&&</td>
      <td>논리 AND</td>
      <td>a && b</td>
    </tr>
    <tr>
      <td>논리 연산자</td>
      <td>||</td>
      <td>논리 OR</td>
      <td>a || b</td>
    </tr>
    <tr>
      <td>논리 연산자</td>
      <td>!</td>
      <td>논리 NOT</td>
      <td>!a</td>
    </tr>
    <tr>
      <td>논리 연산자</td>
      <td>and</td>
      <td>논리 AND (우선 순위가 낮음)</td>
      <td>a and b</td>
    </tr>
    <tr>
      <td>논리 연산자</td>
      <td>or</td>
      <td>논리 OR (우선 순위가 낮음)</td>
      <td>a or b</td>
    </tr>
    <tr>
      <td>논리 연산자</td>
      <td>not</td>
      <td>논리 NOT (우선 순위가 낮음)</td>
      <td>not a</td>
    </tr>
    <tr>
      <td>비트 연산자</td>
      <td>&</td>
      <td>비트 AND</td>
      <td>a & b</td>
    </tr>
    <tr>
      <td>비트 연산자</td>
      <td>|</td>
      <td>비트 OR</td>
      <td>a | b</td>
    </tr>
    <tr>
      <td>비트 연산자</td>
      <td>^</td>
      <td>비트 XOR</td>
      <td>a ^ b</td>
    </tr>
    <tr>
      <td>비트 연산자</td>
      <td>~</td>
      <td>비트 NOT</td>
      <td>~a</td>
    </tr>
    <tr>
      <td>비트 연산자</td>
      <td>&lt;&lt;</td>
      <td>비트 왼쪽 시프트</td>
      <td>a << b</td>
    </tr>
    <tr>
      <td>비트 연산자</td>
      <td>&gt;&gt;</td>
      <td>비트 오른쪽 시프트</td>
      <td>a >> b</td>
    </tr>
    <tr>
      <td>조건부 연산자</td>
      <td>?:</td>
      <td>삼항 조건 연산자</td>
      <td>a ? b : c</td>
    </tr>
    <tr>
      <td>범위 연산자</td>
      <td>..</td>
      <td>두 값을 포함하는 범위</td>
      <td>(1..10)</td>
    </tr>
    <tr>
      <td>범위 연산자</td>
      <td>...</td>
      <td>끝 값을 포함하지 않는 범위</td>
      <td>(1...10)</td>
    </tr>
    <tr>
      <td>기타 연산자</td>
      <td>defined?</td>
      <td>변수나 메소드가 정의되어 있는지 확인</td>
      <td>defined? a</td>
    </tr>
    <tr>
      <td>기타 연산자</td>
      <td>=~</td>
      <td>정규 표현식과 일치하는지 확인</td>
      <td>/pattern/ =~ string</td>
    </tr>
    <tr>
      <td>기타 연산자</td>
      <td>!~</td>
      <td>정규 표현식과 일치하지 않는지 확인</td>
      <td>/pattern/ !~ string</td>
    </tr>
  </tbody>
</table>
</details>

