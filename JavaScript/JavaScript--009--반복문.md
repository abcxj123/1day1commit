# JavaScript 반복문
- 반복문은 특정 작업을 반복적으로 할 때 사용할 수 있는 구문이다.
***
  
### for
for 문은 가장 기본적인 반복문이다. 특정 값에 변화를 주어가면서 정해진 조건이 만족된다면 계속 반복한다.
```
for (let i = 0; i < 5; i++) {
  console.log(i); // 0 1 2 3 4 5
};
```
for 문은 다음과 같이 사용한다.
```
for (초기 구문; 조건 구문; 변화 구문;) {
  코드
}
```
Java와의 차이점은 int가 아닌 let을 사용한다는 것이다.  
  
### 배열과 for
```
const names = ['멍멍이', '야옹이', '멍뭉이'];

for (let i = 0; i < names.length; i++) {
  console.log(names[i]); // 멍멍이 야옹이 멍뭉이
}
```
이렇게 하면 names 배열 안에 있는 원소들을 하나하나 나열할 수 있다.  
### while
while문은 특정 조건이 참이라면 계속해서 반복하는 반복문이다.
```
let i = 0;
while (i < 5) {
  console.log(i); // 0 1 2 3 4
  i++;
}
```
### 객체를 위한 반복문 for...in
객체가 지니고 있는 값에 대하여 반복을 하고 싶다면 for...in 구문을 사용하면 된다.
```
const doggy = {
  name: '멍멍이',
  sound: '멍멍',
  age: 2
};

for (let key in doggy) {
  console.log(`${key}: ${doggy[key]}`); // name: 멍멍이 sound: 멍멍 age: 2
}
```
### break와 continue
반복문 안에서는 break와 continue를 통하여 반복문을 벗어나거나, 그 다음 루프를 돌게끔 할 수 있다.
```
for (let i = 0; i < 10; i++) {
  if (i === 2) continue; // 다음 루프를 실행
  console.log(i); // 0 1 2 3 4 5
  if (i === 5) break; // 반복문을 끝내기
}
```
