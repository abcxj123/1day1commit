# JavaScript Array
- Array는 리스트 형태의 고수준 객체인 배열을 생성할 때 사용하는 전역 객체이다.
- JavaScript 배열은 길이, 자료형이 고정되어 있지 않다.
- 배열의 길이가 언제든지 늘어나거나 줄어들 수 있고, 데이터를 연속적이지 않은 곳에 저장할 수 있으므로, JavaScript 배열은 밀집성을 보장하지 않는다.
***
  
#### 배열 만들기
```
let arr = new Array();
let arr = [];
let fruits = ["사과", "오렌지", "자두"];
```
#### 배열 내 특정 요소 얻기
```
let fruits = ["사과", "오렌지", "자두"];
console.log(fruits[0]); // 사과
```
#### 요소 수정하기
```
fruits[2] = "배"; // fruits = ["사과", "오렌지", "배"]
```
#### 요소 추가하기
```
fruits[3] = "레몬"; // fruits = ["사과", "오렌지", "배", "레몬"]
```
#### 배열의 길이
```
let fruits = ["사과", "오렌지", "자두"];
console.log(fruits.length) // 3
```
#### 배열 전체 출력
```
let fruits = ["사과", "오렌지", "자두"];
console.log(fruits) // 사과, 오렌지, 자두
```
