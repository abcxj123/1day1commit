# JavaScript 배열 내장함수
***
  
### forEach
forEach는 가장 쉬운 배열 내장함수이다. 기존의 for 문을 대체할 수 있다.  
for 문 사용  
```
const superheroes = ['아이언맨', '캡틴 아메리카', '토르', '닥터 스트레인지'];

for (let i = 0; i < superheroes.length; i++) {
  console.log(superheroes[i]); // 아이언맨, 캡틴 아메리카, 토르, 닥터 스트레인지
}
```
forEach 사용  
```
const superheroes = ['아이언맨', '캡틴 아메리카', '토르', '닥터 스트레인지'];

superheroes.forEach(hero => {
  console.log(hero); // 아이언맨, 캡틴 아메리카, 토르, 닥터 스트레인지
});
```
forEach 함수의 파라미터로는 각 원소에 대하여 처리하고 싶은 코드를 함수로 넣어준다. 이 함수의 파라미터 hero는 각 원소를 가르키게 된다.  
이렇게 함수 형태의 파라미터를 전달하는 것을 콜백함수 라고 부른다. 함수를 등록해주면, forEach가 실행을 해준다.
### map
map 은 배열 안의 각 원소를 변활할 때 사용되며, 이 과정에서 새로운 배열이 만들어진다.  
배열 안의 모든 숫자를 제곱해서 새로운 배열 만들기 (for 문 사용)
```
const array = [1, 2, 3, 4, 5];

const squared = [];
for (let i = 0; i < array.length; i++) {
  squared.push(array[i] * array[i]);
}

console.log(squared); // 1, 4, 9, 16, 25
```
forEach 사용  
```
const array = [1, 2, 3, 4, 5];

const squared = [];

array.forEach(n => {
  squared.push(n * n);
});

console.log(squared); // 1, 4, 9, 16, 25
```
map을 사용하면 이를 더 짧은 코드를 사용하여 구현할 수 있다.
```
const array = [1, 2, 3, 4, 5];

const square = n => n * n;
const squared = array.map(square);
console.log(squared); // 1, 4, 9, 16, 25
```
map 함수의 파라미터로는 변화를 주는 함수를 전달해준다. 이를 변화함수라고 부른다.  
위에서 변화함수 square는 파라미터 n을 받아와서 이를 제곱해준다.  
array.map 함수를 사용할 때 square를 변화함수로 사용함으로서, 내부의 모든 값에 대하여 제곱을 해서 새로운 배열을 생성했다.  
변화 함수를 꼭 이름을 붙여서 선언할 필요는 없다. 코드를 다음과 같이 작성하는 것도 가능하다.
```
const squared = array.map(n => n * n);
console.log(squared);
```
### indexOf
indexOf 는 원하는 항목이 몇 번째 원소인지 찾아주는 함수이다.
예를 들어 토르가 몇 번째 항목인지 알고 싶을 때,
```
const superheroes = ['아이언맨', '캡틴 아메리카', '토르', '닥터 스트레인지'];
const index = superheroes.indexOf('토르');
console.log(index); // 2
```
결과는 2가 나타난다.  
index 값은 0부터 시작하기 때문에 0: 아이언맨, 1: 캡틴 아메리카, 2: 토르, 3: 닥터 스트레인지 임을 확인할 수 있다.
