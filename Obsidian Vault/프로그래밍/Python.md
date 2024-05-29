---
sticker: lucide//party-popper
---
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

## 이스케이프 코드
- \\n : 줄바꿈
- \\t : 탭
- \\\\ : 문자 \\ 출력
- \\' : 문자 ' 출력
- \\" : 문자 " 출력ㄷㄷ

## 리스트
 #파이썬 #리스트 
 
- 관계가 있는 데이터를 함께 관리할 때 사용
- 리스트는 대괄호\[]를 사용
- 데이터 요소는 쉼표( , )로 구분
```python 
리스트 명 = [요소1, 요소2, 요소3 ...]
```
- 리스트는 저장되는 요소들의 데이터 형에 제한이 없기 때문에 정수 실수 같이 사용 가능
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
>>> numbers[-1]e
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
>[!note] 파이썬에서는 곱셈연산을 이용해서 동일한 문자를 n번 출력할 수 있다. 사용자에게 문자열을 출력할 때 많이 사용된다
- check변수가 False일 때 cheack is false 문자열을 출력하는 코드
```python
>>> check = False
>>> if not check:
... Tab print('-' * 14)
... Tab print('check is false')
... Tab print('-' * 14)
... Enter
--------------
check is false
--------------
```
- check변수가 True 또는 False인지 검사할 때 \=\=연산자나 !=연산자 사용 가능
```python
>>> check = False
>>> if check == False:
... Tab print('-' * 14)
... Tab print('check is false')
... Tab print('-' * 14)
... Enter
--------------
check is false
--------------
>>> if check != True;
... Tab print('-' * 14)
... Tab print('check is false')
... Tab print('-' * 14)
... Enter
--------------
check is false
--------------
```
- 밑은 많이 사용하는 연산자다

- age 변수가 19 이상일 때와 미만일 때를 구분하기
```python
>>> age = 15
>>> if age >= 19:
... Tab print('You are an adult')
... else:
... Tab print('You are not an adult')
... Enter
You are not an adult
```

- 조건식이 여러개인 경우엔 elif 조건문 사용
- if 조건식이 False인 경우 순차적으로 그다음 elif 조건식을 조사하며 그 결과가 True일 때까지 내려간다
- elif의 조건식에서도 True가 아니라면 else 구문이 처리된다.
```python
>>> score = 84
>>> if score >= 90:
... Tab print('Grade A')
... elif score >= 80:
... Tab print('Grade B')
... elif score >= 70:
... Tab print('Grade C')
... else
... Tab print('Grade D')
... Enter
Grade B
```
- 거리 구간별로 요금을 측적 하는 예제
```python
>>> dist = 300
>>> if dist >= 0 and dist <= 50:
... Tab print('1000won')
... elif dist > 50 and dist <= 100:
... Tab print('2000won')
... else:
... Tab print('Over 3000won')
... Enter
Over 3000won
```

## while 반복문
#파이썬 #조건문 #반복문 while

-  조건이 False가 될 때까지 반복한다
-  조건이 참인 동안 반복문에 포함된 코드를 반복해서 수행한다
```python
while 조건:
	코드
	코드
	...
```
>[!warning] 조건이 False가 되지 않는다면 무한 루프에 빠진다.<br> 무한루프에 빠질시 시스템이 느려질 수 있다

- 1부터 10 까지의 숫자를 출력하는 예제
```python
>>> i = 1
>>> while i <= 10:
... Tab print('i=%d' % i)
... Tab i = i + 1
... Enter
i=1
i=2
i=3
i=4
i=5
i=6
i=7
i=8
i=9
i=10
```
>[!note] 문자열 포매터 %d를 사용해서 문자열 출력시 숫자 데이터로 치환하였다. 이를 문자열 포매팅 기능이라고 한다.

