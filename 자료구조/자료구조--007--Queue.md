# Queue
- 데이터를 저장할 수 있는 자료구조이다.
- 데이터를 뒤(rear)에 추가하고, 앞(front)에서 빼내는 구조이다.
- **FIFO(First In First Out)** 형식을 가진다.
***
### Queue 주요 method
- offer(n), add(n) : 데이터 n을 queue의 가장 뒤에 추가한다.
- poll() : queue의 가장 앞에 있는 원소를 꺼낸다.
- peek() : queue의 가장 앞에 있는 원소를 확인하여 return한다.
- isEmpty() : queue가 비어있는지 여부를 확인한다. 비어있으면 true, 아니면 false를 return한다.
- size() : queue에 들어있는 데이터의 개수를 return한다.
***
### Queue 사용법
```
Queue<Integer> q = new LinkedList<>();

q.add(2);
q.add(4);
q.add(6);
q.add(8);
q.add(10);

System.out.println(q.poll()); // 2

System.out.println(q.peek()); // 4

System.out.println(q.pop()); // 4

System.out.println(q.isEmpty()); // false

System.out.println(q.remove()); // 6

System.out.println(q.remove(10)); // true, 원소 '10'이 지워짐.

System.out.println(q.size()); // 1
```
- queue에 2, 4, 6, 8을 넣었을 때 poll() 연산을 하면 가장 먼저 들어온 2를 꺼내고,  
- peek()을 하면 그 뒤에 있던 4를 반환한다.  
- peek()은 실제로 데이터를 꺼내는 연산은 아니기 때문에  
- 다시 poll()을 실행하면 4를 꺼내오게 된다.  
- queue 안에 6, 8이 아직 남아있으므로, isEmpty()의 결과는 false이다.  
- remove() 연산을 하면 poll()과 마찬가지로 가장 앞에 있는 원소인 6을 꺼내서 return한다.  
- remove(10) 연산을 하면 Queue에 들어있는 10이라는 원소 중 가장 앞에 있는 것을 꺼내고,  
- 해당 연산으로 원소를 찾아서 꺼냈다면 true를, 해당 원소를 찾지 못했을 경우에는 false를 return한다.  
- queue 안에 데이터가 1개 있으므로, size()의 결과는 1이다.
***
주요 method 이외에도 queue의 데이터를 모두 없애는 clear(),  
queue 안에 특정 데이터가 포함되어 있는지 확인하는 contains() 메소드 등이 있다.
