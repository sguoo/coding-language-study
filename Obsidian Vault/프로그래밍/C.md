---
sticker: lucide//skull
---
```c
#include
```

#c
# main 함수

c언어 중괄호로 묶어줄 경우 이를 코드 블록이라 한다

리턴 값이 없는 main을 사용해도 되나, ANCI 표준은 int main()

문장의 끝 세미콜론(;)

한 문장을 종료해 주는 역할

반드시 넣어 줘야 한다.

가독성이 떨어지기 떄문에 ;을 쓸때마다 줄넘김

블록의 지정 중괄호 {}


# 자료형
#c #자료형


## 주석과 함수
#c #주석 #함수 

### 주석 - 사람만 알아볼 수 있도록 적은 설명

→ 컴파일러가 처리하지 않아 프로그램에는 영향을 주지않는다 

\\한 줄 주석

\\*
여러 줄

주석*\

설명할 때 사용


### 함수 - 어떤 작업을 수행하는 코드 / 재사용성을 높여준다
#c #함수

### 전 처리기
#c #전처리기 

전 처리기 컴파일러가 프로그램을 번역하기 전 처리하는 프로그램

→ 모든 전 처리기는 \#로 시작한다

주요 전 처리기 지시자 - \#include, \#define

\#include

파일 포함 지시자

헤더 파일 (header.file) <.h>, “.h”

코드 맨위에 존재하고 있으며, 개발자가 쉽게 코딩을 할 수 있도록 함수나 클래스를 미리 지정해놓은 파일을 의미

<>: 보통 표준 라이브러리 포함할떄 사용한다

“” : 현재 소스파일을 기준으로 헤더파일 포함.

만일 찾지 못하면 컴파일 옵션의 지정된 헤더파일 경로에서 찾는다

ex) “message.h”, “./message.h”, “./header/message.h”

stdio.h : Stardard I/O 라이브러리의 헤더파일
```
#define
```
다른 문자열로 대치될 단어 (매크로 macro)를 정의함

마지막에 ;을 붙이지 않는다


### 상수
#c #상수 

38, 75, 63과 같은 데이터를 직접 표현하거나 저장할 수 있음


## 변수
#c #변수

값을 저장하는 메모리 공간

모든 프로그래밍의 핵심 요소

2차 방정식 a^2 + b^2 = c^2의 변수 a, b, c 와 같은 의미

변수에 저장되는 값은 변경 가능

### **변수 선언과 쓰임**

C변수에 저장하는 값의 종류와 저장되는 범위(크기)에 따라 변수를 다르게 사용해야 하는데, 처음 변수를 지정하는 것

반드시 변수를 사용하기 전에 선언 해야함

### **변수 선언 규칙**

변수 이름은 알파벳, 숫자 언더바(_)로 구성된다

대소문자를 구분한다.(Num과 num는 다른 변수이다.)

숫자로 시작할 수 없고 키워드도 사용할 수 없다

이름 사이에 공백이 삽입될 수 없다

### 변수의 초기화

변수 선언 과정에서 변수의 초기값을 저장할 수 있음

쉼표(,)를 사용하여 동일한 자료형의 여러 변수를 하나의 선언문에서 선언하고 초기화 할 수 있음

#c #자료형 #기타
## 기타 자료형

### 비트(bit)와 바이트(byte)

컴퓨터의 모든 데이터는 2진수

1 비트(bit) = 컴퓨터의 최소단위 0 또는 1을 표시

1바이트(byte) = 8비트(bit), 1문자(영문자) = 1바이트 (byte)

사이즈 구하기 : sizeof(자료형)

unsigned : 0과 양수 만을 표현한다

### 숫자의 범위

int형이 4byte(32bit) → 2^-31 ~ 2^31 -1 (singed인 경우)

→ 자료형의 크기로 인해 논리적 오류 발생할 수 있다

기타 자료형

→ void

### 아스키 코드

미국 표준 협회에 의해 정의된 코드

컴퓨터는 0과1 이진수로 이루어져 있기 때문에 문자를 표현하기 위한 표준 코드

문자와 숫자의 연결 관계를 정의

ASCII 코드의 범위는 0이상 127이하

# scanf()

키보드로부터의 데이터 입력

데이터 입력 시, 데이터를 구분하는 기준은 공백

입력의 끝에는 반드시 엔터 키를 입력해 마무리

 
# 조건문
#c #조건문 

2줄 이상일땐 블록으로 묶어 줘야한


## if 조건문
#c #조건문 #if 

조건을 만족하면(TRUE이면) 특정 명령을 실행하고, 조건을 만족하지 않으면 아무 명령도 실행하지 않는 프로그램의 흐름

```c
if (조건){
	조건이 참일 경우 실행
}
else {
	조건이 거짓일 경우 실행
}
```

## &&연산자의 이용
#c #조건문 #연산자 #and

모든 조건이 참일 경우에만 참이 되는 연산

```c
if (score1 >= 60 && score2 >= 60)
	printf("합격\\n");
else
	printf("불합격\\n");
```


## 조건 연산자
#c #조건문 #연산자 #삼항연산자

경우에 따라서 if~else문을 대신하여 사용할 수 있는 연산자

‘상 향 연산자’라고도 불린다

기호 ? 와 : 로 구성

피연산자는 ‘조건’, A 그리고 B

문장에 따라서 조건 연산자는 if~else문 보다 간결한 표현 가능

```c
printf(num>0 ? "true" : "false")
```

### switch문
#c #조건문 #switch

조건에 따라 해당 레이블로 이동하여 실행을 계속하는 제어문

실행 위치에 대한 표시는 case와 default 레이블 사용

레이블에 사용되는 숫자나 switch문에 전달되는 값 모두 정수이어야 한다

## 스코프와 지역변수
#c #지역변수

```c
#include <stdio.h>

int main(void)
{
	int num = 1;
	if (num == 1) {
		int num = 2;
		num++;
		printf("...%d", num);
	}
	else {
		num++;
		printf("... %d..", num);
	}
	printf("...%d...", num);
	
}
```

스코프와 지역 변수

중괄호 내에 선언이 되는 변수를 가리켜 지역변수라 한다

지역변수는 선언된 중괄호를 벗어나면 메모리 공간에서 소멸된

## while() 반복문
#c #조건문 #반복문 while문

while(조건)문은 조건이 참일때까지 계속 반복 실행한다

while문은 주어진 ‘반복의 조건’이 ‘참’인 동안 ‘반복의 영역’을 반복 실행