| <div style="background-color:white; color: black">문자열 포매팅 | <div style="background-color:white; color: black">설명 |
| --------------------------------------------------------- | ---------------------------------------------------- |
| %d                                                        | 10진수 출력                                              |
| %x                                                        | 16진수 출력                                              |
| %o                                                        | 8진수 출력                                               |
| %f                                                        | 실수 출력                                                |
| %s                                                        | 문자열 출력                                               |
|                                                           |                                                      |

```python
>>> while True: #무한루프
... Tab print('input number : ')
... menu = int(input())
... Tab if menu == 0: break #무한루프 중단
... Tab elif menu == 1: print('number one')
... Tab elif menu == 99:
... Tab Tab continue #continue는 조건 검사 없이 다음 루프 진행
... Tab elif menu == 2:
... Tab Tab print('number two')
... Tab else:
... Tab Tab print('another number')
... Enter
input number :
1
number one
input number :
2
number two
input number :
3
another number
input number :
99
input number :
0
```

## for문
#파이썬 #반복문 #제어문 for

- 리스트나 튜플, 문자열에서 요소를 하나씩 꺼내서 사용할땐 for문을 쓴다.
```python
for 변수 in 리스트|튜플|문자열:
	코드
	코드
	...
```
- 리스트 내용을 순차적으로 화면에 출력하는 예제
```python
>>> numbers = [1, 2, 3, 4, 5]
>>> for n in numbers:
... Tab print(n)
... Enter
1
2
3
4
5
```
- range( ) 함수를 이용하면 리스트를 쉽게 표현 할 수 있다. 숫자 리스트의 시작과 끝을 인자로 사용한다.
- 숫자 리스트를 for 반복문으로 출력하는 예제
```python
>>> numbers = range(1, 6)
>>> for n in numbers:
... Tab print(n)
... Enter
1
2
3
4
5
6
```
-  좌표(x , y)를 저장하는 리스트를 출력하는 예제
```python
>>> coord = [ (0, 0), (10, 15), (20 ,25) ]
>>> for x, y in coord:
... Tab print(x, y)
... Enter
0 0
10 15
20 25
```
- user 딕셔너리의 key만 모아서 dict_keys 객체로 반환하는 예제[^1]

[^1]: 딕셔너리 내부의 keys()함수를 이용한다

```python
>>> user = { 'name': 'Kei', 'age': 35, 'nationality': 'korea'}
>>> user.keys()
dict_keys(['name', 'age', 'nationality'])
```
```python
>>> user = { 'ame': 'Kei', 'age': 35, 'nationality': 'Korea'}
>>> for k in user.keys():
... Tab print(k)
... Enter
name
age
nationality
```

- user 딕셔너리의 value만 모아서 dict_values 객체로 반환하는 예제[^2]

[^2]: 딕셔너리 내부의 value()함수를 이용한다
```python
>>> user = { 'name':'Kei', 'age':35, 'nationality':'Korea'}
>>> user.values()
dict_values(['Kei', 35, 'Korea'])
```
```python
>>> user = { 'name':'Kei', 'age':35, 'nationality':'Korea'}
>>> for v in user.values():
... Tab print(v)
... Enter
Kei
35
Korea
```
- key/value 데이터 쌍 리스트를 반환하는 예제[^3]

[^3]: 딕셔너리 내부의 items()함수를 이용한다
```python
>>> user{ 'name': 'Kei', 'age': 35, 'nationality': 'Korea'}
>>> user.items()
dict_items([('name', 'Kei'), ('age', 35), ('nationality', 'Korea')])
```
```python
>>> user{ 'name': 'Kei', 'age': 35, 'nationality': 'Korea'}
>>> for k, v in user.items():
... Tab print(k,v)
... Enter
name Kei
age 35
nationality Korea
```
# 함수
#파이썬 #함수 
- 하나의 기능을 수행하는 코드들의 집합
- 반복적으로 수행하는 코드들을 기능 단위로 묶은 것
- 함수명으로 그 함수의 역할을 유추할 수 있어야합니다.
![[Python Funtion|200]]
- 파이썬에는 세가지 함수를 사용할 수 있다.
	1. 우리들이 만든 사용자 정의 함수
	2. 시스템 내장 함수
	3. 외장 함수
