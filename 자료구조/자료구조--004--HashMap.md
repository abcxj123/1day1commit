# HashMap
- Map 인터페이스를 구현하고 있는 클래스이다.
- 키(Key)와 값(Value)로 구성되어 있다.
***
### HashMap 특징
- **한 개**의 Key는 **한 개**의 Value만 가질 수 있다.
- 주로 검색하는 일을 할 때 사용하는 자료구조이다. (**검색 속도가 매우 빠르다.**)
- 저장 속도가 느리다.
- Key는 중복이 안되지만, Value는 중복이 가능하다.
***
### HashMap 선언
다음과 같이 HashMap을 선언한다.
```
Map<String, Integer> map = new HashMap<>();
HashMap<Integer, Boolean> map2 = new HashMap<>();
```
***
### HashMap에 데이터 저장하기
다음과 같이 HashMap에 데이터를 저장할 수 있다.
```
HashMap<String, Integer> map = new HashMap<>();
map.put("test", 1000);
map.put("test2", 2000);
```
***
### HashMap 데이터 사용하기
다음과 같이 HashMap의 값을 사용할 수 있다.
```
HashMap<String, Integer> map = new HashMap<>();
map.put("test", 1000);
map.put("test2", 2000);
map.put("test", 3000);

System.out.println(map.get("test")) // 3000
System.out.println(map.get("test2")) // 2000
```
- Key는 중복이 안되므로, 나중에 들어온 3000이라는 Value가 저장되었다.
***
### HashMap에 있는 데이터 삭제하기
다음과 같이 HashMap에 있는 데이터를 삭제할 수 있다.
```
HashMap<String, Integer> map = new HashMap<>();
map.put("test", 1000);
map.put("test2", 2000);

map.remove("test");

System.out.println(map.size()); // 1

map.clear();

System.out.println(map.isEmpty()); // true
```
- remove()는 HashMap에 있는 데이터 중 () 안에 들어있는 값과 일치하는 Key를 삭제한다.  
- clear()는 HashMap에 있는 데이터를 모두 삭제한다.
