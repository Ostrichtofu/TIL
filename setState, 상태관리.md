# 0122 setState, 상태관리



### setState()

##### - setState() 란?

상태(state) 객체에 대한 업데이트를 실행

##### - state란?

렌더링 결과물에 영향을 주는 정보

객체에 속성과 값을 정의할 수 있음

##### - state와 props 차이

- props는 부모 컴포넌트가 자식 컴포넌트에게 주는 값이며 자식 컴포넌트는 이 값 변경 불가능
- props는 사용자의 UI 제공 등에 사용
- state는  컴포넌트 내부에서 선언하고 내부에서 값 변경 가능
- state는 내부 조작 장치(버튼) 등에 사용

##### - setState() 특징

- 비동기로 작동: 브라우저 렌더링이 끝나면 state 값을 업데이트

##### - setState() 사용법

1. setState(updater, [callback])
2. const [getter, setter] = useState(initialValue);
3. getter = > 변수형 setter => 함수형 
