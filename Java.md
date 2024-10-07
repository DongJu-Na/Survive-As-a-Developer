<details>
  <summary>Java 8 의 특징들은 무엇이 있나요?</summary>
  <br/>
  <pre>
자바 8은 프로그래밍 언어 자바에 많은 혁신을 가져왔습니다. 람다 표현식, 스트림 API, 옵셔널 클래스의 도입은 자바 개발자들이 보다 효율적이고 안정적인 코드를 작성할 수 있게 해주었습니다.

이러한 기능들은 자바의 사용성과 생산성을 크게 향상시켰으며, 함수형 프로그래밍의 도입으로 자바의 패러다임을 확장시켰습니다. 자바 8의 특징들은 현대 소프트웨어 개발에 있어서 중요한 역할을 하고 있습니다.

따라서 자바 개발자라면 자바 8의 주요 특징들을 잘 이해하고 활용할 수 있어야 합니다. 이를 통해 더 나은 소프트웨어 개발을 위한 기반을 마련할 수 있습니다.
  </pre>
  <p><b>람다 표현식(Lambda Expressions)</b><br/><br/>
  <code>(parameters) -> expression</code>
  <ul>
   <li>간결한 코드를 작성하게 해줍니다.</li>
   <li>익명 함수로서 함수형 프로그래밍 스타일을 도입합니다.</li>
  </ul>
  </p>
  <p><b>스트림 API(Stream API)</b><br/><br/>
  <code>List&lt;String&gt; filteredList = list.stream().filter(s -> s.startsWith("A")).collect(Collectors.toList());
  </code>
  <ul>
   <li>데이터 컬렉션을 처리하는데 있어 선언적이고 함수형 스타일을 사용하게 합니다.</li>
   <li>병렬 처리와 중간, 최종 연산을 지원합니다.</li>
  </ul>
  </p>
  <p><b>디폴트 메소드(Default Methods)</b><br/><br/>
  <code>
  interface MyInterface { <br/>
 &emsp;&emsp;&emsp;default void newMethod() {<br/>
&emsp;&emsp;&emsp;&emsp;&emsp;// default implementation <br/>
&emsp;&emsp;&emsp;}<br/>
  }
  </code>
  <ul>
   <li>인터페이스에 구현 코드를 포함할 수 있게 하여, 기존 코드를 깨뜨리지 않고 인터페이스를 확장할 수 있습니다.</li>
  </ul>
  </p>
  <p><b>옵셔널 클래스(Optional Class)</b><br/><br/>
  <code>
Optional&lt;String&gt; optional = Optional.ofNullable(value);
  </code>
  <ul>
   <li>NullPointerException을 피하기 위해 도입된 컨테이너 클래스입니다.</li>
  </ul>
  </p>
    <p><b>New Date and Time API</b><br/><br/>
  <code>
LocalDate date = LocalDate.now();
  </code>
  <ul>
   <li>java.time 패키지를 통해 더 나은 날짜와 시간 처리 기능을 제공합니다.</li>
  </ul>
  </p>
</details>

<br/>

<details>
  <summary>오버로딩(Overloading)과 오버라이딩(Overriding) 대해 설명해보실 수 있나요?</summary>
  </br>
  <pre>
<b>메소드 오버로딩(overloading)</b>이란 <br/>
같은 이름의 메소드를 중복하여 정의하는 것을 의미합니다.
자바에서는 원래 한 클래스 내에 같은 이름의 메소드를 둘 이상 가질 수 없습니다.
하지만 매개변수의 개수나 타입을 다르게 하면, 하나의 이름으로 메소드를 작성할 수 있습니다.

즉, 메소드 오버로딩은 서로 다른 시그니처를 갖는 여러 메소드를 같은 이름으로 정의하는 것이라고 할 수 있습니다.
이러한 메소드 오버로딩을 사용함으로써 메소드에 사용되는 이름을 절약할 수 있습니다.
또한, 메소드를 호출할 때 전달해야 할 매개변수의 타입이나 개수에 대해 크게 신경을 쓰지 않고 호출할 수 있게 됩니다.

