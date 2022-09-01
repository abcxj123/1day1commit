# JavaScript 배열 내장함수
***

### concat
concat은 여러 개의 배열을 하나의 배열로 합쳐준다.
```
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const concated = arr1.concat(arr2);

console.log(concated); // 1, 2, 3, 4, 5, 6
```
concat 함수는 arr1과 arr2에 변화를 주지 않는다.

### join
join은 배열 안의 값들을 문자열 형태로 합쳐준다.
```
const array = [1, 2, 3, 4, 5];
console.log(array.join()); // 1,2,3,4,5
console.log(array.join(' ')); // 1 2 3 4 5
console.log(array.join(', ')); // 1, 2, 3, 4, 5
```

### reduce
주어진 배열에 대하여 총 합을 구해야 하는 상황이라면 다음과 같이 구현할 수 있다.
```
const numbers = [1, 2, 3, 4, 5];

let sum = 0;
numbers.forEach(n => {
  sum += n;
});
console.log(sum); // 15
```
여기서 sum을 계산하기 위해 사전에 sum을 선언하고, forEach를 통하여 계속 덧셈했지만,  
reduce 함수를 사용하면 다음과 같이 구현할 수 있다.
```
const numbers = [1, 2, 3, 4, 5];
let sum = array.reduce((accumulator, current) => accumulator + current, 0);

console.log(sum); // 15
```
reduce 함수에는 두 개의 파라미터를 전달한다. 첫 번째 파라미터는 accumulator와 current를 파라미터로 가져와서 결과를 반환하는 콜백함수이고,  
두 번째 파라미터는 reduce 함수에서 사용할 초기값이다. 여기서 accumulator는 누적값을 의미한다.  
reduce를 사용해서 평균도 계산할 수 있다. 평균을 계산하려면, 가장 마지막 숫자를 더하고 나서 배열의 length로 나누어주어야 한다.
```
const numbers = [1, 2, 3, 4, 5];
let sum = numbers.reduce((accumulator, current, index, array) => {
  if (index === array.length - 1) {
    return (accumulator + current) / array.length;
  }
  return accumulator + current;
}, 0);

console.log(sum); // 3
```
위 코드에서 reduce에서 사용한 콜백함수에서는 추가 파라미터로 index와 array를 받아왔다.  
index는 현재 처리하고 있는 항목이 몇 번째인지 가르키고, array는 현재 처리하고 있는 배열 자신을 의미한다.  
