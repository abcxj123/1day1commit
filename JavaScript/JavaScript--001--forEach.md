# Array.prototype.forEach()
forEach() 메서드는 주어진 함수를 배열 요소 각각에 대해 실행합니다.
  
### arr.forEach(callback(currentvalue[, index[, array]])[, thisArg])
  
**`callback`**  
각 요소에 대해 실행할 함수. 다음 세 가지 매개변수를 받습니다.
  
**`currentValue`**  
처리할 현재 요소
  
**`index`** <sub>optional</sub>  
처리할 현재 요소의 인덱스
  
**`array`** <sub>optional</sub>  
forEach()를 호출한 배열
  
**`thisArg`** <sub>optional</sub>  
callback을 실행할 때 this로 사용할 값

***
### for문
```
var arr = [1, 3, 5, 2, 4];

for(var i=0;i<arr.length<i++) {
console.log("index: "+index+", value: "+element);
});
```
### 사용예
```
var arr = [1, 3, 5, 2, 4];

arr.forEach(function(element, index) {
console.log("index: "+index+", value: "+element);
});
```
### 출력
```
index: 0, value: 1
index: 1, value: 3
index: 2, value: 5
index: 3, value: 2
index: 4, value: 4
```
***
  
- for문보다는 느리지만 가독성과 접근성이 훨씬 좋다.
- 중간에 break, continue, return 등으로 벗어날 수 없다.
