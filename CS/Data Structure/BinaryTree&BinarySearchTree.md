## 이진 트리와 이진 탐색 트리
- 이진 트리 ( Binary Tree )
  - 자식 노드가 최대 두 개인 노드들로 구성된 트리
    
- 이진 탐색 트리 ( Binary Search Tree )
  - `이진 탐색 + 연결 리스트`를 결합한 이진트리
  - 탐색을 위한 이진 트리
    - 이진 트리의 하위 개념
  - 빈번한 자료 입력과 삭제를 가능하게끔 고안됨
  - 왼쪽 노드는 작고, 오른쪽으로 갈 수록 노드가 커짐
    - 모든 왼쪽 자식의 값이 루트나 부모보다 작고, 모든 오른쪽 자식의 값이 루트나 부모보다 큰 값을 가짐
  - 이진 탐색 트리 구현 코드
    
    ```
      class treeNode {
      constructor(data) {
        this.data = data;
        this.left = null;
        this.right = null;
      }
    }
    
    class BinarySearchTree {
      constructor() {
        this.root = null;
      }
      insert(data) {
        let node = new treeNode(data);
        if(!this.root) { // 루드가 설정되어 있지 않다면, 루트를 node로 만듦 -> node는 treeNode()에서 뼈대를 받아옴
          this.root = node;
          return this;
        }
        
        let current = this.root; // 비교를 위해 current 를 설정
        while(current){ // current가 true 라면 while문을 돌면서 data와 지금 현재 data인 current data를 비교
          if(data === current.data){ // 중복된 값은 어떤 결과를 리턴하지 않음
            return;
          }
          if(data < current.data){ // data가 current data(기준) 보다 작다면 왼쪽에 넣어줌
            if(!current.left){
              current.left = node;
              break;
            }
            current = current.left; // 이제 current data(기준)는 왼쪽의 data로 줌
          }
          if(data > current.data){ // data가 기준 data(current data) 보다 크다면 오른쪽에 넣어줌
            if(!current.right){
              current.right = node;
              break;
            }
            current = current.right; // 이제 current data(기준)는 오른쪽 data로 줌
          }
        }
      }
    }
  
      let nums = new BinarySearchTree();
      nums.insert(10);
      nums.insert(5);
      nums.insert(2);
      nums.insert(20);
      
      console.log(nums);
    ```
