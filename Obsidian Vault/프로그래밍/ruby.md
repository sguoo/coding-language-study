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

<table>
<tr>
<td>
a==b
</td>
<td>

</td>
</tr>
</table>