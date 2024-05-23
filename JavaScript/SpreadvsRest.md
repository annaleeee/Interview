## Spread vs Rest
- `Spread`
  - 배열 또는 Iterable을 `개별` 요소로 분리
  - 반복 가능한 객체( Iterables )에서 요소들을 바로 Key-Value 형태로 만들어서 사용하게 해주는 문법
  - Iterable의 요소들에 대한 접근이 훨씬 용이함
  - 잘 활용하면 기존 배열 함수 ( Push, Concat )을 쓰지 않아도 됨
      
      ```jsx
      const arr = [1, 2, 3, 4];
      
      console.log(arr); // [1, 2, 3, 4]
      console.log(...arr); // 1 2 3 4
      ```
      
  - 사용
      - 배열 결합 ( 기존에는 concat 이용 )
      - 배열 복사 ( 기존에는 slice, map 이용 )
      - 객체에서의 Spread Operator
          - ES2018에서 객체와 관련된 Spread Operator 추가됨
      - Immutable ( 불변성 )
- `Rest`
  - 파라미터에 …을 이용해서 받으면 나머지 인자를 받아 하나의 `배열`로 만들어 사용
  - rest 파라미터는 항상 마지막에 위치
  - 사용
    - 함수의 Rest Parameter
    - 함수 호출 인자로 사용 ( 기존에는 apply 이용 )
    - Destructuring ( 구조 분해 할당 )

#### [ 총정리 ]
- Spread는 말 그대로 어떠한 객체를 spread해서 요소들에 대한 Key-Value를 만듦
- Rest는 요소들을 하나로 contract 함 → 여러 개의 요소들로 하나의 배열을 만듦
  - 함수의 매개변수 부분에서만 사용 가능
    