## 사용자 정의 함수
#파이썬 #함수 [[사용자 정의 함수| ]]
- 사용자가 직접 만든 함수
- 함수에 포함된 코드들을 묶으며, 소괄호 ( ) 뒤에 <span style="color:red">반드시</span> 쌍점 ( : )을 사용해야 한다
-  함수 명은 변수 명과 동일한 명명 규칙을 가지고 있다
- 경우에 따라서 인자와 결과 값 생략 가능
```python
def 함수명(인자):
	코드
	코드
	...
	return 결괏값
```
-  a와 b를 더해 그 결과를 반환하는 예제
```python
>>> def add(a, b):
... Tab return a+b
... Enter
>>> add(10, 20)
30
```
- 결과를 반환하지 않고 정보와 점수를 입력하면 화면에 출력하는 함수
```python
>>> def print_user(user, score):
... Tab print("name : %s" % user['name'])
... Tab print("age : %d" % user['age'])
... Tab print("score : %d" % score)
... Enter
>>> user = { 'name': 'Kei', 'age': 35}
>>> score = 86
>>> print_user(user,score)
name : Kei
age : 35
score : 86
```
## 내장 함수
#파이썬 #함수 [[내장함수| ]]
- 파이썬에 기본적으로 내장되어 있는 함수
- 별도로 모듈을 import하지 않아도 사용 할 수 있다
### format( )
- 기본적으로 %d와 동일한 기능을 하며 변수 타입과 상관없이 중괄호와 순서에 맞는 인덱만 사용하면 된다
```python
>>> print('integer : {} / float : {} / string : {}'.format(10.3.14, "hello"))
integer : 10 / float : 3.14 / string : hello
>>> print('integer : {0} / float : {1} / string : {2}'.format(10.3.14, "hello"))
integer : 10 / float : 3.14 / string : hello
>>> print('float : {1} / integer : {0} / string : {2}'.format(10.3.14, "hello"))
float : 3.14 / integer : 10 / string : hello
```
### enumerate( )
- 순서가 있는 자료형을 입력하면 인덱스를 포함한 요솟값을 반환한다
- for 반복문을 이용해 순서가 있는 자료형을 탐색할 때 편하다
```python
>>> numbers = [10, 11, 12, 13, 14]
>>> for idx, value in enumerate(numbers):
... Tab print('index:{} / value:{}'.format(idx,value))
... Enter
index: 0 / velue: 10
index: 1 / velue: 11
index: 2 / velue: 12
index: 3 / velue: 13
index: 4 / velue: 14
```
### str( )
- 입력으로 들어온 데이터를 문자열 객체로 반환
```python
>>> str(10)
'10'
>>> type(str(10))
<class 'str'>
>>> str("hello")
'hello'
>>> str("hello".upper())
'Hello'
>>> str("HELLO".lower())
'hello'
>>> str([1,2,3])
'[1,2,3]'
```
### join( )
- 리스트에 포함되어 있는 요소들을 지정한 구분자로 구분해 문자열로 반환 하는 함수
- 리스트 내 요소들을 문자열로 합칠 때 자주 사용
```python
>>> names = ['Kei', 'Tonny', 'Grace', 'Jenny', 'Jaeyoo']
>>> ','.join(names)
'Kei,Tonny,Grace,Jenny,Jaeyoo'
>>> '/'.join(names)
'Kei/Tonny/Grace/Jenny/Jaeyoo'
```
### split( )
- join( )함수와 반대로 문자열을 특정 구분자를 기준으로 분리해 리스트로 반환하는 함수
```python
>>> names = ['Kei', 'Tonny', 'Grace', 'Jenny', 'Jaeyoo']
>>> names_str = ','.join(names)
>>> names_split = names_str.split(',')
>>> names_split
['Kei', 'Tonny', 'Grace', 'Jenny', 'Jaeyoo']
```
### id ( )
- 객체의 고유 주솟값을 반환
- 컴퓨터나 운용체제에 따라 바뀔 수 있다.
```python
>>> a = 10
>>> id(a)
140735531391704
>>> b = a
>>> id(b)
140735531391704
```
### find( )
- 특정 문자열을 찾기 위해 사용한다
- 찾으려는 문자열을 입력 받으면 그 문자열의 시작 위치를 반환한다
- 찾지 못한다면 -1을 반환한다
```python
>>> str = "I want to be a great programmer"
>>> str.find("be")
10
>>> str.find("I")
0
>>> str.find("i")
-1
```
### strip( )
- 문자열 양쪽 끝의 공백을 제거하는 함수
```python
>>> str = " I want to be a great programmer. "
>>> new_str = str.strip()
>>> new_str
'I want to be a great programmer.'
```
### filter( )
- 개별 요소를 반복적으로 셀 수 있는 객체<sup>iterable object</sup>를 입력 받아 각 요소를 함수로 수행 한 후 결과가 True인 것만 묶어서 반환 한것
```python
>>> def is_even(number):
... Tab return number % 2 == 0
... Enter
>>> numbers = range(1, 21)
>>> even_list = list(filter(is_even, numbers))
>>> print(even_list)
[2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
```
>[!note] list생성자는 생략가능한 하나의 인자를 가지며 인자로 들어온데이터(객체)를 리스트로 반환한다

