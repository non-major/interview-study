# useMemo와 useCallback의 개념과 차이점을 설명해 주세요.

## 답변

useMemo는 메모이제이션된 '값'을 반환하고, useCallback은 메모이제이션된 '함수'를 반환합니다.

## Memoization(메모이제이션)

기존에 수행한 연산의 결과값을 어딘가에 저장해두고 동일한 입력이 들어오면 재활용하는 프로그래밍 기법입니다.
React에서는 불필요한 리렌더링을 방지하여 성능을 최적화하는데 사용합니다.

## useMemo

메모이제이션된 '값'을 반환하는 hook

```
useMemo(()=> fn, [deps])
```

deps로 지정한 값이 변하게 된다면 ()=> fn 함수를 실행하고, 그 함수의 반환 값을 반환해줍니다.

## useCallback

메모이제이션된 '함수'를 반환하는 hook

```
useCallback(fn, [deps])
```

deps로 지정한 값이 변하게 된다면 fn 함수를 반환해줍니다.

## useMemo, useCallback의 사용

useMemo

1. 과도한 계산이 포함된 함수를 사용할 때

useCallback

1. 자식 컴포넌트에 props로 함수를 전달할 경우
2. 외부에서 값을 가져오는 api를 호출하는 경우

참고 : https://narup.tistory.com/273
