## Streaming
- Streaming
  - 전체를 렌더링하면 사용자 경험이 떨어질 수도 있음 <br>
    → 먼저 완성된 부분들만 점진적으로 보여주도록 부분 렌더링을 해주는 기능
  - 스트리밍 방식을 사용하는 렌더링
    
    → Progressive Rendering (점진적 렌더링)
    
  - `suspense`를 사용하여 로딩 화면을 지정할 수 있음 <br>
   → suspense라는 도구가 필요함
    - 컴포넌트가 로딩될 때까지 그 화면을 보여 줌
    - fallback UI로 suspense를 props로 던져줌
    - 로딩이 되면 suspense로 감싼 요소들만 html 요소로 넘겨줌
    - 다른 부분은 로딩 화면으로 남아있을 수도 있음 (부분 렌더링)
    - 점진적으로 완성해나감