메소드 오버로딩은 객체 지향 프로그래밍의 특징 중 하나인 다형성(polymorphism)을 구현하는 방법 중 하나입니다.

메소드 오버로딩의 대표적인 예로는 println() 메소드를 들 수 있습니다.
println() 메소드는 전달받는 매개변수의 타입에 따라 다음과 같이 다양한 원형 중에서 적절한 원형을 호출하게 됩니다.

<hr/>
<code>
1. println()
2. println(boolean x)
3. println(char x)
4. println(char[] x)
5. println(double x)
6. println(float x)
7. println(int x)
8. println(long x)
9. println(Object x)
10. println(String x)
</code>
<hr/>
<b>메소드 오버로딩의 조건</b><br/>
자바에서 메소드 오버로딩이 성립하기 위해서는 다음과 같은 조건을 만족해야 합니다.

1. 메소드의 이름이 같아야 합니다.
2. 메소드의 시그니처, 즉 매개변수의 개수 또는 타입이 달라야 합니다.

메소드 오버로딩은 반환 타입과는 관계가 없습니다.

만약 메소드의 시그니처는 같은데 반환 타입만이 다른 경우에는 오버로딩이 성립하지 않습니다.
</pre>
<br/>  
<br/>
<pre>
<b>메소드 오버라이딩(method overriding)</b>
앞서 배운 오버로딩(overloading)이란 서로 다른 시그니처를 갖는 여러 메소드를 하나의 이름으로 정의하는 것이었습니다.

오버라이딩(overriding)이란 상속 관계에 있는 부모 클래스에서 이미 정의된 메소드를 자식 클래스에서 같은 시그니쳐를 갖는 메소드로 다시 정의하는 것이라고 할 수 있습니다.

자바에서 자식 클래스는 부모 클래스의 private 멤버를 제외한 모든 메소드를 상속받습니다.

이렇게 상속받은 메소드는 그대로 사용해도 되고, 필요한 동작을 위해 재정의하여 사용할 수도 있습니다.

즉, 메소드 오버라이딩이란 상속받은 부모 클래스의 메소드를 재정의하여 사용하는 것을 의미합니다.

<br/>
<hr/>
<b>오버라이딩의 조건</b>
자바에서 메소드를 오버라이딩하기 위한 조건은 다음과 같습니다.


1. 오버라이딩이란 메소드의 동작만을 재정의하는 것이므로, 메소드의 선언부는 기존 메소드와 완전히 같아야 합니다.

    하지만 메소드의 반환 타입은 부모 클래스의 반환 타입으로 타입 변환할 수 있는 타입이라면 변경할 수 있습니다.

2. 부모 클래스의 메소드보다 접근 제어자를 더 좁은 범위로 변경할 수 없습니다

3. 부모 클래스의 메소드보다 더 큰 범위의 예외를 선언할 수 없습니다.
</pre>

<ol>
 <li>오버로딩(overloading)은 새로운 메소드를 정의하는 것</li>
 <li>오버라이딩(overriding)은 상속받은 기존의 메소드를 재정의하는 것</li>
</ol>
</details>

<br/>

<details>
  <summary>GC에 대해서 설명해 볼 수 있나요?</summary>
  </br>
<pre>
GC 는 JVM에서 메모리를 관리 해주는 모듈 입니다.
Heap 메모리를 재활용하기 위해서 더이상 참조 되지 않는 객체들을 메모리에서 제거하는 모듈 입니다. 개발자가 직접 메모리를 정리 하지 않아도 되어서 개발 속도가 향상 되는 장점이 있지만 Mark and  Sweep 이라는 과정에서 참조되지 않는 객체를 찾는 과정이 있는데 이 때 스레드가 중단 되어서 성능이 떨어지는 단점이 있습니다.
</pre>
</details>

<br/>

<details>
  <summary>객체지향 프로그래밍에 대해서 설명해 볼 수 있나요?</summary>
  </br>
