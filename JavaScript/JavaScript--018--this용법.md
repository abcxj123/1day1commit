# this
- this는 호출 패턴에 따라 다른 객체를 참조한다.
- 실행 컨텍스트가 생성될 때마다 this의 바인딩이 일어나며 우선순위 순으로 나열해보면 다음과 같다.

### 1. new를 사용했을 때 해당 객체로 바인딩된다.
```
var name = 'javascript';
function func() {
  this.name = 'func';
  this.print = function f() {
    console.log(this.name);
  };
}
var test = new func();
test.print(); // func 출력
```

### 2. call, apply, bind와 같은 명시적 바인딩을 사용했을 때 인자로 전달된 객체에 바인딩된다.
```
function func() {
  console.log(this.name);
}
var obj = { name: 'obj name' };
func.call(obj); // obj name 출력
func.apply(obj); // obj name 출력
func.bind(obj)(); // obj name 출력
```

### 3. 객체의 메소드로 호출할 경우 해당 객체에 바인딩된다.
```
var obj = {
  name = 'obj name',
  print: function p() {
    console.log(this.name);
  },
};
obj.print(); // obj name 출력
```

### 4. 그 외의 경우
- strict mode : <code>undefined</code>로 초기화된다.
- 일반 : 브라우저라면 <code>window</code> 객체에 바인딩된다.
