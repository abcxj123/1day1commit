# PriorityQueue
- PriorityQueue는 Queue와 구조가 비슷하다.
- Queue는 FIFO 구조로 먼저 들어온 순서대로 데이터가 나간다.
- PriorityQueue는 데이터의 우선순위를 정하여 우선순위가 높은 순서대로 나간다.
- PriorityQueue는 우선순위 힙으로 구현할 수 있다.
***
### PriorityQueue 특징
- 우선순위 큐는 값을 비교해야 하므로 null을 허용하지 않는다.
- 내부 구조는 이진트리 힙으로 구성되어 있다.
- add(), poll() method가 O(logn) 시간 복잡도를 가진다.
***
### PriorityQueue 사용법
```
// 큐와는 다르게 PriorityQueue로 선언함. (Queue는 LinkedList)
PriorityQueue<Integer> pq1 = new PriorityQueue<>();

// 기본적으로 오름차순으로 우선순위가 결정되지만, 다음과 같이 내림차순으로 지정할 수 있다.
PriorityQueue<Integer> pq2 = new PriorityQueue<>(Collections.reverseOrder());

pq1.add(2);
pq1.add(6);
pq1.add(10);
pq1.add(8);
pq1.add(4);

System.out.println(pq1.poll()); // 2

System.out.println(pq1.poll()); // 4

System.out.println(pq1.peek()); // 6

System.out.println(pq1.isEmpty()); // false

System.out.println(pq1.remove(10)); // true, 원소 '10'이 지워짐.

System.out.println(pq1.size()); // 2
```
- priorityqueue에 2, 6, 10, 8, 4를 넣었을 때 poll() 연산을 하면 가장 낮은 숫자인 2를 꺼내고,
- 한 번 더 연산하면 다음으로 낮은 숫자인 4를 꺼낸다.  
- peek()을 하면 그 뒤에 있던 6을 반환한다.  
- peek()은 실제로 데이터를 꺼내는 연산은 아니기 때문에  
- 다시 poll()을 실행하면 6를 꺼내오게 된다.  
- priorityqueue 안에 6, 8, 10이 아직 남아있으므로, isEmpty()의 결과는 false이다.   
- remove(10) 연산을 하면 priorityqueue에 들어있는 10이라는 원소 중 가장 앞에 있는 것을 꺼내고,  
- 해당 연산으로 원소를 찾아서 꺼냈다면 true를, 해당 원소를 찾지 못했을 경우에는 false를 return한다.  
- queue 안에 데이터가 2개 남아있으므로, size()의 결과는 2다.
***
주요 method 이외에도 priorityqueue의 데이터를 모두 없애는 clear(),  
priorityqueue 안에 특정 데이터가 포함되어 있는지 확인하는 contains() 메소드 등이 있다.