<pre>
실제 세계의 사물들을 객체로 모델링하여 개발을 진행하는 프로그래밍 기법
가장 대표적인 언어로 Java가 있다.
캡슐화, 상속, 다형성 등과 같은 기법을 이용할 수 있다. 다형성은 동일한 키보드의 키가 다른 역할을 하는 것처럼 하나의 메소드나 클래스가 다양한 방법으로 동작하는 것을 의미한다.
절치지향 언어보다 실행속도가 느리다.
<br/>
4가지 특징

추상화 , 캡슐화 , 상속성 , 다형성

<br/><br/>

절차지향 프로그래밍

물이 위에서 아래로 흐르는 것처럼 순차적인 처리를 중요시하는 프로그래밍 기법이다.
가장 대표적인 언어로 C언어가 있다.
컴퓨터의 처리구조와 유사해 실행속도가 빠르다.
코드의 순서가 바뀌면 동일한 결과를 보장하기 어렵다.

</pre>
</details>

<br/>

<details>
  <summary>접근제어자에 대해서 설명해볼 수 있나요?</summary>
  </br>
  <table>
  <thead>
    <tr>
      <th>접근 제어자</th>
      <th>접근 가능 범위</th>
      <th>설명</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>public</td>
      <td>모든 클래스</td>
      <td>클래스, 메서드, 또는 필드가 모든 다른 클래스에서 접근 가능.</td>
    </tr>
    <tr>
      <td>protected</td>
      <td>동일 패키지 및 하위 클래스</td>
      <td>동일 패키지 내의 클래스와 이 클래스를 상속받은 하위 클래스에서 접근 가능.</td>
    </tr>
    <tr>
      <td>default</td>
      <td>동일 패키지</td>
      <td>접근 제어자를 명시하지 않으면 기본 접근 수준은 default (package-private)로 설정되며, 동일 패키지 내의 클래스에서만 접근 가능.</td>
    </tr>
    <tr>
      <td>private</td>
      <td>동일 클래스</td>
      <td>클래스 내부에서만 접근 가능.</td>
    </tr>
  </tbody>
</table>
<br/>
<pre>
공개범위는 public  >  protected  >  default(생략)  >  private 순
</pre>
</details>

<br/>

<details>
  <summary>제네릭타입에 대해서 설명해볼 수 있나요?</summary>
  </br>
<pre>
<b>제네릭 타입(Generic Types)</b>은 클래스나 메서드를 정의할 때, 사용할 데이터 타입을 미리 지정하는 것이 아니라, 인스턴스를 생성하거나 메서드를 호출할 때 구체적인 타입을 지정할 수 있도록 하는 기능입니다. 제네릭은 코드의 재사용성을 높이고, 컴파일 시 타입 안전성을 제공합니다.
<br/>
<b>제네릭 타입의 장점</b>
1.타입 안전성: 컴파일 시 타입 검사를 통해 런타임 오류를 줄일 수 있습니다.
2.재사용성: 하나의 클래스나 메서드가 다양한 타입을 지원할 수 있습니다.
3.가독성: 코드의 가독성과 유지보수성을 높입니다.
</pre>
<br/>
<table>
  <thead>
    <tr>
      <th>제네릭 타입</th>
      <th>설명</th>
      <th>예시</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>&lt;T&gt;</td>
      <td>일반적인 타입 파라미터</td>
      <td>public class Box&lt;T&gt; { private T item; }</td>
    </tr>
    <tr>
      <td>&lt;E&gt;</td>
      <td>컬렉션의 요소 타입</td>
      <td>public class List&lt;E&gt; { void add(E element); }</td>
    </tr>
    <tr>
      <td>&lt;K, V&gt;</td>
      <td>맵의 키와 값 타입</td>
      <td>public class Map&lt;K, V&gt; { V get(K key); }</td>
    </tr>
    <tr>
      <td>&lt;N&gt;</td>
      <td>숫자 타입</td>
      <td>public class Numeric&lt;N extends Number&gt; { N number; }</td>
    </tr>
    <tr>
      <td>&lt;T, U, V&gt;</td>
      <td>다중 타입 파라미터</td>
      <td>public class Triple&lt;T, U, V&gt; { T first; U second; V third; }</td>
    </tr>
  </tbody>
</table>
</details>

<br/>

<details>
  <summary>함수형 인터페이스에 대해서 설명해볼 수 있나요?</summary>
  </br>