>[!warning] filter( )함수는 filter객체 형태로 반환 하기 때문에 리스트 형태로 사용불가, 사용하려면 list생성자를 사용해야함

### lambda 키워드
- lambda(람다)는 함수를 생성할 떄 사용하는 키워드이다.
- 주로 함수를 정의할 때 사용한다
- def보다 간결하게 정리 할 수 있다
- 복잡한 경우 def 사용, 간결한 경우 lambda 사용
`lamda 인자1, 인자2, ..., 인자n: 코드`
- 인자로 얻은 변수 x에 2를 곱하는 lambda함수와 def함수 비교 그림
![[lambda def bigyo]]
lambda를 사용하는 예제
```python
>>> f = lambda x: x*2
>>> f(2)
4
>>> f(4)
8
```
filter( )함수에 lambda를함수를 사용하는 예제
```python
>>> numbers = range(1, 21)
>>> even_list = list(filter(lambda n: n%2==0, numbers))
>>> print(even_list)
[2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
```
### map( )
- 개별 요소를 반복적으로 셀 수 있는 객체를 입력 받아 각 요소를 함수로 수행 한 후 결과를 보이 반환
- map( ) 함수는 바로바로 계산하지 않기 때문에 게으른 연산<sup>lazy evaluation</sup>을 한다함.
- 결괏값이 필요 할 때까지 계산 하지 않음
```python
>>> def square (number):
... Tab return number ** 2 #**연산자는 제곱을 의미
... Enter
>>> numbers = range(1, 5) #1, 2, 3, 4
>>> square_list = list(map(square, numbers))
>>> print(sqaure_list)
[1, 4, 9, 16]
```
- lambda 함수 활용
```python
>>> numbers = range(1, 5)
>>> square_list = list(map(lambda x : x**2, numbers))
```
## 외장 함수
``import 모듈명``
### sys
- sys는 파이썬 인터프리터와 관련된 정보와 기능을 제공하는 모듈
- 특히 명령행에서 인수를 전달받기 위해 많이 사용함
- ↓처럼 명령 프롬프트 상에서 파이썬 프로그램을 실행할 때 인자 추가 가능
`> python for_test.py 'hello 10`
- 이 값은 sys.argv 리스트에 저장된다
- 전달받은 인수를 이용해 메시지를 출력하는 방법
```python
import sys # sys 모듈 불러오기

print(sys.argv) # 시스템 인자로 들어온 리스트 내용 출력
msg = sys.argv[1] # 'hello'
cnt = int(sys.argv[2]) # 10

for i in range(cnt):
	print(i, msg)
```
- for_test.py 파일을 저장한 경로로 이동해 파이썬 프로그램 실행했을때
```cmd
> python for_test.py 'hello' 10
['for_test.py', 'hello', '10']
0 hello
1 hello
2 hello
3 hello
4 hello
5 hello
6 hello
7 hello
8 hello
9 hello
```
- 종료 할 때는 sys.exit( ) 입력
```python
>>> import sys
>>> for n in range(100):
... Tab print(n)
... Tab if n == 10:
... Tab Tab sys.exit()
... Enter
0
1
2
3
4
5
6
7
8
9
10
# 프로그램 종료됨
```
### pickle
- pickle 모듈은 파이썬 객체를 파일로 저장하고 메모리로 읽어올 수 있도록 하는 모듈
- 저장해 놓은 상태에서 프로그램 종료시 객체 내용 다 사라짐
```python
>>> import pickle # pickle 모듈 임포트
>>> f = open('setting.txt', 'wb')
>>> setting = [ {'title': 'python program'}, {'author': 'Kei'} ]
>>> pickle.dump(setting, f)
>>> f.close()
```
# 클래스
- 객체지향 언어에서는 객체를 생성하기 위해 언어 차원에서 클래스를 지원
- 유사한 기능으로 묶으면 프로그램 복잡도를 낮출 수 있음
## 객체, 인스턴스
- 파이썬에서 사용하는 모든 자료형은 객체
- 객체는 메모리에 적재 되어야만 사용 가능
- 이런 객체를 이용해 프로그래밍 하는 것을 객체지향 프로그래밍이라고 함
- 객체가 어떤 클래스를 나타내는 경우엔 인스턴스<sup>instance</sup>라고 부른다.
- 언어에 따라서는 혼용하여 사용하기도 함
- 파이썬에서 생성하는 모든객체는 인스턴스
- 인스턴스를 만들려면 클래스를 사용해야함
- 클래스는 인스턴스를 만들기 위한 설계도
```python
class 클래스명:
	...
```

