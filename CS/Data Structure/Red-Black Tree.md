## 레드 블랙 트리
- 레드 블랙 트리 ( Red-Black Tree )
  - 자가 균형 이진 탐색 트리 ( Self-balancing binary tree )
    - 일반 이진 탐색 트리에서 자식들이 한쪽으로 치우치는 것을 막기 위한 균형 기능이 추가된 트리
  - 새로 삽입되는 노드의 색은 Red
      - Double Red가 발생하지 않도록 해야 함
        
#### [ 조건 ]
- 모든 노드는 Red이거나 Black
- 루트 노드는 Black
- 모든 리프노드는 Black ( NIL : Null Leaf )
- 노드가 Red면 그 자식은 Black
  - No Double Red → Red 노드가 연속으로 나올 수 없음
- 루트노드에서 모든 리프노드까지의 경로에서 만나는 Black 노드의 수는 같음
