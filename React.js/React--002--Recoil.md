# Recoil이란?
- 페이스북에서 출시한 React 전역 상태관리 라이브러리중 하나이다.
- 다른 라이브러리(Redux, Mobx)와는 달리 React 전용이며, React에 최적화되어 있다.

***
### Atoms
- atoms는 컴포넌트가 구독할 수 있는 상태의 단위이며, 업데이트가 가능하다.
- atom이 업데이트되면 각각의 구독된 컴포넌트는 새로운 값을 반영하여 다시 렌더링된다.
- atoms는 런타임에서 생성될 수도 있다.
- atoms는 React의 로컬 컴포넌트의 상태 대신 사용할 수 있다.
- 동일한 atom이 여러 컴포넌트에서 사용되는 경우 모든 컴포넌트는 상태를 공유한다.  

Atoms는 <code>atom</code>함수를 사용하여 생성한다.
```
const fontState = atom({
  key: 'fontState',
  default: 14,
});
```
컴포넌트에서 atom을 읽고 쓰려면 <code>useRecoilState</code>라는 훅을 사용한다. React의 useState와 비슷하지만 상태가 컴포넌트 간에 공유될 수 있다는 차이가 있다.
```
function FontButton() {
  const [fontSize, setFontSize] = useRecoilState(fontState);
  return (
    <button onClick={() => setFontSize((size) => size + 1)} style = {{fontSize}}>
      Click Button
    </button>
  );
}
```
버튼을 클릭하면 버튼의 글꼴 크기가 1만큼 증가하며, fontState atom을 사용하는 다른 컴포넌트의 글꼴 크기도 같이 변화한다.
***
### Selectors
- Selectors는 atoms 상태 값을 동기 또는 비동기 방식을 통해 변환한다.
- Selector는 atoms나 다른 selectors를 입력으로 받아들이는 순수 함수(pure function)다.
- 상위의 atoms 또는 selectors가 업데이트되면 하위의 selector 함수도 다시 실행된다.
- 컴포넌트들은 selectors를 atoms처럼 구독할 수 있으며 selectors가 변경되면 컴포넌트들도 다시 렌더링된다.
- Selectors는 어떤 컴포넌트가 자신을 필요로하는지, 또 자신은 어떤 상태에 의존하는지를 추적하기 때문에 이러한 함수적인 접근방식을 매우 효율적으로 만든다.  
  
Selectors는 <code>selector</code>함수를 사용해 정의한다.
```
const fontSizeLabelState = selector({
  key: 'fontSizeLabelState',
  get: ({get}) => {
    const fontSize = get(fontSizeState);
    const unit = 'px';

    return `${fontSize}${unit}`;
  },
});
```
<code>get</code> 속성은 계산될 함수이다. 전달되는 <code>get</code> 인자를 통해 atoms와 다른 selectors에 접근할 수 있다.  
다른 atoms나 selectors에 접근하면 자동으로 종속관계가 생성되므로, 참조했던 다른 atoms나 selectors가 업데이트되면 이 함수도 다시 실행된다.  
  
Selectors는 <code>useRecoilValue()</code>를 사용해 읽을 수 있다. <code>useRecoilValue()</code>는 하나의 atom이나 selector를 인자로 받아 대응하는 값을 반환한다.
<code>fontSizeLabelState</code> selector는 writeable하지 않기 때문에 <code>useRecoilState()</code>를 이용하지 않는다.
```
function FontButton() {
  const [fontSize, setFontSize] = useRecoilState(fontSizeState);
  const fontSizeLabel = useRecoilValue(fontSizeLabelState);

  return (
    <>
      <div>Current font size: ${fontSizeLabel}</div>

      <button onClick={setFontSize(fontSize + 1)} style={{fontSize}}>
        Click Button
      </button>
    </>
  );
}
```
버튼을 클릭하면 버튼의 글꼴 크기가 증가하는 동시에 현재 글꼴 크기를 반영하도록 글꼴 크기 레이블을 업데이트하는 두 가지 작업이 수행된다.  
<br>
출처 : https://recoiljs.org/ko/docs/introduction/core-concepts/
