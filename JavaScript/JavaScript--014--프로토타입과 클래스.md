# JavaScript 프로토타입과 클래스
***

### 객체 생성자
객체 생성자는 함수를 통해서 새로운 객체를 만들고 그 안에 넣고 싶은 값 혹은 함수들을 구현할 수 있게 해준다.
```
function Animal(type, name, sound) {
  this.type = type;
  this.name = name;
  this.sound = sound;
  this.say = function() {
    console.log(this.sound);
  };
}

const dog = new Animal('개', '멍멍이', '멍멍');
const cat = new Animal('고양이', '야옹이', '야옹');

dog.say(); // 멍멍
cat.say(); // 야옹
```
객체 생성자를 사용할 때는 보통 함수의 이름을 대문자로 시작하고, 새로운 객체를 만들 때에는 new 키워드를 앞에 붙여주어야 한다.  
같은 객체 생성자 함수를 사용하는 경우, 특정 함수 또는 값을 재사용 할 수 있는데 바로 프로토타입이다.
### 프로토타입
프로토타입은 다음과 같이 객체 생성자 함수 아래에 .prototype[원하는키] = 코드를 입력하여 설정할 수 있다.
```
function Animal(type, name, sound) {
  this.type = type;
  this.name = name;
  this.sound = sound;
}

Animal.prototype.say = function() {
  console.log(this.sound);
};
Animal.prototype.sharedValue = 1;

const dog = new Animal('개', '멍멍이', '멍멍');
const cat = new Animal('고양이', '야옹이', '야옹');

dog.say(); // 멍멍
cat.say(); // 야옹

console.log(dog.sharedValue); // 1
console.log(cat.sharedValue); // 1
```
### 클래스
클래스라는 기능은 다른 프로그래밍 언어에는 있는 기능인데 자바스크립트에는 없었기 때문에 예전 자바스크립트 (ES5) 에서는 클래스 문법이 따로 없었기 때문에  
위에서 작성한 코드처럼 객체 생성자 함수를 사용하여 비슷한 작업을 구현해왔다.  
ES6에서부터는 class 라는 문법이 추가되어, 객체 생성자로 구현했던 코드를 조금 더 명확하고 깔끔하게 구현할 수 있게 해준다.  
추가적으로 상속도 훨씬 쉽게 해줄 수있다.
```
class Animal {
  constructor(type, name, sound) {
    this.type = type;
    this.name = name;
    this.sound = sound;
  }
  say() {
    console.log(this.sound);
  }
}

class Dog extends Animal {
  constructor(name, sound) {
    super('개', name, sound);
  }
}

class Cat extends Animal {
  constructor(name, sound) {
    super('고양이', name, sound);
  }
}

const dog = new Dog('멍멍이', '멍멍');
const cat = new Cat('야옹이', '야옹');

dog.say(); // 멍멍
cat.say(); // 야옹
```
상속을 할 때는 extends 키워드를 사용하며, constructor에서 사용하는 super() 함수가 상속받은 클래스의 생성자를 가르킨다.
```
class Animal {
  constructor(type, name, sound) {
    this.type = type;
    this.name = name;
    this.sound = sound;
  }
}

class Dog extends Animal {
  constructor(name, sound) {
    super('개', name, sound);
  }
}

class Cat extends Animal {
  constructor(name, sound) {
    super('고양이', name, sound);
  }
}

const dog = new Dog('멍멍이', '멍멍');
const dog2 = new Dog('왈왈이', '왈왈');
const cat = new Cat('야옹이', '야옹');
const cat2 = new Cat('냐옹이', '냐옹');

dog.say(); // 멍멍
dog2.say(); // 왈왈
cat.say(); // 야옹
cat2.say(); // 냐옹
```
