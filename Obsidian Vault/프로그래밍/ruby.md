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
## 숫자
 - 단순히 숫자를 쓰면, 컴퓨터는 숫자로 인식한다
 `exemple = 1`

## 문자열
- 따옴표를 이용하여 감싸주면 문자열이 된다
`exemple = 'exemple'`

## 불린 nil

- 다른 언어에서의 bool과 null과 같다
```ruby
true
false
nil
```

## 배열

- 번호와 번호에 데이터로 이루어진 자료구조

```ruby
people = ['ewq', 213131, 3.12, nil, false]
people[0] # => 'ewq'
people[10] # => nil
```
- 대응되는 숫자에 아무 값이 없다면 nil이 된다
- 자료형은 상관 없다

## 해시

- 해시는 키를 값에 매핑할 수 있는 자료구조 

```ruby
colors = {'red'=>'ff0000', 'green'=>'00ff00'} #일반 데이터 타입
colors = {red: 'ff0000', green: '00ff00'} #symbol 데이터 타
```
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
