# JPA란?
- JPA(Java Persistence API)는 자바 진영의 ORM 기술 표준이다.
- JPA가 제공하는 API를 사용하면 객체를 DB에 저장하고 관리할 때, 개발자가 직접 SQL을 작성하지 않아도 된다.
- JPA가 개발자 대신 적절한 SQL을 생성해서 DB에 전달하고, 객체를 자동으로 Mapping해준다.
- JPA는 내부적으로 JDBC API를 활용하는데, 개발자가 직접 JDBC API를  활용하면 패러다임 불일치, SQL 의존성 등으로 인해 효율성이 떨어진다.
- 이 때, JPA를 활용한다면 모든 SQL에 대해 개발자 대신 JPA가 자동으로 해결해 준다는 점에서 생산성을 크게 높일 수 있다.

***
### ORM이란?
- ORM(Object-Relational Mapping)은 객체와 관계형 DB를 매핑한다는 뜻이다.
- ORM 프레임워크를 사용하면 객체를 마치 자바 Collection에 저장하듯 저장할 수 있고, 이에 대해 ORM 프레임워크가 적절한 SQL을 생성해서 DB에 객체를 저장해준다.  
***

### Hibernate란?
- 자바 진영의 다양한 ORM 프레임워크 중 가장 많이 사용되는 성숙한 프레임워크이다.
- 이러한 Hibernate 기반으로 만들어진 ORM 기술 표준이 바로 JPA다.
- 즉, JPA라는 ORM 기술 표준을 구현한 것이 Hibernate이므로, JPA를 사용하려면 Hibernate를 사용하면 된다.
***
JPA로 인해 개발자는 관계형 DB를 사용해도 객체지향 애플리케이션 개발에 집중할 수 있다.  
  
출처 : https://velog.io/@jwkim/JPA-JPA%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80