반복의 영역이 둘 이상의 문장으로 구성되면, 중괄호로 묶는다.

while은 조건이 거짓이면 한 번도 실행되지 않을 수 있다

### 무한루프

while문의 반복조건으로 1이오면 반복조건은 항상 참이 되어 무한루프를 형성(1은 논리적으로 참)

무한루프도 소프트웨어 개발에서 흔히 사용되는 기술

```c
int main(void){
	int i=0;
	
	while(1);
	{
		printf("%d 번째 Hello World \\n", i+1);
		i++
		}
	return 0;
}
```

## do while() 반복문
#c #조건문 #반복문 do while문

do~while의 특징

while문과 달리 조건검사를 뒷부분에서 진행

때문에 while문과 달리 조건에 상관없이 반복영역을 최소 1회 실행

```c
int main(void)
{
	int i = 1;
	int dan;
	
	printf("몇 단의 출력을 원하는가? ");
	scanf("%d", %dan)
	do
	{
	printf("%d x %d = %d\\n",dan,i,dan*1)
	i++
	}while(i<10);
	return 0;
}
```

뒤에있는 while에 세미콜론을 붙여야 한다.

## for문
#c #조건문 #반복문 for문

while문처럼 반복문으로서 원리는 같지만 펴햔 방법이 다름.

조건 식을 포함하여 초기 식(시작 값), 증감 식 등 2가지를 더 넣을 수 있음

반복문을 사용하는 목적 중 하나

정해진 횟수만큼 반복 실행하기 위함

반복문의 기본 구성 3요소

반복 횟수를 세기 위한 변수

반복문의 탈출 조건

탈출 조건 성립을 위한 연산

while문은 기본 구성 3요소가 뿔뿔이 흩어져있다(반복 횟수의 확인이 불편)

for문은 기본 구성 3요소가 한 줄에 나열되어있다.(for문의 장점)

for문과 while문은 상호 변경이 가능

break 와 continue

```c
#include <stdio.h>

main()
{
	int num;
	while(1)
	{
		printf("%d" &num);
		scanf("%d", &num);
		if (num < 0) break;
		if (num == 0) continue;
		if (num % 2 == 1)
			printf("홀수\\n");
	}
	else
		printf("짝수\\n");
}
```

break문은 switch문과 각종 반복문을 빠져나가는데 사용 됨

continue 문은 반복문의 나머지 검사를 허용하고 다음 검사를 빠져나간다

# 배열
#c #배열


배열 사용하기

```c
#include <stdio.h>
int main(void){
	int score[10] = {1,2,3,4,5,6,7,8,9,10};
	for (int i = 0; i<=10; i++){
		printf("%d", score[0]);
	}
}
```

같은 종류의 여러개 데이터를 처리하기 쉽게 나열한 것

정수형, 문자형 등 같은 자료형에 배열 이름을 지정하여 선언

배열의 길이와 동일한 개수의 초기화 리스트 존재

가장 일반적인 초기화 방식

초기화 리스트에 나열된 값은 배열에 순서대로 저장

```c
#include <stdio.h>

int main(void)
{
	int i;
	int arr1[5] = { 1, 2, 3, 4 ,5 };
	int len0fArr1 = sizeof(arr1) / sizeof(int);

	//int lenOfArr1 = size(arr1)/sizeof(arr[0]);
	printf("arr1[5] = {1, 2, 3, 4, 5}의 ~~ \\n");
	for (i = 0; i < len0fArr1; i++) {
		printf("%d번째 요소 ~~ : %d\\n", i + 1, arr1[i]);
	}
	printf("\\n");
	return 0;
}
```

배열의 길이를 나타내는 값이 빠져있는 경우

컴파일러가 초기화 리스트의 수를 참조하여 배열의 길이를 결정

초기화 리스트의 수가 배열의 길이보다 작은 경우

초기화 리스트의 수가 배열의 길이보다 작으면, 나머지 부분은 0으로 초기화

## 문자열 배열
#c #문자열

```c
#include <stdio.h>

int main(void)
{
	char string1[6] = { 'H','e','l','l','o','\0' };
	char string2[6] = "world";
	printf("%s\\n", string1);
	printf("%s\\n", string2);
	printf("%s %s\\n", string1, string2);
	return 0;
}
```

배열로 문자열을 저장하고 처리하기 위해서는 마지막에 문자열의 마지막임을 나타내는 문자 \0을 반드시 넣어 주어야함

널 문자 : C언어에서 문자열의 끝을 나타내는 기호로 사용

5행에서 큰따옴표를 이용하여 문자배열을 초기화하며, 마지막에 자동으로 널 문자 추가

6행에서 printf()함수는 %s형태로 출력

널 문자가 나올 떄까지 문자를 계속 출력

널 문자는 \0,0,null 등으로 표현

6~8행에서 문자열 배열 string, string에 저장되어 있는 문자열을 서식지정자 %s를 이용하여 출력

문자 1개를 나타내는 서식지정자 %c를 이용하여 출력하는 방법도 가능

```c
for(i=0; stirng1[i] != NULL; i++)
	printf("%c", string1[i]);
```

널 문자의 존재와 표현에 대한 이해

```c
int main(void)
{
	printf("AA0BB0CC");
	printf("|");
	printf("AA\\0BB\\0CC");
	printf("|");
	printf("\\0AA");
	printf("|");
}
```

## 배열의 주소
#c #배열주소

scanf 함수로 문자열을 입력 받기 위해 필요한 두 가지 사항

문자열을 저장할 char형 배열

문자열의 입력을 의미하는 서식문자 %s

문자열을 입력 받기 위한 scanf 함수 호출문 구성

배열의 이름은 그자체가 배열의 시작 주소를 의미하는 상수

따라서 배열의 이름을 인자로 전달하면 &연산자를 붙이지 않는다.

scanf 함수는 데이터를 공백으로 구분하므로, 공백을 포함하는 문자열의 입력은 불가능!

## 2차원 배열
#c #2차원 #배열


```c
1차원 -> int arr[17];
2차원 -> int arr[4][17]
3차원 -> int arr[3][4][17]
for (i=0; i<3; i++){
	for(j=0; j<4; j++){
		for(k=0; k<17; k++){
		printf("%d학년 %d반 %d번호", i,j,k);
		}
	}
}
```