<pre>
함수형 인터페이스(Functional Interface)는 하나의 추상 메서드만을 가지는 인터페이스를 의미합니다. 이러한 인터페이스는 Java 8에서 람다 표현식과 함께 도입되었으며, 람다 표현식의 대상 타입으로 사용할 수 있습니다. 함수형 인터페이스는 함수형 프로그래밍 스타일을 Java에 도입하기 위한 중요한 요소입니다.
</pre>

<table>
  <thead>
    <tr>
      <th>함수형 인터페이스</th>
      <th>설명</th>
      <th>추상 메서드</th>
      <th>예시</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Predicate&lt;T&gt;</td>
      <td>매개변수 T를 받아 boolean을 반환</td>
      <td>boolean test(T t)</td>
      <td>
        <pre>
Predicate&lt;Integer&gt; isPositive = x -> x &gt; 0;
System.out.println(isPositive.test(5)); // 출력: true
        </pre>
      </td>
    </tr>
    <tr>
      <td>Function&lt;T, R&gt;</td>
      <td>매개변수 T를 받아 R을 반환</td>
      <td>R apply(T t)</td>
      <td>
        <pre>
Function&lt;String, Integer&gt; lengthFunction = String::length;
System.out.println(lengthFunction.apply("Hello")); // 출력: 5
        </pre>
      </td>
    </tr>
    <tr>
      <td>Supplier&lt;T&gt;</td>
      <td>매개변수를 받지 않고 T를 반환</td>
      <td>T get()</td>
      <td>
        <pre>
Supplier&lt;String&gt; stringSupplier = () -> "Hello";
System.out.println(stringSupplier.get()); // 출력: Hello
        </pre>
      </td>
    </tr>
    <tr>
      <td>Consumer&lt;T&gt;</td>
      <td>매개변수 T를 받아서 처리하고 반환값 없음</td>
      <td>void accept(T t)</td>
      <td>
        <pre>
Consumer&lt;String&gt; printConsumer = System.out::println;
printConsumer.accept("Hello"); // 출력: Hello
        </pre>
      </td>
    </tr>
    <tr>
      <td>UnaryOperator&lt;T&gt;</td>
      <td>입력값과 출력값의 타입이 동일한 함수</td>
      <td>T apply(T t)</td>
      <td>
        <pre>
UnaryOperator&lt;Integer&gt; square = x -> x * x;
System.out.println(square.apply(5)); // 출력: 25
        </pre>
      </td>
    </tr>
    <tr>
      <td>BinaryOperator&lt;T&gt;</td>
      <td>두 개의 동일한 타입 매개변수를 받아 동일한 타입을 반환</td>
      <td>T apply(T t1, T t2)</td>
      <td>
        <pre>
BinaryOperator&lt;Integer&gt; sum = (a, b) -> a + b;
System.out.println(sum.apply(3, 5)); // 출력: 8
        </pre>
      </td>
    </tr>
  </tbody>
</table>

</details>

<br/>

<details>
  <summary>Checked Exception, Unchecked Exception에 대해서 설명해볼 수 있나요?</summary>
  </br>
<pre>
<b>Checked Exception</b>
체크드 익셉션은 컴파일러가 예외 처리를 강제하는 예외입니다. 즉, 체크드 예외가 발생할 가능성이 있는 코드에서는 반드시 예외 처리를 해야 합니다. 이러한 예외는 주로 프로그램 외부의 문제(예: 파일 입출력, 네트워크 통신 등)로 인해 발생합니다.

특징:

컴파일 시점에 예외 처리 여부를 검사.
Exception 클래스를 상속하지만, RuntimeException을 상속하지 않음.
반드시 try-catch 블록이나 throws 키워드를 사용해 예외를 처리해야 함.

<b>Unchecked Exception</b>
언체크드 익셉션은 컴파일러가 예외 처리를 강제하지 않는 예외입니다. 주로 프로그래머의 실수(예: 잘못된 타입 캐스팅, 배열 인덱스 초과 등)로 인해 발생합니다.

특징:

