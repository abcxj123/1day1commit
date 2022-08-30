# JavaScript 배열 내장함수
***
  
### findIndex
만약 배열 안에 있는 값이 숫자, 문자열, 또는 boolean이라면 찾고자하는 항목이 몇 번째 원소인지 알아내려면 indexOf를 사용하면 된다.  
하지만, 배열 안에 있는 값이 객체이거나, 배열이라면 indexOf로 찾을 수 없다.  
아래의 예시에서 id가 3인 객체가 몇 번째인지 찾으려면, findIndex 함수에 검사하고자 하는 조건을 반환하는 함수를 넣어서 찾을 수 있다.
```
const todos = [
  {
    id: 1,
    text: '자바스크립트 입문',
    done: true
  },
  {
    id: 2,
    text: '함수 배우기',
    done: true
  },
  {
    id: 3,
    text: '객체와 배열 배우기',
    done: true
  },
  {
    id: 4,
    text: '배열 내장함수 배우기',
    done: false
  }
];

const index = todos.findIndex(todo => todo.id === 3);
console.log(index); // 2
```
### find
find 함수는 findIndex와 비슷하지만, 찾아낸 값이 몇 번째인지 알아내는 것이 아니라, 찾아낸 값 자체를 반환한다.
```
const todos = [
  {
    id: 1,
    text: '자바스크립트 입문',
    done: true
  },
  {
    id: 2,
    text: '함수 배우기',
    done: true
  },
  {
    id: 3,
    text: '객체와 배열 배우기',
    done: true
  },
  {
    id: 4,
    text: '배열 내장함수 배우기',
    done: false
  }
];

const todo = todos.find(todo => todo.id === 3);
console.log(todo);
```
결과는 다음과 같다.
```
{id: 3, text: "객체와 배열 배우기", done: true}
```
### filter
filter 함수는 배열에서 특정 조건을 만족하는 값들만 따로 추출하여 새로운 배열을 만든다.  
예를 들어, 방금 만들었던 todos 배열에서 done 값이 false인 항목들만 따로 추출해서 새로운 배열을 만들 수 있다.
```
const todos = [
  {
    id: 1,
    text: '자바스크립트 입문',
    done: true
  },
  {
    id: 2,
    text: '함수 배우기',
    done: true
  },
  {
    id: 3,
    text: '객체와 배열 배우기',
    done: true
  },
  {
    id: 4,
    text: '배열 내장함수 배우기',
    done: false
  }
];

const tasksNotDone = todos.filter(todo => todo.done === false);
console.log(tasksNotDone);
```
결과는 다음과 같다.
```
[
  {
    id: 4,
    text: '배열 내장 함수 배우기',
    done: false
  }
];
```
filter 함수에 넣는 파라미터는 조건을 검사하는 함수를 넣어주며, 이 함수의 파라미터로 각 원소의 값을 받아오게 된다.  
위의 코드는 다음과 같이 작성할 수도 있다.
```
const tasksNotDone = todos.filter(todo => !todo.done);
```
filter에 넣어준 함수에서 true를 반환하면 새로운 배열에 따로 추출을 해주는데, 만약 todo.done 값이 false라면,  
!false가 되고 이 값은 true 이기 때문에, 이전의 todo.done == false와 똑같이 작동하게 된다.
