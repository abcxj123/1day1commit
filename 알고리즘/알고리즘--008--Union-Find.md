# Union-Find
- 그래프/트리에서 사용하는 알고리즘이다.
- 서로소인 부분집합의 표현이다.
- 서로 다른 두 노드가 같은 그래프에 속해있는지 찾고자 할 때 사용한다.
- union 연산과 find 연산을 사용한다.
- 시간 복잡도는 O(logN)이다.

***
### Union-Find 코드
#### Union
```
public static int union(int a, int b) {
  a = find(a);
  b = find(b);
  if(a != b) {
    parent[b] = a;
  }
}
```
#### Find
```
public static int find(int a) {
  if(parent[a] == a) {
    return a;
  }
  return parent[a] = find(parent[a]);
}
```
- Union 함수는 a와 b를 같은 그래프로 합치는 함수이다.
- a와 b의 부모를 확인하여 다르다면, b의 부모를 a로 바꾸는 과정을 통해 합칠 수 있다.
- Find 함수는 a의 부모 노드가 무엇인지 찾는 함수이다.
- a의 부모가 a라면 바로 반환하고, 아니라면 a의 부모를 find 함수로 보내 재귀 호출하여 부모를 찾을 수 있다.