- 배열의 메모리 공간 할당
```c
int main(void){
	int arr1[4];
	int arr2[4];
	int arr3[5];
	int arr[3][4];
}
```
```c
int main(void){
	int arr[3][4];
	printf("배열의 시작주소: %d \n", arr);
	printf("1행의 시작주소: %d \n", arr[0]);
	printf("2행의 시작주소: %d \n", arr[1]);
	printf("3행의 시작주소: %d \n", arr[2]);
}
```

### **배열을 포인터로 표현하기**
```c

```

## 2차원 배열 각 행의 위치 정보
### 실행결과를 통해 확인 가능한 사실
- 2차원 배열도 메모리 공간에서는 1차원의 구조를 가짐
- arr\[0], arr\[1], arr\[2]는 배열 각 행의 시작 주소를 의미하므로 값이 16씩 차이가 난다.

###
- arr이 2차원 배열일 때, arr과 arr\[0]이 의미하는 주소 값 동일
- arr은 배열 전체를 의미하고, arr\[0]은 2차원 배열의 첫 번째 행을 의미 함
- 이는 sizeof 연산의 결과로 표현됨
```c
int main(void){
	int arr[3][4];
	printf("sizeof(arr): %d \n", sizeof(arr)); //48
	printf("sizeof(arr[0]): %d \n", sizeof(arr[0])); //16
	printf("sizeof(arr[1]): %d \n", sizeof(arr[1])); //16
	printf("sizeof(arr[2]): %d \n", sizeof(arr[2])); //16
	return 0;
}
```
## 2차원 배열의 초기화
#c #2차원 #배열 #초기화
### 초기화 리스트의 수가 배열의 길이보다 작은 경우
-  중괄호를 하나만 사용하면 순서대로 값이 채워짐
-  1행이 먼저 채워지고, 그 다음에 2행이 채워짐
-  배열 요소의 개수보다 초기화 리스트의 개수가 적다면 나머지 부분은 0으로 채워짐
### 배열의 길이 정보가 빠져있는 경우(1차원 배열)
-  컴파일러가 초기화 리스트의 수를 참조하여 배열의 길이를 결정
### 배열의 세로 길이 정보가 빠져있는 경우
-  컴파일러가 초기화 리스트의 수를 참조하여 배열의 길이를 결정

>[!bug] int i5 = {1, 2, 3, 4, 5}는 되지 않는다
### 2차원 배열에 값 넣기
```c
int arr[2][3];
	arr[2] = 52;
arr[0][0] = 0;
arr[0][1] = 1;
...
arr[1][2] = 5;
printf("%d\n", arr[0][0])
printf("%d\n", arr[0][1])
...
printf("%d\n", arr[1][2])
```
### → 반복문을 사용하여 각각 값을 넣고, 또 출력도 해보자
```c
#include <stdio.h>

int main(void){
	int arr[2][3];
	int k = 0;
	for(int i = 0; i < 2; i++){
		for(int j = 0; j<3; j++){
		arr[i][j] = k;
		k++;
		printf("arr[%d][%d] : %d\n", i, j, arr[i][j]);
		}
	}
}
```
- 학년, 반, 번호를 출력하는 예제
```c
#include <stdio.h>

int main(void) {
	for (int i = 0; i < 3; i++) {
		for (int j = 0; j < 4; j++) {
			for (int k = 0; k < 17; k++) {
				printf("%d학년 %d반 %d번호\n", i+1, j+1, k+1);
			}
		}
	}
}
```
- 5명의 성적을 입력 받고 성적의 총점과 평균을 출력하는 예제
```c
#include <stdio.h>

int main(void) {
	int sungjuk[6][4];
	int k, l;
	for (int i = 0; i < 5; i++){
		for(int j = 0; j < 4; j++){
		scanf("%d"&l);
		sunguk[i][j] = l;
		}
	}
}
	for (int i = 0; i < 5; i++){
		for(int j = 0; j < 4; j++){
			printf("%d", sunguk[i][j]);
		}
	}
}
```

### 2차원 배열에 (반복문) 사용하기
```c
#include <stdio.h>
int main(void){
	int arr[3][3], amount = 0;
	for(int i=0; i < 3; i++){
		for(int j=0; i < 3; j++){
			amount = arr[i][j];
		}
	}
	printf("%d", amount);
}

```
**도서관 좌석 상황 관리 프로그램 만들기**
-  도서관의 자리는 가로 5칸 세로 5칸으로 총 25칸이 존재
- 할당해 줄 좌석의 가로, 세로 정보를 입력 받아, 해당 위치를 할당된 위치로 표시
- 입력된 숫자 정보가 가리키는 좌석이 이미 할당된 좌석일 경우, 할당이 불가능함을 알리는 메시지를출력
- 가로나 세로 정보에 0 이하의 값이 입력될 때 까지 프로그램은 계속해서 실행
```c
#include <stdio.h>
int main(void) {
	int col, row, seat[5][5] = { 0, };
	while (1) {
		printf("할당할 좌석의 세로, 가로 위치 입력: ");
		scanf("%d %d", &col, &row);
		if (col == 0 || row == 0){
				printf("사용해 주셔서 감사합니다.\n");
				break;
		}
		if (seat[col-1][row-1] == 0) {
			printf("할당이 완료되었습니다.\n");
			seat[col-1][row-1]++;
		}
		else if (seat[col-1][row-1] != 0) {
			printf("이미 할당된 자리입니다.\n");
			seat[col-1][row-1]++;
		}
	}
	return 0;
}
```
n\*n 배열 구조를 출력하는 예제
```c
#include <stdio.h>
int main() {
	int size, ol=0, li=0;
	scanf("%d", &size);
	int arr[size][size];
	for (int i = 1; i <= size; i++) {
        ol = 0;
        ol = size-li;
		for (int j = 1; j <= size; j++) {
			arr[size][size] = size*j;
            printf("%d ", ol);
            ol += size;
		}
        li ++;
        printf("\n");
	}
}
```
달팽이 구조를 출력하는 예제
```c
#include <stdio.h>

int main() {
    int n = 3, m = 4; // 배열의 크기 n x m
    int arr[3][4] = {0}; // 3x4 배열 초기화
    int value = 1; // 채울 숫자 시작 값

    // 모든 대각선을 처리
    for (int line = 0; line <= n + m - 2; line++) {
        // 시작 위치 결정
        int start_col = line < m ? line : m - 1;
        int start_row = line - start_col;

        // 대각선을 따라 값을 채워 나감
        while (start_row < n && start_col >= 0) {
            arr[start_row][start_col] = value++;
            start_row++;
            start_col--;
        }
    }

    // 결과 출력
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < m; j++) {
            printf("%d ", arr[i][j]);
        }
        printf("\n");
    }

    return 0;
}

```
## 인덱스 다루기
`blist`에 값에 `alist`값을 대입시키는 예제
```c
#include <stidio.h>
int main() {
	int alist[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
	int blist[10] = { 0, };
	for (int i = 9; i >= 0; i--) {
		blist[i] = alist[i];
		printf("blist[%d]: %d\n", i + 1, blist[i]);
	}
}
```
`blist`에 값에 `alist`값을 거꾸로 대입 시키는 예제
```c
#include <stdio.h>
int main() {
	int alist[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
	int blist[10] = { 0, };
	for (int i = 10; i > 0; i--) {
		blist[10-i] = alist[i-1];
		printf("blist[%d]: %d\n",10-i, blist[10-i]);
	}
}
```
`alist`의 값을 왼쪽으로 한칸 옮겨서 `blist`에 대입하는 예제
```c
#include <stdio.h>

int main() {
	int alist[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
	int blist[10];
	for (int i = 0; i < 10; i++) {
		blist[i] = alist[(i + 1) % 10];

	}
	for (int i = 0; i < 10; i++) {
		printf("%d ", blist[i]);
	}
	return 0;
}
```
`alist`의 값을 오른쪽으로 한칸 옮겨서 `blist`에 대입하는 예제
```c
#include <stdio.h>

int main() {
	int alist[10] = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
	int blist[10];
	for (int i = 0; i < 10; i++) {
		blist[i] = alist[(i + 9) % 10];

	}
	for (int i = 0; i < 10; i++) {
		printf("%d ", blist[i]);
	}
	return 0;
}
```