런타임 시점에 예외가 발생.
RuntimeException 클래스를 상속.
예외 처리를 강제하지 않지만, 필요에 따라 예외 처리를 할 수 있음.
</pre>

<table>
  <thead>
    <tr>
      <th>구분</th>
      <th>체크드 예외 (Checked Exception)</th>
      <th>언체크드 예외 (Unchecked Exception)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>상속 관계</td>
      <td>Exception 클래스를 상속하나, RuntimeException을 상속하지 않음</td>
      <td>RuntimeException 클래스를 상속</td>
    </tr>
    <tr>
      <td>컴파일러 강제 여부</td>
      <td>컴파일 시 예외 처리를 강제</td>
      <td>컴파일 시 예외 처리를 강제하지 않음</td>
    </tr>
    <tr>
      <td>주로 발생하는 상황</td>
      <td>프로그램 외부의 문제 (파일 입출력, 네트워크 통신 등)</td>
      <td>프로그래머의 실수 (잘못된 타입 캐스팅, 배열 인덱스 초과 등)</td>
    </tr>
    <tr>
      <td>예외 처리 방법</td>
      <td>try-catch 블록이나 throws 키워드를 사용하여 예외를 처리해야 함</td>
      <td>예외 처리가 선택 사항이지만 필요에 따라 처리 가능</td>
    </tr>
    <tr>
      <td>예시</td>
      <td>
        <pre>
        
import java.io.FileReader;
import java.io.IOException;

