## Spread vs Rest
- Spread
  - 배열 또는 Iterable을 ‘개별’ 요소로 분리
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
