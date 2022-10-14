# preventDefault()
- 어떤 이벤트를 명시적으로 처리하지 않은 경우, 해당 이벤트에 대한 사용자 에이전트의 기본 동작을 실행하지 않도록 지정한다.
- 이벤트 흐름의 어떤 단계에서라도 preventDefault()를 호출하면 이벤트를 취소한다.
- 이벤트에 대한 구현체의 기본 동작을 실행하지 않는다.
  
### 예시
```
function checkName(e) {
  var charCode = e.charCode;
  if (charCode != 0) {
    if (charCode < 97 || charCode > 122) {
      e.preventDefault();
      displayWarning(
        "영문 소문자만 입력하세요."
        + "\n" + "charCode: " + charCode + "\n"
      );
    }
  }
}
```
# stopPropagation()
- 현재 이벤트의 추가 전파를 방지한다.
- 하지만 기본 동작이 발생하는 것을 방지하지는 않습니다. 진행중이던 이벤트는 계속 처리된다.
- 이벤트를 즉각적으로 중지하려면 preventDefault()를 사용해야 한다.
  
```
e.stopPropagation();
```
***
## e.preventDefault vs e.stopPropagation()
- e.preventDefault는 이벤트의 고유 동작을 중지시킨다.
- e.stopPropagation은 이벤트가 상위 엘리먼트로 전파하는 것을 중단시킨다. (이벤트 자체를 중단시키지는 않는다.)
