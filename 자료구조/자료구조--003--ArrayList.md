# ArrayList
- 배열보다 느리지만, 배열에서 많은 조작이 필요한 경우 유용하게 사용할 수 있다.
- List 인터페이스에서 상속 받아 사용된다.
- **ArrayList는 객체가 추가되어 용량이 초과하면 부족한 크기만큼 용량이 자동으로 늘어난다.**
***
### ArrayList 선언
다음과 같이 ArrayList를 선언한다.
```
ArrayList<Integer> list = new ArrayList<>();
ArrayList<String> list2 = new ArrayList<>();
```
***
### ArrayList에 데이터 저장하기
다음과 같이 ArrayList에 데이터를 저장할 수 있다.
```
ArrayList<Integer> list = new ArrayList<>();
list.add(1);
list.add(2);
list.add(3);
```
***
### ArrayList 데이터 사용하기
다음과 같이 ArrayList의 값을 사용할 수 있다.
```
ArrayList<Integer> list = new ArrayList<>();
list.add(1);
list.add(2);
list.add(3);

System.out.println(list.get(2)); // 3
System.out.println(list.contains(1)); // true
System.out.println(list.indexOf(2)); // 1
```
- index가 0부터 시작하기 때문에 3을 출력한다.  
- contains()는 ()안에 있는 데이터가 Arraylist에 존재하는지 유무를 알려준다.  
- indexOf()는 ()안에 있는 데이터 중 가장 처음의 index를 출력한다.
***
### ArrayList에 있는 데이터 변경하기
다음과 같이 ArrayList에 있는 데이터를 변경할 수 있다.
```
ArrayList<Integer> list = new ArrayList<>();
list.add(1);
list.add(2);
list.add(3);

list.set(0, 10);

System.out.println(list.get(0)); // 10
```
***
### ArrayList에 있는 데이터 삭제하기
다음과 같이 ArrayList에 있는 데이터를 삭제할 수 있다.
```
ArrayList<Integer> list = new ArrayList<>();
list.add(1);
list.add(2);
list.add(3);

list.remove(1);

System.out.println(list.get(0)); // 2

list.clear();
```
- remove()는 Arraylist에 있는 데이터 중 () 안에 들어있는 값과 같은 가장 처음 데이터를 삭제한다.  
- clear()는 Arraylist에 있는 데이터를 모두 삭제한다.
