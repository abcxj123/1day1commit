# JavaScript 연산자
- 연산자는 프로그래밍 언어에서 특정 연산을 하도록 하는 문자이다.  
***
  
### 산술 연산자
산술 연산자는 사칙 연산과 같은 작업을 하는 연산자를 의미한다.
- `+` : 덧셈
- `-` : 뺄셈
- `*` : 곱셈
- `/` : 나눗셈
```
let a = 1 + 2;  
console.log(a); // 3  
  
let a = 1 + 2 - (3 * 4) / 4;
console.log(a); // 0  
  
let a = 1;
a++;
++a;
console.log(a) // 3  
  
let a = 1;
console.log(a++); // 1
console.log(++a); // 3  

let a = 1;
a--;
console.log(a) // 0
```
### 대입 연산자
대입 연산자는 특정 값에 연산을 한 값을 바로 설정할 때 사용할 수 있는 연산자이다.
```
let a = 1;
a += 3;
a -= 3;
a *= 3;
a /= 3;
console.log(a); // 1
```
### 논리 연산자
논리 연산자는 boolean 타입을 위한 연산자이다. 논리 연산자는 if문을 사용할 때 매우 유용하다.
- `!` : NOT
- `&&` : AND
- `||` : OR
#### NOT
```
const a = !true;
console.log(a); // false

const b = !false;
console.log(b); // true
```
#### AND
```
const a = true && true;
console.log(a); // true

let f = false && false; // false
f = false && true; // false
f = true && false; // false
```
#### OR
```
let t = true || false; // true
t = false || true; // true
t = true || true; // true

let t = false || false // false
```
### 비교 연산자
비교 연산자는 두 값을 비교할 떄 사용할 수 있다.
```
const a = 1;
const b = 1;
const equals = a === b;
console.log(equals); // true

const value = 'a' !== 'b'; // true

console.log(1 != '1'); // false
console.log(1 !== '1'); // true

const a = 10;
const b = 15;
const c = 15;

console.log(a < b); // true
console.log(b > a); // true
console.log(b >= c); // true
console.log(a <= c); // true
console.log(b < c); // false
```
### 문자열 붙이기
```
const a = '안녕';
const b = '하세요';
console.log(a + b); // 안녕하세요
```
