# 정규화
- 정규화란 데이터의 중복을 최소화하고 데이터의 무결성을 향상하며 데이터를 유연하게 데이터들을 구조화하는 프로세스를 의미한다.
- 데이터베이스를 정규화할 때 정규화된 정도에 따라 정규형으로 표현한다.
- 각 정규형이 되기 위해선 만족시켜야 할 제약조건들이 있으며, 높은 차수의 정규형일 수록 조건이 까다롭다.
***
### 정규화의 목적
- 불필요한 중복 데이터를 제거한다.
- 각종 이상 현상(Anomaly)을 방지하고 테이블의 구성을 논리적이고 직관적이게 한다.
- 이상 현상 : 갱신 이상, 삽입 이상, 삭제 이상
- 데이터베이스 구조 확장 시 재디자인을 최소화한다.
***
### 정규화 과정
- 제 1 정규화 : 테이블의 칼럼이 원자 값(하나의 값)을 갖도록 테이블을 분해하는 것이다.
- 제 2 정규화 : 제 1 정규화에 속하면서, 기본 키가 아닌 모든 속성이 기본 키에 완전 함수 종속된 형태이다.
- 제 3 정규화 : 제 2 정규화에 속하면서, 기본 키를 제외한 모든 속성이 기본 키에 이행적 함수 종속이 되지 않는 형태이다.
- BCNF : 제 3 정규화에 속하면서, 모든 결정자가 후보키 집합에 속한 정규형이다.
