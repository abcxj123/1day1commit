# JavaScript 객체
- 객체는 우리가 변수 혹은 상수를 사용하게 될 때 하나의 이름에 여러 종류의 값을 넣을 수 있게 해준다.
***
  
### 예시
```
const dog = {
  name: '멍멍이',
  age: 2
};

console.log(dog.name); // 멍멍이
console.log(dog.age); // 2
```  

객체를 선언할 때에는 이렇게 `{ }` 문자 안에 원하는 값들을 넣어주면 된다. 값을 집어 넣을 때에는
```
키: 원하는 값
```
형태로 넣으며, 키에 해당하는 부분은 공백이 없어야한다.  
만약에 공백이 있어야 하는 상황이라면 이를 따옴표로 감싸서 문자열로 넣어주면 된다.  
```
const sample = {
  'key with space' : true
};
```
   
### 함수에서 객체를 파라미터로 받기
```
const ironMan = {
  name: '토니 스타크',
  actor: '로버트 다우니 주니어',
  alias: '아이언맨'
};

const captainAmerica = {
  name: '스티븐 로저스',
  actor: '크리스 에반스',
  alias: '캡틴 아메리카'
};

function print(hero) {
  const text = `${hero.alias}(${hero.name}) 역할을 맡은 배우는 ${
    hero.actor
  } 입니다.`;
  console.log(text);
}

print(ironMan); // 아이언맨(토니 스타크) 역할을 맡은 배우는 로버트 다우니 주니어입니다.
print(captainAmerica); // 캡틴 아메리카(스티븐 로저스) 역할을 맡은 배우는 크리스 에반스입니다.
```

### 객체 안에 함수 넣기
객체 안에 함수를 넣을 수도 있다.
```
const dog = {
  name: '멍멍이',
  sound: '멍멍!',
  say: function say() {
    console.log(this.sound);
  }
};

dog.say(); // 멍멍!
```
객체 안에 함수를 넣을 때, 화살표 함수로 선언한다면 제대로 작동하지 않는다.  
그 이유는, function으로 선언한 함수는 this가 제대로 자신이 속한 객체를 가르키게 되는데, 화살표 함수는 그렇지 않기 때문이다.  
