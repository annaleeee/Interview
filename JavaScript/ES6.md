## ES6에서 새로 생긴 기능
- `블록 스코프, let, const`
  - 블록 스코프 ( 범위 : 중괄호 안 )
  - 블록 { } 이 생성될 때마다 새로운 스코프가 형성
  - var는 함수 스코프 ( 범위 : 함수 안 )
- `클래스`
- `모듈`
  - 애플리케이션을 구성하는 개별적 요소로 재사용한 코드 조각
  - 파일 단위로 분리하며 필요에 따라 명시적으로 모듈을 로드하여 사용
  - 엄격 모드에서만 적용됨
    - 모듈에서 선언된 변수나 함수가 자동으로 전역 스코프에 적용되지 않음
  - 자기만의 스코프를 가짐
- `화살표 함수`
- `매개변수 기본값 ( Default Parameters )`
  - 함수 정의할 때 파라미터는 기본적으로 ‘undefined’ 타입으로 정해짐
    - 디폴트 파라미터를 함수 선언에 적어 놓지 않으면 기본적으로 ‘undefined’ 타입이 됨
- `템플릿 리터럴 ( `` )`
  - 표현식 삽입을 통해 간결한 표현이 가능
  - 동적인 값을 표현하는 것이 수월해짐
  - 줄바꿈 허용, 공백 그대로 적용
- `디스트럭쳐링 ( Destructuring )`
  - 구조 분해 할당
  - 구조화된 배열 또는 객체를 Destructuring(비구조화)하여 개별적인 변수에 할당
  - 배열 또는 객체 리터럴에서 필요한 값만 추출하여 변수에 할당하거나 반환할 때 유용
- `스프레드 연산자 ( … )`
  - 기존 배열이나 객체의 전체 또는 일부를 다른 배열이나 객체로 빠르게 복사 가능
- `심볼 ( Symbol ) 타입`
- `프로미스`
  - 비동기 처리를 위한 객체
    ```
      const promise = new Promise((resolve, reject) => {
        // ...비동기 처리할 영역
        // 보통 network 통신에 사용
      });
    ```
  - Promise 객체의 3가지 상태
    - 대기 ( pending )
      - 이행하지도, 거부하지도 않은 초기 상태
    - 이행 ( fulfilled )
      - 연산이 성공적으로 완료됨
    - 거부 ( rejected )
        - 연산 실패
