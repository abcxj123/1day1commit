# JavaScript 배열 내장함수
***
  
splice는 배열에서 특정 항목을 제거할 때 사용한다.  
splice를 사용할 때 첫 번째 파라미터는 어떤 인덱스부터 지울지를 의미하고,  
두 번째 파라미터는 그 인덱스부터 몇 개를 지울지를 의미한다.
```
const numbers = [10, 20, 30, 40];
```
위 배열에서 30을 지운다고 가정한다면, 30이 몇 번째 index인지 알아낸 후, 이를 splice를 통해 지워줄 수 있다.
```
const numbers = [10, 20, 30, 40];
const index = numbers.indexOf(30);
numbers.splice(index, 1);
console.log(numbers); // 10 20 40
```
### slice
slice는 splice랑 조금 비슷하다. slice는 배열을 잘라낼 때 사용하고, 중요한 점은 기존의 배열을 건들이지 않는다는 것이다.  
slice에는 두 개의 파라미터를 넣게 되는데, 첫 번째 파라미터는 어디서부터 자를지,  
그리고 두 번째 파라미터는 어디까지 자를지를 의미한다.
```
const numbers = [10, 20, 30, 40];
const sliced = numbers.slice(0, 2); // 0부터 시작해서 2전까지

console.log(sliced); // 10 20
console.log(numbers); // 10 20 30 40
```
### shift 와 pop
shift와 pop은 비슷하지만 조금 다르다.  
shift는 첫 번째 원소를 배열에서 추출해준다. (해당 원소는 배열에서 사라진다.)  
```
const numbers = [10, 20, 30, 40];
const value = numbers.shift();
console.log(value); // 10
console.log(numbers); // 20, 30, 40
```
pop을 마지막 원소를 배열에서 추출해준다. (해당 원소는 배열에서 사라진다.)
```
const numbers = [10, 20, 30, 40];
const value = numbers.pop();
console.log(value); // 40
console.log(numbers); // 10 20 30
```
pop은 push의 반대로 생각하면 된다. push는 배열의 맨 마지막에 새 항목을 추가하고, pop은 맨 마지막 항목을 추출한다.
### unshift
unshift는 shift의 반대이다.  배열의 맨 앞에 새 원소를 추가한다.
```
const numbers = [10, 20, 30, 40];
numbers.unshift(5);
console.log(numbers); // 5 10 20 30 40
```
