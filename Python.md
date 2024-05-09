#파이썬 


# 자료형
#파이썬 #자료형 


### **연산**
#파이썬 #연산자 #연산

```python
>>> 10 + 5
15
>>> (10 - 5) * 2
5
```
- 파이썬은 소수점을 사용하지 않는 한 기본적으로 int 형으로 처리한다.
```python
>>> 2.2 * 5
11.0
>>> 1.0 / 0.2
5
>>> 3 / 2
1.5
```
- 파이썬은 소수점을 사용하거나 기본적으로 계산 결과가 실수인 경우에는 float형으로 
  처리한다.
- 나눗셈 결과를 정수 형태로 하고 싶으면 //연산자 사용, 나머지는 %을 사용한다.
```python
>>> 3 / 2
1.5
>>> 3 // 2
1
>>> 5 / 2
2.5
>>> 5 // 2
2
>>> 5 % 2
1
```
- 챗봇 개발에 필요한 딥러닝이나 통계 모델을 구현 할 경우 거듭제곱 연산 사용
- 파이썬에서는 거듭제곱 연산자로 ** 사용
```python
>>> 2 ** 5
32
>>> 2 ** 10
1024
```

## 변수
#파이썬 #변수

- 변수를 사용할 때는 등호(=)를 사용한다.
- 변수명은 숫자로 시작 불가능
```python
>>> a = 10
>>> b = 20
>>> a * b #변수 a와 b의 곱셈을 실행
200
```

## 문자열
#파이썬 #문자열 

- 문자열이란 문자들의 집합을 의미
- 파이썬은 큰 따옴표나 작은 따옴표를 이용하여 문자열을 표현
- 숫자 1234와 문자열 '1234'는 다르다.
```python
>>> '1234'
'1234'
>>> 'hello'
'hello'
>>> "hello"
'hello'
```
- 변수를 나타낼 때는 등호 사용
```python
>>> msg = 'Hello'
>>> msg
'Hello'
>>> error = 'err 404'
>>> error
'err 404'
```
- 작은 따옴표나 큰 따옴표를 사용할 때는 작은 따옴표는 큰 따옴표를, 큰 따옴표는 
  작은 따옴표로 감싸줌
```python
>>> msg1 = '"Nice to meet you", chatbot says'
>>> msg1
'"Nice to meet you", chatbot says'
>>> msg2 = "I'm programming now"
>>> msg2
"I'm programming now"
```
- 줄바꿈은 \\n 사용 복잡한 수면 작은따 따옴표 3개 또는 큰 따옴표 3개
- 메시지 출력은 print()함수
```python
>>> msg3 = 'Hello\nbro!!'
>>> msg3
'Hello\nbro!!'
>>>print(msg3)
Hello
bro!!
```
```python
>>>msg4 = '''Hello
...bro!!'''
>>>msg4
Hello\nbro!!
>>> print(msg4)
Hello
bro!!
```
```python
>>> msg5 = """Hello
... bro!!"""
>>> msg4
Hello\nbro
>>> print(msg5)
Hello
bro!!
```
>[!note] 이스케이프 코드란 프로그래밍할 때 사용 할 수 있도록 미리 정의해놓은 코드

이스케이프 코드
- \\n : 줄바꿈
- \\t : 탭
- \\\\ : 문자 \\ 출력
- \\' : 문자 ' 출력
- \\" : 문자 " 출력

## 리스트
 #파이썬 #리스트 
 