>[!note] 이번 예제부터는 파이썬 인터프리터를 이용하기엔 불편하다.  </br>따라서 앞으로는 굳이 `Tab`이나 `Enter`를 표기하지 않겠다.


- 간단한 인사 메시지와 챗봇이름을 출력하는 예제
```python
#챗봇 클래스
class Charbot : #1
	def sayHello(self): #2
		print("say hello")

	def sayMyName(self): #3
		print("My name is Kbot :D")

#챗봇 인스턴스 생성
chatbot = Chatbot() #4
chatbot.sayHello() #5
chatbot.sayMyName() #6
```
1. Chatbot이라는 클래스를 정의한다. 보통 클래스의 첫 글자는 대문자로 쓴다. [^4]
2. 'say hello'문자열을 출력하는 메서드를 정의한다. 클래스의 매서드를 정의할 때는 함수를 정의할 때와 마찬가지로 def키워드를 사용한다.
	- 첫 번째 인자로 반드시 self 키워드를 사용해야함. 지금은 클래스 자신(self)이 갖고있는 메서드로 이해
3. 'My name is Kbot :D' 문자열을 출력하는 메서드를 정의한다
4. Chatbot 클래스의 인스턴스를 생성한다
5. sayHello( ) 메서드를 호출한다. 생성된 인스턴스에서 점( . )을 사용해 원하는 메서드를 호출한다
6. sayMyName( ) 메서드를 호출한다

[^4]: 일반 변수랑 구별하기 위함
```python
#결과
say Hello
My name is Kbot :D
```
## 생성자와 소멸자
- 인스턴스가 생성될 때 자동으로 호출하는 생성자<sup>constructor</sup>라는 메서드를 제공한다
- 생성자 메서드명은 사용자가 임의로 정할 수 없다.
- 생성자 메서드로 \_init_을 사용한다