public class CheckedExceptionExample {
    public static void main(String[] args) {
        try {
            FileReader reader = new FileReader("somefile.txt");
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
        </pre>
      </td>
      <td>
        <pre>
public class UncheckedExceptionExample {
    public static void main(String[] args) {
        int[] numbers = {1, 2, 3};
        System.out.println(numbers[5]);  // ArrayIndexOutOfBoundsException 발생
    }
}
        </pre>
      </td>
    </tr>
  </tbody>
</table>

</details>

<br/>

<details>
  <summary>자바 리플렉션에 대해서 설명해볼 수 있나요?</summary>
  </br>
<pre>
자바 리플렉션(Java Reflection)은 런타임에 클래스, 메서드, 필드 등을 동적으로 검사하고 조작할 수 있는 기능입니다. 리플렉션을 사용하면 프로그램 실행 중에 객체의 메타데이터(클래스, 메서드, 필드 등)를 분석하고, 이를 통해 동적으로 객체를 생성하거나 메서드를 호출할 수 있습니다.

주요 개념:
1. 클래스 정보 얻기:
   - `Class<?>` 객체를 통해 클래스의 메타데이터를 얻을 수 있습니다.
   - 예: 
      ```java 
      Class<?> clazz = Class.forName("com.example.MyClass"); 
      ```

2. 생성자 접근:
   - 클래스의 생성자를 통해 새로운 인스턴스를 동적으로 생성할 수 있습니다.
   - 예: 
     ```java
     Constructor<?> constructor = clazz.getConstructor(String.class);
     Object instance = constructor.newInstance("parameter");
     ```

3. 메서드 접근:
   - 클래스의 메서드 정보를 얻고, 동적으로 메서드를 호출할 수 있습니다.
   - 예:
     ```java
     Method method = clazz.getMethod("myMethod", String.class);
     Object result = method.invoke(instance, "argument");
     ```

4. 필드 접근:
   - 클래스의 필드 정보를 얻고, 필드 값을 읽거나 쓸 수 있습니다.
   - 예:
     ```java
     Field field = clazz.getField("myField");
     field.set(instance, "new value");
     Object value = field.get(instance);
     ```

5. 리플렉션의 장점:
   - 동적 모듈 로딩 및 객체 조작: 컴파일 타임에 알 수 없는 클래스나 메서드를 런타임에 동적으로 로드하고 사용할 수 있습니다.
   - 프레임워크 개발: 리플렉션을 이용하여 의존성 주입, 애너테이션 기반 설정 등 다양한 기능을 구현할 수 있습니다.

6. 리플렉션의 단점:
   - 성능 저하: 리플렉션은 일반적인 메서드 호출보다 느립니다.
   - 보안 문제: 접근 제어를 우회할 수 있으므로, 보안상 문제가 발생할 수 있습니다.
   - 유지보수 어려움: 코드 가독성이 떨어지고, 리플렉션을 과도하게 사용하면 유지보수가 어려워질 수 있습니다.

자바 리플렉션은 강력한 도구이지만, 필요할 때 신중하게 사용하는 것이 좋습니다.

</pre>
</details>


<br/>

<details>
  <summary>Java 자료구조에 대해서 설명해보세요.</summary>
  </br>
<pre>
# Java 자료구조 개요

## 자료구조란?
- **설명**: 자료구조(Data Structure)는 데이터를 효율적으로 저장하고 관리하기 위한 방법을 의미합니다. 다양한 형태의 자료구조를 통해 데이터를 체계적으로 저장하고, 필요할 때 빠르고 효율적으로 접근하거나 수정할 수 있습니다. 자바에서는 여러 기본적인 자료구조를 제공하며, 개발자는 이를 활용하여 최적화된 프로그램을 작성할 수 있습니다.

## 1. 배열 (Array)
- **설명**: 같은 타입의 데이터가 연속적으로 저장되는 자료구조입니다. 배열은 고정된 크기를 가지며 인덱스를 통해 요소에 접근합니다.
- **장점**: 인덱스를 사용한 빠른 접근.
- **단점**: 크기가 고정되어 있어 동적으로 크기를 조절할 수 없음, 삽입 및 삭제가 비효율적.

## 2. 리스트 (List)
- **설명**: 순서가 있는 데이터의 집합입니다. 자바에서 `ArrayList`와 `LinkedList`가 대표적인 리스트 구현체입니다.
    - **ArrayList**: 내부적으로 배열을 사용하여 구현됩니다. 인덱스를 통해 빠르게 접근할 수 있지만, 크기를 동적으로 변경할 수 있습니다.
    - **LinkedList**: 각 요소가 노드로 이루어져 있으며, 노드는 다음 요소에 대한 참조를 가집니다. 삽입과 삭제가 빠르지만 인덱스 접근은 느립니다.

## 3. 스택 (Stack)
- **설명**: 후입선출(LIFO, Last In First Out) 구조를 가지는 자료구조입니다. `push`로 요소를 추가하고, `pop`으로 가장 마지막에 추가된 요소를 제거합니다.
- **사용 사례**: 재귀 호출, 브라우저의 뒤로 가기 기능, 수식의 괄호 검사 등.

## 4. 큐 (Queue)
- **설명**: 선입선출(FIFO, First In First Out) 구조를 가지는 자료구조입니다. `offer`로 요소를 추가하고, `poll`로 가장 먼저 추가된 요소를 제거합니다.
- **변형**:
  - **우선순위 큐 (Priority Queue)**: 각 요소가 우선순위를 가지며, 높은 우선순위를 가진 요소가 먼저 처리됩니다.

## 5. 맵 (Map)
- **설명**: 키-값 쌍으로 데이터를 저장하는 자료구조입니다. `HashMap`, `TreeMap`, `LinkedHashMap` 등이 자바에서 사용됩니다.
  - **HashMap**: 해시 함수를 사용하여 키를 관리하며, 빠른 검색, 삽입, 삭제가 가능합니다.
  - **TreeMap**: 키를 자동으로 정렬하여 저장하며, 이진 검색 트리 기반으로 구현됩니다.
  - **LinkedHashMap**: 삽입 순서를 유지하며 저장합니다.

## 6. 셋 (Set)
- **설명**: 중복되지 않는 요소의 집합입니다. `HashSet`, `TreeSet`, `LinkedHashSet` 등이 있습니다.
  - **HashSet**: 해시 함수를 사용하여 요소를 관리하며, 빠른 검색, 삽입, 삭제가 가능합니다.
  - **TreeSet**: 요소를 자동으로 정렬하여 저장합니다.

## 7. 트리 (Tree)
- **설명**: 계층 구조를 가지는 자료구조입니다. 이진 트리, AVL 트리, 레드블랙 트리 등이 있습니다.


</pre>
</details>

<br/>

<details>
  <summary>자바 컬렉션 프레임워크(Java Collection Framework)에 대해서 설명하고 List , Map , Set 에 대해서 각각 설명해보세요.</summary>
  </br>
<pre>
# Java 컬렉션 프레임워크

## 1. 컬렉션 프레임워크란?
- **설명**: 자바 컬렉션 프레임워크는 자바에서 데이터 구조를 표준화된 방식으로 다루기 위해 제공하는 클래스와 인터페이스의 집합입니다. 이 프레임워크는 데이터를 저장, 검색, 정렬, 조작하는 다양한 자료구조 및 알고리즘을 포함하고 있습니다.
- **장점**:
  - **일관된 API**: 다양한 컬렉션을 다루기 위한 일관된 메서드를 제공합니다.
  - **성능 최적화**: 다양한 상황에 맞는 효율적인 자료구조와 알고리즘을 선택할 수 있습니다.
  - **타입 안정성**: 제네릭스를 사용하여 컴파일 시점에 타입을 체크할 수 있습니다.

## 2. 주요 컬렉션 인터페이스

### 2.1 List
- **설명**: List는 순서가 있는 요소의 집합입니다. 중복된 요소를 허용하며, 인덱스를 통해 각 요소에 접근할 수 있습니다.
- **구현 클래스**:
  - **ArrayList**: 배열 기반으로 구현된 리스트. 빠른 인덱스 접근과 동적 크기 조절이 가능.
  - **LinkedList**: 노드 기반으로 구현된 리스트. 요소의 삽입과 삭제가 빠름.
  - **Vector**: ArrayList와 유사하지만, 동기화를 지원하여 스레드 안전성을 보장.

### 2.2 Set
- **설명**: Set은 중복되지 않는 요소의 집합입니다. 순서가 보장되지 않으며, 각 요소는 고유합니다.
- **구현 클래스**:
  - **HashSet**: 해시 테이블 기반의 집합. 빠른 검색과 삽입이 가능.
  - **LinkedHashSet**: HashSet과 유사하지만, 요소의 삽입 순서를 유지.
  - **TreeSet**: 요소를 정렬된 상태로 저장하는 집합. 이진 검색 트리 기반.

### 2.3 Map
- **설명**: Map은 키-값 쌍으로 데이터를 저장하는 구조입니다. 각 키는 고유하며, 하나의 키에 대해 하나의 값만 매핑됩니다.
- **구현 클래스**:
  - **HashMap**: 해시 테이블 기반의 맵. 빠른 검색과 삽입이 가능.
  - **LinkedHashMap**: HashMap과 유사하지만, 삽입 순서를 유지.
  - **TreeMap**: 키를 자동으로 정렬하여 저장. 이진 검색 트리 기반.
  - **Hashtable**: HashMap과 유사하지만, 동기화를 지원하여 스레드 안전성을 보장.

## 3. List, Set, Map 비교

| 특성       | List                                          | Set                                         | Map                                      |
|------------|-----------------------------------------------|---------------------------------------------|------------------------------------------|
| **순서**   | 유지됨                                         | 유지되지 않음                               | 키에 대해 정의된 순서가 있을 수 있음     |
| **중복**   | 허용됨                                         | 허용되지 않음                               | 키는 중복되지 않으며, 값은 중복 가능     |
| **접근**   | 인덱스를 통한 요소 접근 가능                   | 인덱스를 통한 접근 불가                     | 키를 통한 값 접근 가능                   |
| **대표 구현 클래스** | `ArrayList`, `LinkedList`, `Vector`          | `HashSet`, `LinkedHashSet`, `TreeSet`      | `HashMap`, `LinkedHashMap`, `TreeMap`   |


</pre>
</details>

<br/>

<details>
  <summary>Enum 에 대해서 설명해보세요.</summary>
  </br>
<pre>
 Enum은 "Enumeration"의 약자다. Enumeration은 "열거, 목록, 일람표" 라는 뜻을 가지고 있으며, 보통 한글로는 열거형이라고 부른다. 즉, 열거형(enum)은 요소, 멤버라 불리는 명명된 값의 집합을 이루는 자료형이다
</pre>
</details>