# 포인터

- 변수나 상수의 주소 값을 저장한 변수
- 주소 값 하나는 1 바이트 크기의 메모리 공간을 표현
- 하나의 주소 값은 1바이트 단위로 할당이 된다
- 주소 값을 표현하는데 필요한 바이트 수는?
	- 표현하고 싶은 주소 값의 범위에 따라 달라짐
	- 주소 값의 바이트 수가 클수록 넓은 범위의 주소 값 표현 가능
- 만약 주소 값을 16비트로 표현한다면?
	- 2의 16 제곱이므로 사용할 수 있는 주소 값의 범위가 넓어짐
>[!warning] 컴퓨터 사양 따라 달라지는 것에 유의

>[!bug] 잘 모르면 실행시키지 말 것! 컴퓨터가 깡통이 될 수도 있음


## 포인터의 개념
```c
#include <stdio.h>

int main()
{
	int *p;
	int a;
	scanf("%d", &a);
	p = &a;
	printf("%d\n", *p) //a가 나온다.
}
```
- 변수
	- 메모리 상의 저장 공간 -> 그 위치를 알면 사용 할 수 있음
- 위치\==주소
- 주소를 사용하기 위한 조건
	- 주소를 구하는 주소 연산자 &
	- 주소를 담는 포인터 *
	- 간접 참조 연산자 \*pi = 10
###  **주소 연산자 &**
- 변수 앞에 붙여 사용하며 할당된 메모리의 시작 주소값을 구한다
- int a; → 주소 : &a
### **포인터 \***
-  시작 주소값을 저장하는 변수이며 가르키는 자료형을 표시하여 선언
		`char *pc int *pi double *pd`
- 간접 참조 연산자
	- `*pi = 10;`
## 포인터 변수
![[C pointer]]
- 주소 값을 얻기 위해 사용되는 &
	-  & 연산자가 단항 연산자로 사용되면 아무런 동작도 하지 않
- 포인터(pointer)
	- 변수나 상수의 주소 값
- 포인터 변수
	- 주소 값의 저장을 위한 변수
```c
int main(void){
	int num1=3;
	char num2='A';
	double num3=3.15;
	int * ptr1=&num1;
	char * ptr2=&num2;
	double * ptr3=&num3;
	
	printf("num1의 저장위치: %#x \n", ptr1);
	printf("num2의 저장위치: %#x \n", ptr2);
	printf("num3의 저장위치: %#x \n\n", ptr3);
	
	printf("포인터 변수 ptr1의 크기: %d \n", sizeof(ptr1));
	printf("포인터 변수 ptr2의 크기: %d \n", sizeof(ptr2));
	printf("포인터 변수 ptr3의 크기: %d \n", sizeof(ptr3));
 //모두 크기가 4바이트 64비트 환경에서는 8바이트
}
```
## 포인터 형(type)과 * 연산자
- 포인터 형과 특성은?
	- 데이터에 데이터 형이 존재하듯, 포인터에도 포인터 형 존재
	- 데이터 형이 데이터의 특성을 나타내듯 포인터 형도 포인터의 특성을 나타냄
	- 포인터 형은 가리키는 대상의 특성을 나타 냄
```c
int *    : int형 포인터
char *   : char형 포인터
double * : double형 포인터
```
![[C pointer2]]
- 포인터 변수도 변수이기 때문에 값의 변경이 허용
```c
int main(void){
	int num1=10;
	int num2=20;

	int * p1;
	int * p2;
	int * temp;

	p1=&num1;
	p2=&num2;

	printf("p1 참조 값: %d\n", *p1); //10
	printf("p2 참조 값: %d\n\n", *p2); //20
	temp=p1;
	p1=p2;
	p2=temp;
	printf("p1 참조 값: %d\n", *p1); //20
	printf("p2 참조 값: %d\n\n", *p2); //10
	return 0;
}
```
- 주소로 값 변경 가능
- 포인터와 함게 사용이 되는 * 연산자(간접 참조 연산자)
```c
int main(void){
	int num = 10;
	int * ptr;

	ptr=&num;
	printf("포인터 ptr이 가리키는 변수 값: %d \n", *ptr);

	*ptr=20;
	printf("포인터 ptr이 가리키는 변수 값: %d \n", *ptr);
	printf("num에 저장된 값: %d \n\n", num);

	(*ptr)++;
	printf("포인터 ptr이 가리키는 변수 값: %d \n", *ptr);
	printf("num에 저장된 값: %d \n\n", num);
	return 0;
	/// ptr에 저장된 주소 값의 메모리 공간<num>을 참조하라
}
```
###  **대입 연산자**
`a=10; b=a; *pa=10; b = *pa`
### **피 연산자**
`a+20; *pa +20;`
### **출력**
`printf("%d",a); printf("%d",*pa)`
### **입력**
`scanf("%d", &a); scanf("%d", pa);`

