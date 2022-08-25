# JavaScript 함수
- 함수는 특정 코드를 하나의 명령으로 실행할 수 있게 해주는 기능이다.
***
  
### 함수
우리는 특정 값들의 합을 구하고 싶을 때 다음과 같은 코드를 작성한다.  
```
const a = 1;  
const b = 1;  
const sum = a + b;  
```
이 작업을 함수로 구현한다면,
```
function add(a, b) {  
  return a + b;  
}  
  
const sum = add(1, 2);  
console.log(sum); // 3
```

다음과 같은 코드에서는 return 아래의 코드는 호출이 안된다.
```
function add(a, b) {  
  return a + b;  
  console.log('호출이 되지 않는 코드');
}  
  
const sum = add(1, 2);  
console.log(sum); // 3
```

### 화살표 함수
함수를 선언하는 방식 중 또 다른 방식은 화살표 함수 문법을 사용하는 것이다.
```
const add = (a, b) => {
  return a + b;  
};
  
console.log(add(1, 2)); // 3  
```
코드 블록 내부에서 바로 return을 하는 경우는 다음과 같이 줄여서 쓸 수도 있다.  
```  
const add = (a, b) => a + b;
console.log(add(1, 2)); // 3  
```
화살표 함수와 일반 function으로 만든 함수의 주요 차이점은  
화살표 함수에서 가르키는 this와 function에서 가르키는 this가 서로 다르다는 것이다.
