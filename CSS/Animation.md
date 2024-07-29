## CSS Animation vs JS Animation
`CSS Animation`
  - JS보다 좀 더 간단한 애니메이션을 구현 및 처리하는 데 사용
  #### [ 장점 ]
  - 반응형으로 구현하기 좋음
  - 외부 라이브러리를 필요로 하지 않음
  - 애니메이션이 어디서 일어나는지 알아보기 쉬움
    - CSS는 선언형 특징 有 → 요소에 직접 애니메이션을 지정
  - 메인 스레드가 아닌 별도의 컴포지터 스레드에 그려짐 <br>
    → 메인 스레드에서 작업하는 JS보다 효율적임
    - 메인 스레드에는 스타일 지정, 레이아웃 변경, 페인트 같은 자바스크립트가 수행되는 스레드
  - 간편성
    - CSS만으로 애니메이션을 만듦 → 쉽고 빠르게 작성 가능
---
`JavaScript Animation`
- 효율적이고 세밀하게 다룰 수 있음
- JavaScript의 requestAnimationFrame API나 JavaScript 애니메이션 라이브러리 사용
  - requestAnimationFrame API ⇒ 프레임을 정확히 제어 가능
 #### [ 장점 ]
 - 요소의 스타일이 변하는 스타일마다 제어할 수 있음
  - 세밀한 구성 가능
- GPU를 통한 하드웨어 가속 제어 가능
- 브라우저 호환성 측면에서 CSS보다 뛰어남
  - 크로스 부라우징 측면에서 좋음