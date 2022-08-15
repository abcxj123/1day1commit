# useState()
컴포넌트의 상태 관리를 위해 React Hooks에서 제공되는 함수.

```
const [상태 값 저장 변수, 상태 값 갱신 함수] = useState(상태 초기 값);
```

  
### 사용예
```
const [number, setNumber] = useState(0);
const [name, setName] = useState("홍길동");
```

***

- 더 짧은 코드로 큰 성능을 낼 수 있다.
- 컴포넌트를 단순화 할 수 있다.
