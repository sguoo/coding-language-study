# Kotlin이란?

- 코틀린<sup>Kotlin</sup>이란 InteliJ IDEA라는 통합 개발 환경으로 유명한 젯브레인<sup>JetBrains</sup>에서 개발한 언어
- Kotlin/JVM[^1]: 자바 가상 머신에서 동작하는 애플리케이션을 만들 수 있다
- Kotlin/JS: 자바스크립트로 웹 브라우저에서 작동하는 애플리케이션을 만들 수 있다
- Koltlin/Native: LLVM 컴파일러를 이용하여 여러플랫폼을 타깃으로하는 애플리케이션을 만들수 있다
- LLVM컴파일러[^2]를 통해 안드로이드와 iOS에서 작동하는 애플리케이션 작동 가능
- 임베디드, IoT<sup>Internet of Things</sup>등을 타겟으로 한 애플리케이션 개발 가능

[^1]: JVM<sup>Java Virtual Machine, 자바 가상 머신</sup>  OS에 종속받지 않고 CPU가 JAVA를 인식, 실행할 수 있게 하는 가상 컴퓨터
[^2]: LLVM은 멀티플렛폼을 위한 중간 언어인 비트코들를 생성해 arm, x86, PowerPC 등에서 실행 할 수 있는 코드를 만드는 컴파일러용 도구

# 코틀린의 장점
- 자료형 오류를 미리 잡을 수 있는 정적 언어이다
- 널 포인터 예외로 인한 프로그램의 중단 예방 가능
- 간결하고 효율적
- 함수형, 객체지향 프로그래밍 모두 가능
- 세미콜론( ; ) 생략 가능

# 변수와 자료형, 연산자
## 패키지

```kotlin
package com.acaroom //패키지 이름의 예
```
```kotlin
package com.acroom.net.upload // 네트워크 업로드 기능을 가진 코틀린 파일에 적은 패키지 이름
```

### 클래스 추가하기

`com.example.edu`패키지에 Person class 추가하기
```kotlin
package com.example.edu

class Person(val name: String, val age: Int)
```

`default`패키지에 Person class 추가하기
```kotlin
class Person(val name: String, val age: Int)
```

### 클래스 가져오기

`math 클래스` 사용법
```kotlin
import kotlin.math.PI
import kotlin.math.abs //전부 가져오려면 import kotlin.math.* 사용
```

사용자 클래스 가져오기
```kotlin
import com.example.edu.Person
```

## 변수와 자료형

### 변수를 선언하고 자료형 추론하기

- 변수는 val, var라는 키워드를 사용하여 선언 할 수 있다
- val키워드는 최초로 지정한 변수의 값으로 초기화되고 Read-Only 변수가 된다
- var로 변수를 선언하면 초깃값이 있더라도 값을 바꿀 수 있다

#### 변수를 선언 하는 방법
![[Kotlin 1]]

### 자료형 변환
- 코틀린에서는 자료형이 다르면 변환 함수를 사용해야한다
```kotlin
val a: Int = 1 //Int형 변수 a를 선언하고 1을 할당
val b: Double = a //자료형 불일치 오류 발생
val c: Int = 1.1 //자료형 불일치 오류 발생
```

- int형 변수 a에 double형 으로 변환하는 메서드 사용
```kotlin
val b: Double = a.toDouble() //변환 메서드 사용
```
- 자료형이 다른 값을 연산하면 아래와 같이 된다
```kotlin
val result = 1L + 3 //Long형 + Int형 → result는 Long
```