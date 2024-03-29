# OOP 5가지 설계 원칙
### 1. SRP(Single Responsibility Principle) : 단일 책임 원칙
- 클래스는 단 하나의 목적을 가져야 하며, 클래스를 변경하는 이유는 단 하나의 이유여야 한다.

### 2. OCP(Open-Closed Principle) : 개방 폐쇠 원칙
- 클래스는 확장에는 열려있고, 변경에는 닫혀 있어야 한다.

### 3. LSP(Liskov Subsitution Principle) : 리스코프 치환 원칙
- 상위 타입의 객체를 하위 타입으로 바꾸어도 프로그램은 일관되게 동작해야 한다.

### 4. ISP(Interface Segregation Principle) : 인터페이스 분리 원칙
- 클라이언트는 이용하지 않는 메소드에 의존하지 않도록 인터페이스를 분리해야 한다.

### 5. DIP(Dependency Inversion Principle) : 의존 역전 법칙
- 클라이언트는 추상화(인터페이스)에 의존해야 하며, 구체화(구현된 클래스)에 의존해선 안된다.
