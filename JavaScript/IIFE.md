## 즉시 실행 함수 ( IIFE ; Immediately Invoked Function Expression )
- 즉시 실행 함수
  - 정의되자마자 즉시 실행되는 자바스크립트 함수
    - 한 번만 호출되며, 다시 호출할 수 없음
  - 이름이 없는 익명 함수를 사용하는 것이 일반적임
    - 기명 즉시 실행 함수의 경우 함수 이름이 함수 몸체에서만 유효한 식별자이므로 함수를 다시 호출할 수 없음

#### [ 사용 이유 ? ]
- 전역변수 사용을 억제하기 위해
  - 전역 스코프 오염 X
- 정보 은닉을 위해
- 렉시컬 환경을 공유하는 클로저를 만들기 위해