### 

- 포인터는 변수이므로 값을 다른 주소로 바꿀 수 있음
	`int a , b; int *p = &a; p=&b;`
- 포인터의 크기는 컴파일러에 따라 다를 수 있음 (sizeof로 확인)
	`int *p; printf("주소크기: %d", sizeof(p));`
- 포인터는 가르키는 자료형이 일치할 때만 대입이 가능
	`int *p; double \*pd`
	`pd = p; (X)`

- 주소와 포인터의 차이
	- 주소는 변수에 할당된 메모리 저장 공간 시작 주소 값 자체
	 → 변수의 주소는 변경하거나 수정 할 수 없다.
	- 포인터는 그 값을 저장하는 또 다른 메모리 공간
	 → 다른 주소를 대입하여 그 값을 바꿀 수 있다
	 → 연산도 가능하다.

## 널(NLL) 포인터와 포인터의 형 변환

-  포인터가 잘못 사용되는 경우

>[!bug]-  실행시키면 컴퓨터가 터질 수도 있다.


```c
int main(void){
	int * p1;
	double *p2;

	printf("쓰레기 값1: %#x \n", p1); //쓰레기 값 확인하기
	printf("쓰레기 값2: %#x \n\n", p2); 
	//쓰레기값 초기화! 어디를 참조할지 모른다.
	
	printf("어떤 정수가 찍힐까? %d \n", *p1); //잘못된 연산
	printf("어떤 정수가 찍힐까? %d \n\n",  *p2);
	//의도하지 않은 영역의 데이터 읽어 들임
	
	*p1=25; //위험한 연산
	*p2=3.15;
	//큰 문제 발생 가능한 상황!

	printf("저장된 정수%d \n", *p1);
	printf("저장된 실수%f \n\n", *p2);
	return 0;
}
```
- 널 포인터
	- 널 포인터는 '아무 곳도 가리키고 있지 않다' 라는 상징적인 의미를 지님
	- 널 포인터는 NULL로 표현이 되며, 이는 상수 0이다
	- 안전성 위해서 포인터 변수는 NULL로 초기화 시킨다.
```c
int main(void){
	int * ptr=0; // int * ptr = NULL

	*ptr = 100;
	printf("%d", *ptr);

	return 0;
}
```
```c
int main(void){
	int num = 10;
	char * p = &num; //자동 형 변환 발생
	....
}
```
```c
int main(void){
	int num=10;
	char * p=(char *)&num; 
	//의도적이라면 명시적으로 형 변환하여 의도적임을 표현하자!
	....
}
```
## 포인터가 필요한 이유
- 임베디드 프로그래밍 할 때 메모리에 직접 접근하는 경우
- 동적 할당한 메모리 사용하는 경우
- 함수의 매개변수로 값을 전달 하는 것이 아닌 주소 공간을 전달하는 이유는 인수로 전달된 변수의 값을 함수 내에서 변경할 수 있기 때문에

## 문자열과 포인터
![[C pointer3|1000]]
- 포인터는 주소 값이 없을까?
	- 포인터도 변수이니 당연히 주소 값을 얻어낼 수 있음
```c
int main(void){
	int num1=3;
	double num2=3.15;
	
	int * ptr1=&num1;
	double * ptr2=&num2;
	
	printf("ptr1의 저장 값: %#x \n", ptr1);
	printf("ptr1의 주소 값: %#x \n\n", &ptr1); //& 연산자를 이용하여 포인터 변수의 주소값 출력
	
	printf("ptr2의 저장 값: %#x \n", ptr2);
	printf("ptr2의 주소 값: %#x \n\n", &ptr2); //& 연산자를 이용하여 포인터 변수의 주소값 출력 
	return 0;
}
```
## 포인터의 포인터
```c
int main(void){
	int num1=3;
	double num2=3.15;
	
	int * ptr1=&num1;
	double * ptr2=&num2;
	
	int ** dptr1=&ptr1;
	int ** dptr2=&ptr2;
	
	printf("ptr1의 저장 값: %#x \n", ptr1);
	printf("ptr1의 주소 값: %#x \n\n", dptr1);
	
	printf("ptr2의 저장 값: %#x \n", ptr2);
	printf("ptr의 주소 값: %#ㅌ \n\n", dptr2);
	return 0;
}
```
- dptr1과 dptr2의 주소값을 출력하는 프로그램 예제
```c
int main(void){
	int num1=3;
	double num2=3.15;
	
	int * ptr1=&num1;
	double * ptr2=&num2;
	
	int ** dptr1=&ptr1;
	int ** dptr2=&ptr2;
	
	printf("ptr1의 저장 값: %#x \n", ptr1);
	printf("ptr1의 주소 값: %#x \n\n", &dptr1);
	
	printf("ptr2의 저장 값: %#x \n", ptr2);
	printf("ptr의 주소 값: %#x \n\n", &dptr2);
	return 0;
}
```
```c
int main(void){
	int num1=3;
	int num2=30;
	int* ptr=&num1;
	int** dptr=&ptr;
	printf("ptr이 가리키는 변수 값: %d \n", num1);
	printf("ptr이 가리키는 변수 값: %d \n", *ptr);
	printf("ptr이 가리키는 변수 값: %d \n\n", **dptr);
	
	*dptr = &num2;
	printf("ptr이 가리키는 변수 값: %d \n", num2);
	printf("ptr이 가리키는 변수 값: %d \n", *ptr);
	printf("ptr이 가리키는 변수 값: %d \n\n", **dptr);
	
	**dptr+=3000;
	printf("ptr이 가리키는 변수 값: %d \n", num2);
	printf("ptr이 가리키는 변수 값: %d \n", *ptr);
	printf("ptr이 가리키는 변수 값: %d \n", **dptr);
}
```
- 이중 포인터든 그냥 포인터든 둘 다 사용 가능하다.

- 결과값 출력 예측
```c
#include <stdio.h>
int main(){
	int num=10;
	int *ptr=&num;
	int **dptr=&ptr;
	*ptr=100;
	printf("%d\n",num); //100
	**dptr=200;
	printf("%d", num) //200
}
```
## 배열과 포인터, 포인터 연산
-  포인터 연산이란?
	-  포인터를 피연산자로 하는 연산 전부를 의미