- 관계가 있는 데이터를 함께 관리할 때 사용
- 리스트는 대괄호\[]를 사용
- 데이터 요소는 쉼표( , )로 구분
```python 
리스트 명 = [요소1, 요소2, 요소3 ...]
```
- 리스트는 저장되는 요소들의 데이터형에 제한이 없기 때문에 정수 실수 같이 사용 가능
```python
>>> numbers = [1, 2, 3, 4, 5]
>>> numbers
[1, 2, 3, 4, 5]
>>> real_numbers[1.0, 2.0, 3.0, 4, 5]
>>> real_numbers
[1.0, 2.0, 3.0, 4, 5]
>>> type(real_numbers) #real_numbers의 타입 확인
<class 'list'>
```
- 리스트는 문자열과 마찬가지로 인덱싱과 슬라이싱 지원
- 각 요소에 접근하려면 인덱싱을 해야함
```python
>>> numbers = [1, 2, 3, 4, 5]
>>> numbers
[1, 2, 3, 4, 5]
>>> numbers[1]
2
>>> numbers[-1]
5
>>> numbers[2:]
[3, 4, 5]
>>> numbers[-2:]
[4, 5]
>>> numbers[1:-2]
[2, 3]
```
- 수정은 원하는 요소 위치에 새로운 데이터 대입
```python
>>> numbers = [1, 2, 3, 4, 5]
>>> numbers
[1, 2, 3, 4, 5]
>>> numbers[0] = 9
>>> numbers
[9, 2, 3, 4, 5]
```
- append( )는 리스트에 마지막에 요소를 추가하는 함수
- 리스트에 점( . )을 붙여 사용
```python
>>> numbers = [1, 2, 3, 4, 5]
>>> numbers
[1, 2, 3, 4, 5]
>>> numbers.append(9)
>>> numbers
[1, 2, 3, 4, 5, 9]
```
- insert( )는 원하는 자리에 데이터를 삽입하는 함수
```python
>>> numbers = [1, 2, 3, 4, 5]
>>> numbers
[1, 2, 3, 4, 5]
>>> numbers.insert(1, 1.5)
>>> numbers
[1, 1.5, 2, 3, 4, 5]
```
- pop( )는 리스트의 맨 마지막 요소나 원하는 위치의 요소를 꺼내면서 삭제하는 함수
```python
>>> numbers = [1, 2, 3, 4, 5]
>>> numbers
[1, 2, 3, 4, 5]
>>> numbers.pop()
5
>>> numbers
[1, 2, 3, 4]
```
```python
>>> numbers = [1, 2, 3, 4, 5]
>>> numbers
[1, 2, 3, 4, 5]
>>> numbers.pop(2)
3
>>> numbers
[1, 2, 4, 5]
>>> a = numbers.pop(3)
>>> a
5
>>> numbers
[1, 2, 4]
```
- 리스트 요소를 삭제할 때 pop( ) 함수 외에 del사용 가능
- pop( )와 다르게 꺼내지 않고 바로 삭제
```python
>>> numbers = [1, 2, 3, 4, 5]
>>> numbers
[1, 2, 3, 4, 5]
>>> del numbers[2]
>>> numbers
[1, 2, 4, 5]
```
- 리스트에 포함된 요소를 구하려면 len( ) 함수를 사용
```python
>>> numbers = [1, 2, 3, 4, 5]
>>> numbers
[1, 2, 3, 4, 5]
>>> len(numbers)
5
```
>[!note] 챗봇을 만들다보면 다른 함수 등장 가능

## 튜플
#파이썬 #튜플 

- 튜플은 리스트와 마찬가지로 다양한 데이터를 집합 형태로 관리 가능
- 한번 생성하면 내용 수정 불가능
- 대괄호\[ ] 가 아닌 소괄호\( ) 사용
```python
튜플명 = (요소1, 요소2, 요소3, ...)
```
- 튜플은 리스트와 마찬가지로 저장되는 요소들의 자료형 제한이 없음
```python
>>> numbers = (1, 2, 3, 4, 5)
>>> numbers
(1, 2, 3, 4, 5)
>>> real_numbers = (1.0, 2.0, 3.0, 4, 5, 'six') #다양한 자료형 사용
>>> real_numbers
(1.0, 2.0, 3.0, 4, 5, 'six')
>>> type(real_numbers) #real_numbers의 타입 확인
<class 'tuple'>
```
- 인덱싱과 슬라이스 지원
- 요소에 접근하려면 인덱싱 사용, 대괄호 사용
- 슬라이싱은 기존 튜플에서 잘라낼 시작위치와 끝위치, 쌍점을 사용해 새로운 튜플 생성
- 튜플의 요소를 변경할 수 없다는 점만 빼면 리스트와 동일
```python
>>> numbers = (1, 2, 3, 4, 5)
>>> numbers
(1, 2, 3, 4, 5)
>>> numbers[1]
2
>>> numbers[-1]
5
>>> numbers[2:]
(3, 4, 5)
>>> numbers[-2:]
(4, 5)
>>> numbers[1:-2]
(2, 3)
```
- **튜플의 요소는 변경 불가능**
- 변경하려하면 '튜플 객체는 요소 데이터를 할당하지 못한다'는 오류 출력
```python
>>> numbers = (1, 2, 3, 4, 5)
>>> numbers[0] = 9
Traceback (most call last):
    File "<stdin>", line 1, in <module>
TypeError: 'tuple' object does not support item assignment
```
- 새로운 요소를 추가할 수 없지만 덧셈 연산을 사용해서 데이터를 추가한 듯한 효과 가능
- 이때, 덧셈 연산은 튜플 객체끼리만 가능
```python
>>> numbers = (1, 2, 3, 4, 5)
>>> new_numbers = numbers + (6, 7)
>>> new_numbers
(1, 2, 3, 4, 5, 6, 7)
>>> numbers
(1, 2, 3, 4, 5)
```
- 튜플에 1개 요소 일 때 int형과 튜플을 덧셈 연산 했을때 오류가 뜸
```python
>>> numbers + (1)
Traceback (most recent call last):
	File "<stdin>", line 1, in <module>
TypeError: can only concatenate tuple (not "int") to tuple
```
- 단순히 보면 1개의 요소처럼 보이지만, 파이썬에서는 수학 연산의 소괄호인지 
  튜플의 소괄호 인지 구별 불가
- 그로 인해 튜플 요소임을 쉼표로 알려줘야 함
```python
>>> numbers + (1, )
(1, 2, 3, 4, 5, 1)
```
## 딕셔너리
#파이썬 #딕셔너리

