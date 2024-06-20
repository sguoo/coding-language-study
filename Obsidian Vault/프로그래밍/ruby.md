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

## 비교연산자

<details>

<summary>
| **연산자 종류**  | **연산자**    | **설명**                               | **예제**                |
| ----------- | ---------- | ------------------------------------ | --------------------- |
| **산술 연산자**  | `+`        | 덧셈                                   | `a + b`               |
|             | `-`        | 뺄셈                                   | `a - b`               |
|             | `*`        | 곱셈                                   | `a * b`               |
|             | `/`        | 나눗셈                                  | `a / b`               |
|             | `%`        | 나머지                                  | `a % b`               |
|             | `**`       | 거듭제곱                                 | `a ** b`              |
| **비교 연산자**  | `==`       | 두 값이 같은지 비교                          | `a == b`              |
|             | `!=`       | 두 값이 다른지 비교                          | `a != b`              |
|             | `>`        | 크기 비교 (왼쪽이 큰 경우 참)                   | `a > b`               |
|             | `<`        | 크기 비교 (오른쪽이 큰 경우 참)                  | `a < b`               |
|             | `>=`       | 크기 비교 (왼쪽이 크거나 같은 경우 참)              | `a >= b`              |
|             | `<=`       | 크기 비교 (오른쪽이 크거나 같은 경우 참)             | `a <= b`              |
|             | `<=>`      | 비교 연산자 (왼쪽이 크면 1, 같으면 0, 오른쪽이 크면 -1) | `a <=> b`             |
|             | `===`      | case 문에서 동일한지 비교                     | `(1..10) === 5`       |
| **대입 연산자**  | `=`        | 대입                                   | `a = b`               |
|             | `+=`       | 더한 값을 대입                             | `a += b`              |
|             | `-=`       | 뺀 값을 대입                              | `a -= b`              |
|             | `*=`       | 곱한 값을 대입                             | `a *= b`              |
|             | `/=`       | 나눈 값을 대입                             | `a /= b`              |
|             | `%=`       | 나머지 값을 대입                            | `a %= b`              |
|             | `**=`      | 거듭제곱한 값을 대입                          | `a **= b`             |
| **논리 연산자**  | `&&`       | 논리 AND                               | `a && b`              |
|             | `\|`       | 논리 OR                                | `a \| b`              |
|             | `!`        | 논리 NOT                               | `!a`                  |
|             | `and`      | 논리 AND (우선 순위가 낮음)                   | `a and b`             |
|             | `or`       | 논리 OR (우선 순위가 낮음)                    | `a or b`              |
|             | `not`      | 논리 NOT (우선 순위가 낮음)                   | `not a`               |
| **비트 연산자**  | `&`        | 비트 AND                               | `a & b`               |
|             | `\|`       | 비트 OR                                | `a \| b`              |
|             | `^`        | 비트 XOR                               | `a ^ b`               |
|             | `~`        | 비트 NOT                               | `~a`                  |
|             | `<<`       | 비트 왼쪽 시프트                            | `a << b`              |
|             | `>>`       | 비트 오른쪽 시프트                           | `a >> b`              |
| **조건부 연산자** | `?:`       | 삼항 조건 연산자                            | `a ? b : c`           |
| **범위 연산자**  | `..`       | 두 값을 포함하는 범위                         | `(1..10)`             |
|             | `...`      | 끝 값을 포함하지 않는 범위                      | `(1...10)`            |
| **기타 연산자**  | `defined?` | 변수나 메소드가 정의되어 있는지 확인                 | `defined? a`          |
|             | `=~`       | 정규 표현식과 일치하는지 확인                     | `/pattern/ =~ string` |
|             | `!~`       | 정규 표현식과 일치하지 않는지 확인                  | `/pattern/ !~ string` |
</summary>
</details>