-  포인터 관려 연산자의 종류
	- 메모리 참조 연산:E * 연산자
	- 주소 값 반환 연산: & 연산자
	- 포인터 덧셈 연산: +,++
	- 포인터 뺄셈  연산: -, --
```c
int main(void){ //실행시키지 마세요
	int num1=10;
	double num2=7.12345;
	int * ptr1=&num1; //ptr1은 100으로 가정
	double * ptr2=&num2; //ptr2는 200으로 가정
	printf("ptr1: %d \n", ptr1); //100
	printf("ptr2: $d \n\n", ptr2); //200

	ptr1++, ptr2++;
	printf("ptr1: %d \n", ptr1); //104
	printf("ptr2: %d \n\n", ptr2); //108

	ptr1--, ptr2--;
	printf("ptr1: %d \n", ptr1); //100
	printf("ptr2: %d \n\n", ptr2); //100

	printf("ptr1: %d \n", ptr1-3); //88
	printf("ptr2: %d \n\n", ptr2-3) //76
	return 0;	
}
```
```c
#include <stdio.h>
int main(void){
	int arr[]={1, 2, 3, 4, 5};

	int * p=&arr[2];

	printf("현 위치: %d \n\n", *p);

	printf("한 칸 앞: %d \n", *(p+1));
	printf("두 칸 앞: %d \n\n", *(p+2));
	
	printf("한 칸 뒤: %d \n", *(p-1));
	printf("두 칸 뒤: %d \n", *(p-2));
	return 0;
}
```
```c
#include <stdio.h>
int main(){
	char *str ="He Is My Best Friend!"
	if()
}
```
- 배열의 이름을 이용한 포인터 연산
```c
#include <stduo.h>
int main(void){
	int arr[3]={100, 200, 300};
	printf("arr[0]는 %d, *arr는 %d \n", arr[0], *arr);
	return 0;
}
```

- TYPE형 1차원 배열의 이름은 TYPE형 포인터
	-  int 형 1차원 배열의 이름은 int형 포인터
	- double형 1차원 배열의 이름은 double형 포인터
	- char형 1차원 배열의 이름은 char포인터
```c
int main(void) {
	int arr[5] = { 1, 2, 3, 4, 5 };
	int i;

	for (i = 0; i < 5; i++)
		printf("%d", arr[i]);

	printf("\n");

	for (i = 0; i < 5; i++)
		printf("%d", *(arr + i));

	printf("\n");
		return 0;

}
```
```c
int main(void){
	int arr[5]={1, 2, 3, 4, 5};
	int * pArr = arr;
	int i;

	for(i=0; i<5; i++)
		printf("%d", pArr[i]);

	printf("\n");

	for(i=0; i<5; i++)
		printf("%d ", *([Arr+i]));

	printf("\n");
	return 0;
}
```

- arr\[i]와 \*(arr+i)는 동일한 문장
	- 배열의 관점에서건 포인터의 관점에서건 arr\[i]와 \*(arr+i)는 같은 결과를 보임.
	- arr\[i]는 배열의 이름을 이용할 때 주로 사용
	- \*(arr)는 포인터를 이용할 때 주로 사용한다
- 포인터에 배열명을 저장할 수 있다
```c
#include <stdio.h>
int main(void){
	int ary[3], i;
	int *pa = ary;
	*pa = 10;
	*(pa+1)=20;
	pa[2]=pa[0]+pa[1];
	for(i=0; i<sizeof(ary)/sizeof(int); i++)
		printf("%5d", pa[i])
}
```
- 만일, 할당 영역을 벗어난 경우
	실행이 되지 않을 수 있다.
-  포인터로 배열을 만들 수 있을까?
```c
int main(void){
	int n1, n2, n3;
	int * arrPtr[3] = {&n1, &n2, &n3}

	int i;
	for(i=0; i<3; i++){
		printf("숫자 입력: ")
		scanf("%d", arrPtr[i])
	}

	printf("입력된 숫자의 총 합은 %d입니다.\n",n1 + n2 + n3)
}
```
## 2차원 배열과 포인터
int arr\[4]\[2];
![[C pointer vaeyul]]

![[Pointer 2chawon kgi|400]]

# 함수
## 함수의 작성과 사용
- 1~2까지의 합, 1~5까지의 합, 1~100까지의 합을 출력하는 예제
```c
#include <stdio.h>

int main(void){
	int temp = 0;
	for(int i = 0; i < 2; i++)
		temp += i;
	printf("%d", temp);
	temp = 0;
	for(int i = 0; i < 5; i++)
		temp += i;
	printf("%d", temp);
	temp = 0;
	for(int i = 0; i < 100; i++)
		temp += i;
	printf("%d", temp)
	temp = 0;
}
```
- 함수의 필요성
	- 중복 작업을 없애고 간략하고 프로그램 작성의 난이도를 낮춘다.
	- 여러사람이 분할해서 작업 할 수 있다.
	- 자주 사용되는 코드는 한 번만 작성해서 필요할 때 호출해서 쓴다.
	- 오류가 검증된 함수는 재검사를 할 필요가 없다.
	- 모든 프로그램을 바꿀 필요없이 쉽게 바꿀 수 있다.
- 함수란?
	- 함수<sup>funtion</sup>을 통해 특정 용도의 코드를 한 곳에 모아 놓은 것
	- 마치 자동차의 부품처럼 사용되어 갈아 끼거나 바꿀 수도 있다
	→ 독립적인 기능을 가지는 프로그램의 구성 요소

```c
int main(void){
	int a[10] = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9};
	int tmp;
	// 다음의 값 바꾸기 a[0] ↔ a[3], a[1] ↔ a[5], a[2] ↔ a[4], a[7] ↔ a[9]
	tmp = a[3];
	a[3] = a[0];
	a[0] = tmp;
	printf("a[0]: %d a[3]: %d", a[0], a[3]);
	
	tmp = a[5];
	a[5] = a[1];
	a[1] = tmp;
	printf("a[1]: %d a[5]: %d", a[1], a[5]);
	
	tmp = a[4];
	a[4] = a[2];
	a[2] = tmp;
	printf("a[2]: %d a[4]: %d", a[2], a[4]);

	tmp = a[9];
	a[9] = a[7];
	a[7] = tmp;
	printf("a[7]: %d a[9]: %d", a[7], a[9]);

	return 0;
}
```
- 함수의 구성 요소
	- 함수의 이름
	- 함수의 입력
	- 함수의 출력
	- 함수의 몸