- key와 value를 한 쌍으로 가지는 해시 형태의 자료형
- key와 value 한 쌍을 중괄호로 둘러싸고 있으며 쉼표( , )로 구분
- key는 숫자와 문자열만 사용 가능하고 value는 데이터의 형태 제한이 없음
```python
딕셔너리명 = { key1: value1, key2: value2, ...}
```
>[!note] 딕셔너리로 사용되는 key는 한번 정의되면 변경 불가능, 반면에 value는 언제든지 변경 가능
```python
>>> user1 = {'name' : '홍길동', 'age': 30, 'email': 'hong@habit.co.kr'}
>>> user1
{'name': '홍길동', 'age': 30, 'email': 'hong@habit.co.kr'}
>>> type(user1)
<class 'dict'>
```
- 위에서 저장된 변수 user1은 ↓와 같은 그림으로 저장됨

| Key     | Value               | Type          |
| ------- | ------------------- | ------------- |
| 'name'  | '홍길동'               | <class 'str'> |
| 'age'   | 30                  | <class 'int'> |
| 'email' | 'hong@hanbit.co.kr' | <class 'str'> |
- ↓는 key에 문자열을 사용했으며,  value에 리스트를 저장함
```python
>>> dict1 = { 'Kei': [100, 'hi', 4.5] }
>>> dict1['Kei']
[100, 'hi', 4.5]
>>> dict1['Kei'][1]
'hi'
```
- ↓는 key에 숫자를 사용
```python
>>> dict2 = { 10 : 'ten'}
>>> dict2[10] # Key가 10인 Value를 확인
'ten'
```
>[!note] 딕셔너리는 순서 없는 자료형이기 때문에, 리스트처럼 인덱스로 value에 접근 할 수 없고, key를 이용해 value에 접근해야 한다. 

>[!warning] 인덱스를 사용하면 오류가 발생한다. Key가 숫자인 경우에는 인덱스 처럼 보이기 때문에 주의해야한다.

- 딕셔너리에 새로운 key/value를 추가하는 방법은 대괄호를 이용해 원하는 key와 value를 저장하면 된다.
```python
>>> dict3 = { }
>>> dict3['a'] = 'A'
>>> dict3['b'] = 'B'
>>> dict3
{'a' : 'A', 'b' : 'B'}
```
- 리스트 자료형을 가지는 데이터 쌍을 딕셔너리에 추가 할 수 있다.
- 리스트나 튜플처럼 딕셔너리의 value에도 다양한 형태의 자료형을 추가 할 수 있다.
```python
>>> dic3[3] = [1, 2, 3]
>>> dic3
{'a' : 'A', 'b' : 'B' 3: [1, 2, 3]}
>>> dict3[4] = {'name':'Kei', 'age': 35}
>>> dict3
{'a' : 'A', 'b' : 'B', 3: [1, 2, 3], 4: {'name': 'Kei', 'age': 35}}
```
- 딕셔너리에 있는 데이터 쌍을 하나씩 삭제하는 방법과 모든 데이터 쌍을 한번에 
  삭제하는 방법이 있다
- 특정 key를 가지는 데이터 쌍을 삭제하기 위해서는 del 사용
- ※<span style="color:yellow"> 딕셔너리가 갖고있지 않은 key를 이용해 삭제하려 하면 에러 발생</span>
- 모든 데이터 쌍을 한 번에 삭제하기 위해서는 clear( )함수 사용
```python
>>> dek duct3['a']
>>> dict3
{'b': 'B', 3: [1, 2, 3], 4: {'name': 'Kei', 'age': 35}}
>>> del dict3[3]
>>> dict3
{'b': 'B', 4: {'name': 'Kei', 'age': 35}}
>>> dict3.clear()
{ }
```
## 불리언
#파이썬 #불리언
- 불리언<sup>boolean</sup>은 참과 거짓을 나타내는 자료형이다
- 간단하게 불<sup>bool</sup>로 나타내기도 한다
- 참은 True로, 거짓은 False로 표현한다
- ※<span style="color: yellow"> 첫 문자에 소문자 사용시 오류 발생</span>
```python
>>> check = True
>>> uncheck = False
>>> type(check)
<class 'bool'>
>>> uncheck
False
```
# 파이썬 제어문
#파이썬 #제어문
## if 조건문
#파이썬 #제어문 #조건문 if문

- 조건을 판단 했을 때 논리적으로 참일 경우에만 코드 수행
```python
if 조건1: #조건1이 True인 경우 실행
	코드
	코드
elif 조건2: #생략할 수 있으며 조건이 많으면 여러번 사용 가능
	코드 #조건2가 True인 경우 실행
	코드
else: #다른 조건이없는 경우 생략 가능
	코드 #if의 모든 조건이 해당되지 않는 경우 실행
	코드
```
- 파이썬 인터프리터에서는 if 제어문 내부로 들어갈 때 프롬프트가 ...으로 변한다
- 이때 ``Tab``키를 눌러 들여쓰기를 한다.
- ``Enter``키를 입력하면 if문을 빠져나오는 즉시 실행됨
```python
>>> check = True
>>> if check:
... Tab print('-' * 13)
... Tab print('check is true')
... Tab print('-' * 13)
... Enter
-------------
check is true
-------------
```