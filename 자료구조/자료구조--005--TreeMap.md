# TreeMap
- Map 인터페이스를 구현하고 있는 클래스이다.
- 키(Key)와 값(Value)로 구성되어 있다.
***
### TreeMap 특징
- **한 개**의 Key는 **한 개**의 Value만 가질 수 있다.
- 주로 검색하는 일을 할 때 사용하는 자료구조이다. (**검색 속도가 매우 빠르다.**)
- 저장 속도가 느리다.
- Key는 중복이 안되지만, Value는 중복이 가능하다.
- Key 값을 기준으로 데이터가 정렬된다.
***
### HashMap과의 차이
#### 1. HashMap
- HashMap은 데이터 전체를 다시 사용할 때 순서가 뒤바뀐다.
- HashMap은 다른 Map에 비해 빠른 탐색 시간을 갖는다.
- HashMap은 해시 함수를 사용하기 때문에 O(1)의 시간 복잡도를 갖는다.
#### 2. TreeMap
- TreeMap은 HashMap과 달리 Key - Value 쌍을 RedBlack Tree로 저장하여 관리한다.
- TreeMap에 있는 Key 값을 기준으로 정렬된다.
- Comparator, Comparable 인터페이스를 구현하면 사용자가 정렬 기준을 정할 수 있다.
- TreeMap은 O(logn)의 시간 복잡도를 갖는다.
