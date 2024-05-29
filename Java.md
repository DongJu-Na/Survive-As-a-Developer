<details>
  <summary>Java 8 의 특징들은 무엇이 있나요?</summary>
  </br>
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