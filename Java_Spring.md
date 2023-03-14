자바의 특징
객체 지향
확장성과 재사용성

플랫폼 독립성
JVM 이라는 가상 환경 위에서 실행 되기 때문에 OS에 독립적

뛰어난 에코 시스템
뛰어난 라이브러리와 미들 웨어가 많으며 자바 생태계가 잘 형성되어 있음

자바의 3가지 에디션
Java SE : Standard Edition. 가장 표준. PC나 서버에서 동작하는 애플리케이션 용
Java EE : Enterprise Edition. 웹 서비스, 서버 간 통신, 메일 송신 등 서버에 필요한 기능 포함
Java ME : Micro Edition. 임베디드 시스템 용
자바의 2가지 환경
JRE : Java Runtime Environment. 자바 파일(JAR나 클래스 파일)의 실행 환경
JDK : Java Development Kit. 자바 개발 환경. 실행 뿐 아니라 컴파일러 및 디버거 포함
-> 디버깅을 위해 JDK가 필요할 수도 있다.
자바 실행 순서
java 소스 코드 (.java) 작성
컴파일러가 (.java) -> (.class) 클래스 파일로 컴파일
각 OS 용 JVM에서 (.class) 파일을 해석하여 실행
자바 수식자
접근 제한자

abstract
말 그대로 추상적인 클래스 또는 메소드 앞에 붙인다
인스턴스화 할 수 없으며 이를 상속하여 구현해서 사용
abstract 메소드는 abstract 클래스 안에서만 존재 가능

static
해당 클래스가 인스턴스화 되지 않아도 액세스 가능

final
필드 : 필드 값 변경 금지
메소드 : Override 금지
클래스 : 해당 클래스 상속 금지

transient
클래스를 직렬화할 경우 직렬화 대상에서 제외. 불필요한 데이터는 직렬화하지 않도록 한다.

직렬화 : 인스턴스화 된 자바 객체를 바이트 열로 변환

volatile
해당 데이터를 main memory에 저장하겠다는 것 명시
멀티 스레드 환경에서 액세스 되는 필드에 대해 캐싱 금지

synchronized
해당 메서드 또는 블록에 대해서 한번에 하나의 스레드만 접근 가능

명명 규칙
변수는 명사. 메소드는 동사
-> 필드에 isXXX와 같은 이름 짓지 말자!! 이것은 메소드의 이름

자바는 정적 타입 언어
즉, 자료형이 변수 선언 시에 정해짐 -> 컴파일 시 정합성 판단.
동적 타입 언어는 변수 선언 시에는 자료형을 정하지 않음 -> 실행 시 정합성 판단.

기본형 : long, int, char, boolean, ...
참조형 : 인스턴스에 대한 포인터를 저장하는 타입
// 기본형
int i = 1;

// 참조형
String name = new String("hi");
String name = "hi";
래퍼 클래스
자료형에 대한 다양한 기능 제공을 위해 래퍼 클래스 사용

Integer num1 = new Integer(1);
Integer num2 = Integer.valueOf(1);		// 캐시된 객체 반환, -128~127은 캐싱되어 있음

int num = num2.intValue();
래퍼 클래스는 null을 가질 수 있지만 기본형은 null을 가질 수 없다

Integer numInteger = null;		// 가능
int numInt = null;		// 불가능. 무조건 초기값은 0 -> 혼란 초래 할 수 있으니 Integer 쓰자
익명 클래스
익명 클래스는 이름이 없는 클래스
클래스 정의와 인스턴스화를 한번에 진행

//  TaskHandler 라는 인터페이스 구현하고 인스턴스화
TaskHandler taskHandler = new TaskHandler() {
    public boolean handle(Task task) {
    	// 익명 함수 내용 구현,,,
    }
}
equals 와 hashCode
객체의 값이 동일한지 판단하기 위해서 equals 라는 함수를 사용한다. 이 때 equals 함수를 오버 라이드해서 어떤 기준으로 등가성을 처리할 지 정할 수 있다.
이 때 꼭 같이 선언해줘야 하는 함수가 hashCode 이다!! hashCode함수는 객체의 내용을 해시값으로 반환한다. 즉, 같은 값을 가지는 객체일 경우 같은 해시값을 갖는다. 하지만 같은 해시값이라고 해서 꼭 같은 값을 가지는 객체는 아니다!

equals 를 사용할 때 hashCode도 함께 사용해야 하는 이유는 무엇일까?
equals 메소드는 값을 하나씩 검증하기 때문에 계산 시간이 오래 걸린다. 반면에 해시값은 해시값으로 변환하는 과정과 해당 해시값을 비교하는 과정만 거차가 때문에 보다 빠르게 객체의 동일 여부를 판단할 수 있다.
hash 값으로 비교 -> hash 값이 동일할 경우 equals로 보다 더 정밀한 비교
위와 같은 flow는 HashMap, HashSet 에도 똑같이 적용된다.

class Point{
    int x;
    int y;
    
    Point(int x, int y) {
    	this.x = x;
        this.y = y;
    }
    
    @Override
    public boolean equals(Object obj) {
    	if (this == obj)
        	return true;
        if (obj == null)
        	return false;
        if (getClass() != obj.getClass())
        	return false;
        Point other = (Point) obj;
        if (x != other.x)
        	return false;
        if (y != other.y)
        	return false;
    }
    
    @Override
    public int hashCode() {
    	final int prime = 31;
        int result = 1;
        result = prime * result + x;
        result = primt * result + y;
        return result;
    }
    
    // 자바 7부터 hash 메소드 사용 가능
    @Override
    public int hashCode() {
    	return Objects.hash(this.x, this.y);
    }
}
public static final보다 enum을 사용해야 하는 이유?
1. 타입 안전하다.
enum 자체를 넘기기 때문에 타입이 맞지 않는 파라미터를 넘길 일이 없다.

2. public static final을 사용할 경우 상수 클래스에서 상수의 값을 변경해도 이용 클래스 쪽 상수의 값은 변경되지 않을 수 있다.

//  상수 클래스 쪽의 정의
public static final String SELECTED_COLOR = "blue";

// 이용 클래스 쪽의 정의
public String coloe = SELECTED_COLOR;
위의 상황에서 SELECTED_COLOR = "red";로 수정했다.
하지만 수정한 부분은 컴파일이 되지 않고 이용 클래스쪽만 컴파일한다면 red로 변경되지 않고 여전히 blue로 남아있다.

enum은 static final과 달리 이용하는 쪽의 클래스에는 값이 전개되지 않기 때문에 사용 클래스도 다시 컴파일할 필요가 없다.


jpa 영속성의 종류
jpa의 장점
인터페이스와 추상클래스의 차이
동기와 비동기의 차이
동기방식의 api서버와 비동기방식의 api 서버의 차이와 장단점
jpa에서 영속성을 관리하는법
퇴사한 이유
hashcode equals 차이
