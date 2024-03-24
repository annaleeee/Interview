## Prop Drilling
- Prop Drilling
  - state나 data를 여러 하위 컴포넌트를 통과하여 특정 하위 컴포넌트에 전달하는 비공식 용어
  - React 컴포넌트 트리의 일부로 데이터를 전달하기 위한 프로세스
      - props를 통해 데이터를 전달하는 과정에서 중간 컴포넌트는 그 데이터가 필요하지 않음에도 자식 컴포넌트에 전달하기 위해 props를 전달해야하는 과정

#### [ 장점 ]
  - 컴포넌트 간 데이터를 가장 쉽고 빠르게 전달 가능
  - 작은 규모의 프로젝트에서 컴포넌트를 잘게 분할하여 prop drilling을 통해 전달하면, 정적으로 따라가는 것만으로도 어떤 데이터가 어디서 사용되는지 쉽게 파악 가능 / 수정도 용이함

#### [ 문제점 ]
  - 넘겨주는 대부분의 하위 컴포넌트에 넘겨준 prop 값이 불필요한 값
  - 프로젝트 규모가 커지고 컴포넌트 수가 많아지면, 코드가 훨씬 복잡해질 수 있음

#### [ 해결 방법 ]
  - React에서 직접 만들고 권장하는 Context API 사용
  - 전역 상태관리 라이브러리 사용 (Redux, Recoil, Jotai)
      - 전역으로 관리하는 저장소에서 직접 state를 꺼내 쓸 수 있음
      - 애플리케이션 전체의 상태를 중앙에서 관리
  - Children을 적극적으로 사용
      - 하나의 컴포넌트에서 값 관리, 그 값을 하위요소로 전달할 때 코드 추적이 어려워지지 않게 됨
  - 커스텀 훅 사용
      - 중복 코드를 최소화하고 데이터를 전달하는 등 유용한 커스텀 훅을 사용하여 문제 완화