<details>
  <summary>스프링의 기초 원리 - DI, IoC 가 왜 사용되었는지?</summary>
  </br>
  <pre>
DI(Dependency Injection)와 IoC(Inversion of Control)는 스프링 프레임워크의 핵심 원리로, 이 두 가지 개념은 <u>더 유연하고 확장 가능한 애플리케이션을 설계하는 데 중요한 역할을 합니다.</u> 이 개념들이 왜 사용되는지 설명하겠습니다.

<br/><br/><br/>

<b>IoC(Inversion of Control)</b>
IoC는 제어의 역전이라는 개념입니다. 전통적인 프로그래밍에서는 객체가 자신의 종속성을 스스로 생성하고 관리합니다. 그러나 IoC를 적용하면 객체의 생성과 관리를 컨테이너나 프레임워크가 대신 담당합니다. 이를 통해 다음과 같은 이점이 있습니다:

1.관심사의 분리: 객체가 자신의 종속성을 직접 관리하지 않기 때문에, 비즈니스 로직과 객체 생성 로직이 분리됩니다.

2.유연한 확장성: 객체 생성 로직이 분리되면, 다양한 설정 파일이나 주입 방법을 통해 쉽게 객체를 교체하거나 확장할 수 있습니다.

3.테스트 용이성: 객체의 종속성을 쉽게 모의(Mock) 객체로 대체할 수 있기 때문에, 단위 테스트 작성이 용이해집니다.

<b>DI(Dependency Injection)</b>
DI는 의존성 주입이라는 개념으로, 객체의 종속성을 외부에서 주입해주는 방식을 말합니다. DI를 통해 객체의 생성과 종속성 주입을 스프링 컨테이너가 관리하게 됩니다. 
이를 통해 다음과 같은 이점이 있습니다.

1.코드의 유연성 증가: 객체가 필요로 하는 종속성을 외부에서 주입받기 때문에, 객체의 의존성을 쉽게 변경하거나 주입할 수 있습니다.

2.결합도 감소: 객체 간의 강한 결합을 약화시켜, 객체가 다른 객체에 의존하지 않고 인터페이스를 통해 상호작용하도록 유도합니다.

3.재사용성 향상: 종속성 주입을 통해 재사용 가능한 컴포넌트를 만들 수 있으며, 설정 파일이나 주입 방법을 변경함으로써 다양한 환경에서 재사용할 수 있습니다.

<b>요약</b>
스프링에서 DI와 IoC를 사용하는 이유는 객체의 생성과 생명주기를 관리하는 책임을 개발자에서 프레임워크로 이전함으로써, 코드의 유연성과 재사용성을 높이고, 결합도를 낮추어 유지보수와 테스트를 용이하게 하기 위함입니다.
  </pre>
</details>

<br/>

<details>
<summary>Spring AOP 의 역할에 대해 설명해보실 수 있나요?</summary>
</br>
<pre>
<b>Spring AOP(Aspect-Oriented Programming)</b>는 스프링 프레임워크의 중요한 기능 중 하나로, 관심사 분리를 통해 모듈화된 코드를 작성할 수 있게 합니다. AOP는 주로 횡단 관심사(cross-cutting concerns)를 분리하여 코드의 가독성과 유지보수성을 향상시키는 데 사용됩니다. Spring AOP의 역할에 대해 설명하겠습니다.

1.횡단 관심사(Cross-Cutting Concerns) 분리 애플리케이션에는 비즈니스 로직 외에도 로깅, 트랜잭션 관리, 보안, 캐싱 등의 기능이 필요합니다. 이러한 기능은 여러 모듈에서 공통적으로 사용되며, 이를 횡단 관심사라고 합니다. AOP를 사용하면 이러한 횡단 관심사를 핵심 비즈니스 로직에서 분리하여 모듈화할 수 있습니다.

2.AOP의 주요 구성 요소 Spring AOP는 다음과 같은 주요 구성 요소로 이루어져 있습니다:

Aspect: 횡단 관심사를 모듈화한 것으로, 여러 어드바이스와 포인트컷을 포함합니다.
Join Point: 어드바이스가 적용될 수 있는 실행 지점으로, 메서드 호출이나 예외 처리 등이 포함됩니다.
Advice: 실제로 횡단 관심사를 구현한 코드로, 특정 시점에 실행됩니다. 어드바이스는 Before, After, After Returning, After Throwing, Around 등의 타입이 있습니다.
Pointcut: 어드바이스가 적용될 Join Point를 정의한 것으로, 특정 메서드나 클래스에 적용할지 결정합니다.
Weaving: 어드바이스를 실제 대상 객체에 적용하는 과정으로, 컴파일 시, 로드 시, 런타임 시에 수행될 수 있습니다.

3.AOP의 이점
관심사의 분리: 핵심 비즈니스 로직과 횡단 관심사를 분리함으로써 코드의 가독성과 유지보수성을 높입니다.
코드 중복 감소: 여러 곳에서 반복되는 횡단 관심사 코드를 하나의 어드바이스로 정의하여 중복을 줄입니다.
유지보수 용이성: 횡단 관심사를 모듈화하면 변경 사항을 한 곳에서 관리할 수 있어 유지보수가 용이합니다.
코드 가독성 향상: 비즈니스 로직에서 부가 기능을 분리함으로써 비즈니스 로직의 가독성이 향상됩니다.

간단한 예시로 메서드 실행 전후에 로깅하는 AOP를 생각해볼 수 있습니다.

<code>
@Aspect
public class LoggingAspect {

    @Before("execution(* com.example.service.*.*(..))")
    public void logBefore(JoinPoint joinPoint) {
        System.out.println("Method " + joinPoint.getSignature().getName() + " is about to start");
    }

    @After("execution(* com.example.service.*.*(..))")
    public void logAfter(JoinPoint joinPoint) {
        System.out.println("Method " + joinPoint.getSignature().getName() + " has finished");
    }
}
</code>
위 예시에서 @Before와 @After 어드바이스는 com.example.service 패키지의 모든 메서드 실행 전후에 로깅을 수행합니다. 이를 통해 핵심 비즈니스 로직에 로깅 코드를 추가할 필요 없이 로깅 기능을 분리할 수 있습니다.

<b>요약</b>
Spring AOP는 <u>횡단 관심사를 핵심 비즈니스 로직에서 분리하여 모듈화함으로써 코드의 가독성과 유지보수성을 향상시키는 역할</u>을 합니다. 이를 통해 공통 기능의 재사용성을 높이고 코드 중복을 줄일 수 있습니다.
</pre>
</details>

<br/>

<details>
  <summary>Spring Interceptor, Filter 의 차이점과 사용용도에 대해 설명해보실 수 있나요?</summary>
  </br>
  <pre>

  </pre>
  <p><b></b><br/><br/>
  <code></code>
  <ul>
   <li></li>
   <li></li>
  </ul>
  </p>
</details>

<br/>

<details>
  <summary>Spring MVC에 대해 설명해보실 수 있나요?</summary>
  </br>
  <pre>

  </pre>
  <p><b></b><br/><br/>
  <code></code>
  <ul>
   <li></li>
   <li></li>
  </ul>
  </p>
</details>