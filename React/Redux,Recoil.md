## Redux vs Recoil
- Redux
  - Faceook이 고안한 Flux 아키텍처 많이 사용 (Flux 패턴을 구현한 라이브러리)
      - 데이터 흐름은 단방향으로 흐름
      - action, reducer, selector, store를 초기 세팅하는 부분은 많은 코드를 소모
      - React에 최적화된 라이브러리 X
          
          → 2020년 Facebook에서 Recoil 출시
          
  - 상태를 전역적으로 관리 → 어느 컴포넌트에 상태를 둬야할지 고민할 필요 X
  - 불변성 유지 중요
      - 상태를 읽기 전용으로 취급
  - 틀이 정해져 있어 유지보수 용이함
  - 다양한 미들웨어의 존재
- Recoil
  - A state management library for React
  - Context API 기반으로 구현된 함수형 컴포넌트에서만 사용 가능
  - 비동기 처리를 기반으로 작성되어 동시성 모드 제공
      - Redux와 같이 다른 비동기처리 라이브러리에 의존할 필요 X
<br>
-> redux에서는 store라는 단일 객체에서 관리되었다면, recoil에서는 atom(상태의 단위) 기반으로 전역 상태 관리
<br>

#### [ Redux 대신 Recoil 선택하는 이유 ? ]
  - Redux의 복잡한 코드
  - 간단한 Recoil 개념
  - 쉽게 사용하는 비동기 로직

#### [ Redux의 3가지 원칙 ]
1) The truth comes from one source
  - 진실은 하나의 근원으로부터
    - 애플리케이션의 모든 상태는 하나의 저장소(store)에서 객체 트리 구조로 저장됨
    - 별도의 컴포넌트마다 동기화가 필요없이 store에서 각각
    
    → 실행 취소/다시 실행(undo/redo)을 손쉽게 구현 가능
    
2) State is read-only
  - 상태는 읽기 전용이다
    - 상태는 불변데이터이며, 오직 Action 객체만이 상태교체를 요청할 수 있음
        - 그 요청으로 Reducer가 상태를 변경해줌
        - 액션 객체 → 어떤 상태 변화가 일어나야 하는지 기술된 객체

3) Changes should be written as pure functions
  - 변화는 순수 함수로 작성되어야 한다
    - 액션을 인자로 받아 상태를 변화시키는 reducer는 순수 함수로 만들어야 함
    - reducer는 side effect를 발생시키지 않음
    
    ** reducer
    - 이전 상태와 액션을 받아 다음 상태를 반환하는 순수 함수
    - 이전 상태를 변경하는 것이 아니라, 새로운 상태 객체를 생성해서 반환해야 함
      