```c
#include <stdio.h>
int Increment(int n){
	n++;
	return n;
}

int main(void){
	int num = 2;
	num = Increment(num);
	printf("num: %d \n", num);
	
	num = Increment(num);
	printf("num: %d \n", num);
	
	num = Increment(num);
	printf("num: %d \n", num);
	return 0;
}
```
![[c funtion]]

![[c funtion 1]]

## 함수를 구성하는 요소들
- 함수는 변수와 같이 사용하기 전에 먼저 선언되어야 한다.
```c
///int add(int x, int y) 먼저 선언해 줘야 한다

int main(){
	int a=5, a=3, res;
	result= add(a, b);   → ERROR :컴파일러는 add가 뭔지 모른다
	printf("%d", result);
}
int add(int x, int y){
	result = x + y;
	return result;
}
```
- 한번에 함수를 선언해도 가능
```c

int add(int x, int y){
	result = x + y;
	return result;
}

int main(){
	int a=5, a=3, res;
	result= add(a, b);
	printf("%d", result);
}
```
- 매개변수의 이름을 같이 사용하는 경우
```c
int add(int a, int b){
	int result = a + b;
	return result;
}
int main(){ //main함수의 a와 add함수의 a는 다른 변수이다
	int a = 5, b = 3, result;//매개변수값이 복사되는 방식
	result = add(a, b);//add함수의 값이 바뀌어도 main함수의 값에는 영향이 없다.
	printf("%d", result);
}
```
## 변수의 범위
### 지역 변수
![[c funtion 3]]
### 전역 변수
![[c funtion 4]]
### 함의 영역
![[C funtion 5]]
### 함수의 형태  
- void를 이용한 함수의 정의  
	- void는 "존재하지 않음"을 의미  
	- 반환형을 사용하지 않음 
  
- 매개변수의 개수  
	- 출력은 많아야 하나지만, 입력은 둘 이상 될 수 있따.  
	- 콤마 연산자를 이용해서 둘 이상의 매개변수 선언

- 정의된 함수 내에서 다른 함수를 호출 할 수 있다.int 
```c
int Quotient(int n1, int n2){
	return n1 / n2;
}
int Remainder(int n1, int n2){
	return n1 % n2;
}
void IntDivide(int n1, int n2){
	printf("%d / %d의 몫: %d \n", n1, n2, Quotient(n1, n2));
	printf("%d / %d의 나머지: %d \n", n1, n2, Remainder(n1, n2));
}
int main(void){
	printf("5 나누기 2의 결과***** \n");
	IntDivide(5, 2);
	printf("\n"); //한 줄 건너 뛰기

	printf("12 나누기 5의 결과 ***** \n");
	IntDivide(12, 5);
	printf("\n");
	return 0;
}
```
### 함수의 호출
-  함수가 호출되면 호출된 함수의 실행을 위해 이동
-  전달인자는 매개변수를 초기화
-  매개변수는 선언된 함수 내에서만 접근 가능
-  반환 값은 함수가 호출된 위치로 전달
-  정의된 함수는 반복 호출이 가능하다
-  함수가 호출될 때마다 매개변수는 초기화 된다

- ### Call-By-Value vs. Call-By-Reference
- 포인터를 이용하면 함수 내에서 외부에 있는 변수에 직접 접근이 가능
- Call-By-Value
	- 변수에 저장된 값을 전달하는 형태의 함수 호출
	- 별도의 변수를 선언해서 전달되는 값을 저장하는 형태
- Call-By-Reference -> 매개변수를 포인터로 사용
	- 주소 값을 전달하는 형태의 함수호출
	- 주소 값이 전달되므로 함수 내에서 주소 값을 기반으로 한 변수의 접근 가능
```c
#include <stdio.h>
void CallByVal(int num){

	num++;

}
void CallByRef(int * ptr){

	(*ptr)++;

}

int main(void){

	int val=10;
	
	CallByVal(val);
	
	printf("CallByVal: %d \n", val);
	
	CallByRef(&val);
	
	printf("CallByRef: %d \n", val);
	
	return 0;

}
```

- 1부터 n까지의 합을 구하는 예제
```c
int sum(int);

int main(){
	int n;
	scanf("%d", &n);

	printf("누계 합은 : %d", sum(n));
}

int sum(int n){
	if (n < 1) return 0;
	else
		return sum(n-1) + n;
}
```

# 구조체<sup>structure</sup>

```c
#include <math.h>
#define POINT_NUMBER 5

double CalDist(double x1, double y1, double s2, double y2);
double CalLineLen(double xpos[], double ypos[]);

int main(void){
	double lineLen=0;
	double xPosArr[POINT_NUMBER];
	double yPosArr[POINT_NUMBER];

	int i;
	for(i=0; i<POINT_NUMBER; i++){
		printf("점 %d의 좌표 입력", i+1);
		scanf("%lf %lf", &xPosArr[i], &yPosArr[i]);
	}

	lineLen=CalLineLen(xPosArr, yPosArr);
	printf("라인의 길이: %g \n", lineLen);
	return 0;
}
```

- 예제에서 표현하고 있는 점의 좌표 정보가 지니는 특징
![[c struture]]
- 데이터들의 일반적인 특징
	- 소프트웨어 개발 과정에서 표현하는 데이터들은 그룹을 형성한다
## 구조체의 정의
![[c structure 2]]

```c
struct point
{
	double xPos;
	double yPos;
};
```
> 정의가 이뤄지고 난 다음부터 point는 변수의 선언에 사용되는 자료형의 이름으로 인식됨.
> 즉, point라는 이름은 ==프로그래머가 정의한 자료형==


<table style="border: 2px solid">
<tr>
<th></th>
<th style="color:red">double</th>
<th style="color:red">point</th>
</tr>
<tr>
<th>제공 방식</th>
<th>기본적으로 제공</th>
<th>프로그래머의 정의에 의해 제공</th>
</tr>
<tr>
<th>변수 선언</th>
<th>double num;<br>double num1, num2;</th>
<th>struct point pnt;<br>struct point p1, p2</th>
</tr>
<tr>
<th>
접근 방식
<th>num=20</th>
<th>pnt.xPos=20<br>
pnt.yPos=20</th>
</tr>
</table>
- 기본 자료형 double과 구조체 자료형 point와 비교

