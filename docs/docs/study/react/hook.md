# react hook

## Hook 이란
함수 컴포넌트에서 React의 기능을 사용할 수 있게 해주는 JavaScript 함수. 이전에는 클래스 컴포넌트에서만 상태(state) 관리와 생명주기(lifecycle) 메서드를 사용할 수 있었지만, Hook을 사용하면 함수 컴포넌트에서도 이러한 기능들을 사용할 수 있다.

## useState
매번 하던거. state 를 관리한다.
useState() 함수는 state 변수와 setState() 함수를 리턴한다. 이걸 가지고 상태 관리하면 됨.

## useEffect
함수 컴포넌트의 생명주기(lifecycle)와 관련된 작업을 수행하기 위해 사용
```typescript
useEffect( 콜백함수(), 의존성 배열[] )
```

```javascript
useEffect(() => {
  // 컴포넌트의 업데이트 시 실행되는 코드
  // ...

  return () => {
    // 업데이트 시 클린업(cleanup) 코드
    // ...
  };
}, [dependency]);

```
위의 예시에서 `[dependency]` 부분에 특정 상태나 속성의 의존성 배열(dependency array)을 전달하면, 해당 상태나 속성의 값이 변경될 때마다 useEffect 효과가 실행됨.
빈 배열(`[]`)을 전달하면, 해당 useEffect 효과는 컴포넌트가 마운트될 때 한 번만 실행됨.

## useContext
Context는 React 컴포넌트 트리를 통해 전역적으로 데이터를 공유할 수 있는 메커니즘입니다. useContext를 사용하면 Context에서 값을 읽거나 업데이트할 수 있습니다.
[react 공식문서 context](https://react.dev/learn/passing-data-deeply-with-context)
state 중 전역으로 관리해야 할 친구들을 useContext 로 사용하면 될 듯

## useRef
state 와 비슷한데, 렌더링을 바로바로 안함.
DOM 요소에 대한 참조를 유지할 수 있다.
주로 useEffect 와 함께 사용되는데 컴포넌트와 무관한 부가 작업을 수행하는 데 쓰임. 클린업 작업을 정의하거나 외부 라이브러리에 대한 초기화 작업을 하는 데 사용가능.
화면에 표시하는 정보를 저장하려면 상태를 사용. [useRef vs useState](https://react.dev/learn/referencing-values-with-refs#differences-between-refs-and-state)
[공식문서 useRef](https://react.dev/reference/react/useRef)

## useCallback, useMemo
[티스토리가 세상을 구한다](https://narup.tistory.com/273)

## useReducer, useLayoutEffect, etc ...
