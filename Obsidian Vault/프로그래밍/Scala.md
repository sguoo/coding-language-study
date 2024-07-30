
# 키워드


| 키워드      | 설명                                                              | 예시                                                                 |
|-------------|-----------------------------------------------------------------|---------------------------------------------------------------------|
| abstract    | 클래스나 멤버가 추상적임을 나타냅니다.                                   | `abstract class Animal { def sound: String }`                       |
| case        | 케이스 클래스를 정의할 때 사용됩니다.                                   | `case class Person(name: String, age: Int)`                         |
| catch       | 예외를 처리할 때 사용됩니다.                                           | `try { ... } catch { case e: Exception => println(e.getMessage) }`  |
| class       | 새로운 클래스를 정의할 때 사용됩니다.                                    | `class Person(val name: String, val age: Int)`                      |
| def         | 메서드를 정의할 때 사용됩니다.                                          | `def greet(name: String): String = s"Hello, $name"`                 |
| do          | do-while 루프를 시작할 때 사용됩니다.                                 | `do { ... } while (condition)`                                      |
| else        | if-else 문에서 사용됩니다.                                           | `if (condition) { ... } else { ... }`                               |
| extends     | 상속을 나타낼 때 사용됩니다.                                          | `class Student(name: String, age: Int) extends Person(name, age)`   |
| false       | 불리언 값 false를 나타냅니다.                                       | `val isStudent = false`                                             |
| final       | 클래스나 멤버가 더 이상 확장 또는 오버라이드될 수 없음을 나타냅니다.                | `final class Car`                                                   |
| finally     | try 블록의 끝에서 항상 실행되는 코드를 정의합니다.                            | `try { ... } finally { ... }`                                       |
| for         | 반복문을 정의합니다.                                               | `for (i <- 1 to 10) { println(i) }`                                 |
| if          | 조건문을 정의합니다.                                               | `if (condition) { ... }`                                            |
| implicit    | 암시적 변환 또는 값을 정의할 때 사용됩니다.                                 | `implicit val defaultValue: Int = 10`                               |
| import      | 다른 패키지나 객체를 가져올 때 사용됩니다.                                  | `import scala.collection.mutable`                                   |
| lazy        | 지연 평가 변수를 정의합니다.                                         | `lazy val resource = expensiveComputation()`                        |
| match       | 패턴 매칭을 수행할 때 사용됩니다.                                       | `x match { case 1 => "one" case 2 => "two" case _ => "other" }`     |
| new         | 새로운 인스턴스를 생성할 때 사용됩니다.                                   | `val p = new Person("Alice", 25)`                                   |
| null        | 널 값을 나타냅니다.                                                | `val noValue: String = null`                                        |
| object      | 싱글턴 객체를 정의합니다.                                            | `object Singleton { def greet(): String = "Hello" }`                |
| override    | 슈퍼 클래스의 멤버를 재정의할 때 사용됩니다.                                | `override def toString: String = "Overridden toString"`             |
| package     | 패키지를 정의합니다.                                               | `package com.example`                                               |
| private     | 접근 제한자를 정의합니다.                                           | `private val secret = "hidden"`                                     |
| protected   | 접근 제한자를 정의합니다.                                           | `protected def calculate(): Int = 42`                               |
| return      | 값을 반환할 때 사용됩니다.                                           | `def add(a: Int, b: Int): Int = return a + b`                       |
| sealed      | 상속 계층을 제한합니다.                                             | `sealed trait Shape`                                                |
| super       | 슈퍼 클래스의 멤버를 참조할 때 사용됩니다.                                | `super.toString`                                                    |
| this        | 현재 객체를 참조합니다.                                             | `this.name`                                                         |
| throw       | 예외를 던질 때 사용됩니다.                                           | `throw new Exception("Error")`                                      |
| trait       | 트레이트를 정의합니다.                                              | `trait Flyable { def fly(): Unit }`                                 |
| true        | 불리언 값 true를 나타냅니다.                                        | `val isScalaFun = true`                                             |
| try         | 예외가 발생할 수 있는 코드를 정의합니다.                                  | `try { ... }`                                                       |
| type        | 새로운 타입을 정의합니다.                                            | `type StringList = List[String]`                                    |
| val         | 불변 변수를 정의합니다.                                             | `val name = "Alice"`                                                |
| var         | 가변 변수를 정의합니다.                                             | `var age = 25`                                                      |
| while       | while 루프를 정의합니다.                                           | `while (condition) { ... }`                                         |
| with        | 트레이트를 믹스인할 때 사용됩니다.                                      | `class Bird extends Animal with Flyable`                            |
| yield       | for 루프에서 값을 생성할 때 사용됩니다.                                  | `val squares = for (i <- 1 to 5) yield i * i`                       |
