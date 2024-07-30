
# 키워드



<details>

1. **abstract**: 클래스나 멤버가 추상적임을 나타냅니다. 추상 클래스는 인스턴스를 생성할 수 없으며, 서브 클래스에서 구현해야 합니다.
   ```scala
   abstract class Animal {
     def sound: String
   }
   ```

2. **case**: 케이스 클래스를 정의할 때 사용됩니다. 케이스 클래스는 불변이며, 패턴 매칭에 사용됩니다.
   ```scala
   case class Person(name: String, age: Int)
   ```

3. **catch**: 예외를 처리할 때 사용됩니다.
   ```scala
   try {
     // Some code that might throw an exception
   } catch {
     case e: Exception => println(e.getMessage)
   }
   ```

4. **class**: 새로운 클래스를 정의할 때 사용됩니다.
   ```scala
   class Person(val name: String, val age: Int)
   ```

5. **def**: 메서드를 정의할 때 사용됩니다.
   ```scala
   def greet(name: String): String = s"Hello, $name"
   ```

6. **do**: do-while 루프를 시작할 때 사용됩니다.
   ```scala
   do {
     // Loop body
   } while (condition)
   ```

7. **else**: if-else 문에서 사용됩니다.
   ```scala
   if (condition) {
     // If body
   } else {
     // Else body
   }
   ```

8. **extends**: 상속을 나타낼 때 사용됩니다.
   ```scala
   class Student(name: String, age: Int) extends Person(name, age)
   ```

9. **false**: 불리언 값 false를 나타냅니다.
   ```scala
   val isStudent = false
   ```

10. **final**: 클래스나 멤버가 더 이상 확장 또는 오버라이드될 수 없음을 나타냅니다.
    ```scala
    final class Car
    ```

11. **finally**: try 블록의 끝에서 항상 실행되는 코드를 정의합니다.
    ```scala
    try {
      // Some code
    } finally {
      // Cleanup code
    }
    ```

12. **for**: 반복문을 정의합니다.
    ```scala
    for (i <- 1 to 10) {
      println(i)
    }
    ```

13. **if**: 조건문을 정의합니다.
    ```scala
    if (condition) {
      // If body
    }
    ```

14. **implicit**: 암시적 변환 또는 값을 정의할 때 사용됩니다.
    ```scala
    implicit val defaultValue: Int = 10
    ```

15. **import**: 다른 패키지나 객체를 가져올 때 사용됩니다.
    ```scala
    import scala.collection.mutable
    ```

16. **lazy**: 지연 평가 변수를 정의합니다. 변수가 처음 사용될 때 초기화됩니다.
    ```scala
    lazy val resource = expensiveComputation()
    ```

17. **match**: 패턴 매칭을 수행할 때 사용됩니다.
    ```scala
    x match {
      case 1 => "one"
      case 2 => "two"
      case _ => "other"
    }
    ```

18. **new**: 새로운 인스턴스를 생성할 때 사용됩니다.
    ```scala
    val p = new Person("Alice", 25)
    ```

19. **null**: 널 값을 나타냅니다.
    ```scala
    val noValue: String = null
    ```

20. **object**: 싱글턴 객체를 정의합니다.
    ```scala
    object Singleton {
      def greet(): String = "Hello"
    }
    ```

21. **override**: 슈퍼 클래스의 멤버를 재정의할 때 사용됩니다.
    ```scala
    override def toString: String = "Overridden toString"
    ```

22. **package**: 패키지를 정의합니다.
    ```scala
    package com.example
    ```

23. **private**: 접근 제한자를 정의합니다. 같은 클래스에서만 접근 가능합니다.
    ```scala
    private val secret = "hidden"
    ```

24. **protected**: 접근 제한자를 정의합니다. 같은 클래스와 서브 클래스에서 접근 가능합니다.
    ```scala
    protected def calculate(): Int = 42
    ```

25. **return**: 값을 반환할 때 사용됩니다.
    ```scala
    def add(a: Int, b: Int): Int = return a + b
    ```

26. **sealed**: 상속 계층을 제한합니다. sealed 클래스는 같은 파일에서만 상속될 수 있습니다.
    ```scala
    sealed trait Shape
    ```

27. **super**: 슈퍼 클래스의 멤버를 참조할 때 사용됩니다.
    ```scala
    super.toString
    ```

28. **this**: 현재 객체를 참조합니다.
    ```scala
    this.name
    ```

29. **throw**: 예외를 던질 때 사용됩니다.
    ```scala
    throw new Exception("Error")
    ```

30. **trait**: 트레이트를 정의합니다. 트레이트는 다중 상속을 지원합니다.
    ```scala
    trait Flyable {
      def fly(): Unit
    }
    ```

31. **true**: 불리언 값 true를 나타냅니다.
    ```scala
    val isScalaFun = true
    ```

32. **try**: 예외가 발생할 수 있는 코드를 정의합니다.
    ```scala
    try {
      // Some code
    }
    ```

33. **type**: 새로운 타입을 정의합니다.
    ```scala
    type StringList = List[String]
    ```

34. **val**: 불변 변수를 정의합니다.
    ```scala
    val name = "Alice"
    ```

35. **var**: 가변 변수를 정의합니다.
    ```scala
    var age = 25
    ```

36. **while**: while 루프를 정의합니다.
    ```scala
    while (condition) {
      // Loop body
    }
    ```

37. **with**: 트레이트를 믹스인할 때 사용됩니다.
    ```scala
    class Bird extends Animal with Flyable
    ```

38. **yield**: for 루프에서 값을 생성할 때 사용됩니다.
    ```scala
    val squares = for (i <- 1 to 5) yield i * i
    ```

</details>