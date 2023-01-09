### List
#### 1. ArrayList
- add : O(1)
- remove : O(n)
- get : O(1)
- contains : O(n)
- iterator.remove : O(n)
- 데이터의 인덱스를 가지고 있어 데이터 검색시 빠르다.
#### 2. LinkedList
- add : O(1)
- remove : O(1)
- get : O(n)
- contains : O(n)
- iterator.remove : O(1)
- 데이터 추가 및 삭제시 빠르다.
***
### Set
#### 1. HashSet
- add : O(1)
- contains : O(1)
- next : O(h/n), h = 테이블 용량
- 중복되지 않는 값을 등록할 때 용이
- Hash를 사용하여 특정 값을 찾을 때 O(1) 시간이 걸린다.
- 순서 없이 저장된다.
- null 허용
#### 2. LinkedHashSet
- add : O(1)
- contains : O(1)
- next : O(1)
- 속도는 HashSet에 비해 느리지만 좋은 성능을 보장한다.
- 등록한 순서대로 정렬한다.
- null 허용
#### 3. TreeSet
- add : O(logn)
- contains : O(logn)
- next : O(logn)
- 객체 기준으로 정렬하므로 상대적으로 느리다.
- null 허용 x
***
### Map
#### 1. HashMap
1. get : O(1)
2. containsKey : O(1)
3. next : O(h/n), h = 테이블 용량
- 순서 없이 저장된다.
- null 허용
#### 2. LinkedHashMap
1. get : O(1)
2. containsKey : O(1)
3. next : O(1)
- 순서대로 저장된다.
- null 허용
#### 3. TreeMap
- get : O(logn)
- containsKey : O(logn)
- next : O(logn)
- 데이터를 추가하면서 자동으로 정렬된다.
- null 허용 x
***
### Queue
#### 1. PriorityQueue
- offer(add) : O(logn)
- get(peek) : O(1)
- poll : O(logn)
- size : O(1)
- null 허용 x
#### 2. ArrayDeque
- offer(add) : O(1)
- get(peek) : O(1)
- poll : O(1)
- size : O(1)
- 앞 뒤로 요소를 추가하거나 제거할 수 있는 자료구조이다.
