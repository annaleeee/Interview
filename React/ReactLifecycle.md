## React Lifecycle (리액트 생명주기)
- React Lifecycle
  - Lifecycle은 컴포넌트가 생성, 사용, 소멸될 때까지의 생명주기
      - mount ( 생성 ), update, unmount ( 제거/소멸 )
  
  [ Mount ]
  
  - `constructor`, `static getDerivedStateFromProps( )`, `render( )`, `componentDidMount( )`
      - ComponentDidMount
          - 컴포넌트가 생성될 때 한 번 호출
  
  [ Update ]
  
  - `static getDerivedStateFromProps( )` , `shouldComponentUpdate( )`, `render( )`, `getSnapshotBeforeUpdate( )`, `componentDidUpdate( )`
      - ComponentDidUpdate
          - 컴포넌트의 props 또는 state 값이 변경되었을 때
            
  - 업데이트 일어나는 상황
      - props 변경 시
      - state 변경 시
      - 부모 컴포넌트가 리렌더링 될 때
      - this.forceUpdate로 강제로 렌더링을 트리거 할 때
  
  [ UnMount ]
  
  - `ComponentWillUnMount( )`
      - 컴포넌트가 소멸될 때 호출
        
[ React Lifecycle을 알아야 하는 이유 ]
  - 생명주기를 알고 생명주기에 따라 어떤 작업을 처리해줘야 하는지 지정해줘야 불필요한 리렌더링을 방지할 수 있음
