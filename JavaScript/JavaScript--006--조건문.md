# JavaScript 조건문
- 조건문을 사용하면 특정 조건이 만족됐을 때 특정 코드를 실행할 수 있다. 
***
  
### if 문
가장 기본적인 조건문은 if 문이다. if 문은, "~하다면 ~를 해라"를 의미한다.  
  
```
const a = 1;  
  
if (a + 1 === 2) {
  console.log(`조건 만족');
} // 출력 됨  
  
const a = 0;  
  
if (a + 1 === 2) {
  console.log('조건 만족');
} // 출력 안됨
  
const a = 1;  
  
if (true) {
  const a = 2;
  console.log('if문 안의 a 값은 ' + a); // 2
 }
console.log('if문 밖의 a 값은 ' + a); // 1
```
### if-else 문
if-else 문은 "~하다면 ~하고, 그렇지 않다면 ~해라."를 의미한다.
```
const a = 10;  
  
if (a > 15) {
  console.log('a가 15보다 크다.');
} else {
  console.log('a가 15보다 크지 않다.');
} // 'a가 15보다 크지 않다' 출력
```
### if-else if 문
if-else if 문은 여러 조건에 따라 다른 작업을 해야할 때 사용한다.
```
const a = 10;  
  
if (a === 5) {
  console.log('5입니다!');
} else if (a === 10) {
  console.log('10입니다!');
} else {
  console.log('5도 아니고 10도 아닙니다.');
} // '10입니다!' 출력
  
a = 5 -> '5입니다!' 출력
a = 7 -> '5도 아니고 10도 아닙니다.' 출력
```
### switch/case 문
switch/case 문은 특정 값이 무엇이냐에 따라 다른 작업을 하고싶을 때 사용한다.
```
const device = 'iphone';  
  
switch (device) {
  case 'iphone':
    console.log('아이폰!');
    break;
  case 'ipad':
    console.log('아이패드!');
    break;
  case 'galaxy note':
    console.log('갤럭시 노트!');
    break;
  default:
    console.log('모르겠네요..');
} // '아이폰!' 출력
```