- 구조체
	- 자료를 체계적으로 관리하기 위한 구조체를 문법 제공
	- 구조체눈 struct키워드로 사용 (data struct에서 유래)
- 구조체의 선언
	- struct 구조체명 {변수, 변수}
```c
struct /*예약어*/ student /*구조체 이름*/
{
	int num;
	double grade; //구조체 멤버
};
```
```c
struct person{
	char name[20];
	int age;
	char address[100];
};
```
- 구조체의 사용
	- 변수 선언: struct 구조체명 + 변수 명
	- <span style="color:red; font-size: ">struct person s1;</span>
- 멤버 변수의 사용
```c
s1 . num = 2;
```
```c
struct point{
	double xPos;
	double yPos;
};
int main(void){
	double num;
	struct point pnt; //구조체 변수 선언

	num = 1.2;
	pnt.xPos=2.2; //변수 수pnt는 두개의 변수 xPos와 yPos로 이루어져 있기 때문에 xPos로                    접근할지 yPos로 접근할지 명시해야 함
	pnt.yPod=3.4;

	printf("num: %g \n", num);
	printf("pnt.xPos: %g \n", pnt.xPos);
	printf("pnt.yPos: %g \n", pnt.yPos);

	printf("num의 크기: %d바이트 \n", sizeof(num));
	printf("pnt의 크기: %d바이트 \n", sizeof(pnt));
	return 0;
}
```
- 구조체와 구조체 변수를 동시에 선언 할 수 도 있다
```c
struct person{
	double xPos;
	double yPos;
}pnt;
```
- `struct 변수명` 방식말고 구조체 변수 선언 방법
```c
struct point{
	double xPos;
	double yPos;
};

typedef struct point POINT;

int main(void){
	POINT pnt;
}
```
- 이렇게 쓸 경우 POINT를 ==구조체 별칭==이라 부름

- 익명 구조체 사용하기
```c
tyoedef struct{
	char name[20];
	int age;
	char addresss[100];
	} Person;
```
## 구조체 변수의 활용
- 함수의 인자로 전달 및 반환 가능
- 대입연산자의 피연산자로 사용 가능
- 구조체 변수를 이용한 사칙연산은 불가능
	- 구조체 멤버에는 문자열의 저장이 가능한 char형 배열이 올 수 도 있으므로 사칙연산에 의미를 부여하기 어렵다.
```c
struct _point{
	double xPos;
	double yPos;
};
typedef struct _point point;
point IncrePos(point pnt){
	pnt.xPos++;
	pnt.yPos++;
	return pnt;
}
int main(void){
	point p1, p2, p3;
	p1.xPos=0.5;
	p1.yPos=1.5;

	p2=p1;
	p3=IncrePos(p2);
}
```
```c
struct _person{
	char name[30];
	char ID[15];
	unsigned int age;
}
typedef struct _person person;

void ShowPersonData(person prsn){
	printf("이름: %s \n", prsn.name);
	printf("주민등록번호: %s \n", prsn.ID);
	printf("나이: %u \n", prsn.age);
}

int main(void){
	person jongsoo;
	person copyman;

	strcpy(jongsoo.name, "한종수"); //char형 배열을 초기화 하기 위한 strcpy함수 사용
	strcpy(jongsoo.ID, "900218-1012589");

	copyman=jongsoo; //구조체 변수 jongsoo에 저장된 값을 동일한 자료형 변수인 copyman에 대입연산을 사용해 복사
	ShowPersonData(copyman);
	return 0;
}
```

## 구조체 포인터
```c
typedef struct {
	char name[20];
	int age;
	char address[100];
	
} Person;

Person *p1; //메모리를 할당해 줘야한다
*p1 = (Person*)malloc(sizeof(Person));
```
```c
void printStruct(struct address *lp);

int main(void){
	struct address list[5]={
		{"홍길동", 23, "111-2222", "서울시 중구"},
		{"이순신", 56, "232-2222", "대구시"},
		{"장보고", 32, "451-2222", "대전시"},
		{"유관순", 74, "851-2222", "광주시"},
		{"안중근", 12, "889-2222", "부산시"}
	};

	printfStruct(list);

		return 0;
}
```
```c
void printStruct(struct address *lp) {
    int i;
    for (i = 0; i < 5; i++) {
        printf("%15s %5d %15s %20s\n",
               (lp + i)->name, (lp + i)->age, (lp + i)->tel, (lp + i)->addr);
    }
}

// OR

void printStruct(struct address *lp) {
    int i;
    for (i = 0; i < 5; i++) {
        printf("%15s %5d %15s %20s\n",
               lp[i].name, lp[i].age, lp[i].tel, lp[i].addr);
    }
}

```

- 구조체 배열
	- 구조체도 필요에 따라 배열의 형태로 선언 가능
	- 선언방식이 기본 자료형의 배열 선언방식과 동일하다

```c
#define ARRY_LEN 3
#define NAME_LEN 30
#define PID_LEN 15

typedef struct _person
{
	char name[NAME_LEN];
	char ID[PID_LEN];
	unsigned int age;
} person;

void ShowPersonData(person * ptr);

int main(void){
	int i;
	person.personArr[ARRY_LEN]={
		{"한종수", "900218-102589", 20},
		{"이성은", "910218-102589", 19},
		{"윤지민", "930218-102589", 17}
	};

	for(i=0; i<ARRY_LEN; i++)
		ShowPersonData(&personArr[i]);
	return 0;
}
```
```c
void ShowPersonData(person * ptr){
	printf("이름: %s \n", (*ptr).name);
	printf("주민등록번호: %s \n", (*ptr).ID);
	printf("나이: %u \n\n", ptr->age);
}
```

<h3>배열 표현</h3> `lp[i].name`

<h3>함수 표현</h3>
- 구조체를 함수로 전달하는 경우 구조체의 복사본이 함수로 전달되게 된다

- 구조체 포인터 사용하기
	1. call by Value 로 값 넘기는 방법
	2. call by Reference 로 값 넘기는 방
```c
#define PI 3.14
typedef struct _point{
	double xPos;
	double yPos;
} point;

typedef struct _circle{
	point center;
	double rad;
} circle;

void ShowCircleInfo(const circle * ptr){
	printf("원의 중심: [%g, %g] \n", 
				(ptr->center, xPos, (ptr->center), yPos));
	printf("원의넓이: %g \n",
				(ptr->rad)*(ptr->rad)*PI);
}
int main(void){
	circle cl={
		[]
	}
}
```