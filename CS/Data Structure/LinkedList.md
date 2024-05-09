## Linked List ( 연결리스트 )
- 연결리스트
  - 데이터랑 넥스트로 구성되어있는 노드들로 이어져있는 자료구조
  - 노드를 코드로 변환하려면 ?
    - class 사용
        - Node 클래스 1개 + 연결리스트 클래스 1개
        - 생성자 함수의 인자로 data를 넣어줌

---
#### [ CODE ]
- append 메서드
  - 시간 복잡도 : O(n)
    - 중간에 삽입하는 것이 아니라 순서대로 끝에 추가하기 때문
      
    <br>

    ```jsx
    class Node{
      constructor(data){
        this.data = data;
        this.next = null;
      }
    }
    class LinkedList{
      constructor(){
        this.head = null;
      }
      append(newData){
        let newNode = new Node(newData);
        if(this.head === null){
               this.head = newNode;
               return; // list에 노드를 이미 추가했는데 더 이상 할게 없음 (함수 목적 종료)
         }
         let current = this.head; // 첫번째 노드
         while(current.next != null){
              current = current.next // current 이동 (list를 순회)
         }
         current.next = newNode; // 자기 자신을 참조 / 두번째 노드일 때 while문 걸림
      }
    }
    
    let linkedList = new LinkedList(); // 인스턴스 생성
    linkedList.append("hello");
    linkedList.append("bye");
    console.log(linkedList.head); // 첫번째 노드에 접근
    ```

- append + insert 메서드
    
    ```jsx
    class Node{
      constructor(data){
        this.data = data;
        this.next = null;
      }
    }
    
    class LinkedList{
      constructor(){
        this.head = null;
      }
      append(newData){
        let newNode = new Node(newData);
        if(this.head === null){
               this.head = newNode;
               return;
         }
         let currentNode = this.head; 
         while(currentNode.next != null){
              currentNode = currentNode.next 
         }
         currentNode.next = newNode; 
      }
    
    	insertAt(newData, index){
        let newNode = new Node(newData);
        if(index == 0){ 
          this.head = newNode; // 연결리스트의 head를 새로운 노드로 설정
        } else { // currentNode를 삽입할 인덱스 전까지 head부터 이동시켜야 함
          let currentNode = this.head; // 현재 head값을 할당
          for(let i=0; i < index-1; i++){ // 삽입하고 싶은 index 전까지 반복문을 돌려 currentNode를 이동시킴
            currentNode = currentNode.next; 
          }
          newNode.next = currentNode.next; 
          currentNode.next = newNode; // currentNode의 next가 새로운 노드를 참조하게 해서 새로운 노드를 연결리스트에 삽입
        }
      }
    }
    
    let linkedList = new LinkedList(); 
    linkedList.append("hello");
    linkedList.append("bye");
    linkedList.insertAt("Good Morning");
    linkedList.insertAt("Good Night");
    console.log(linkedList.head); // 첫번째 노드에 접근
    ```

---

#### [ Velog ]
https://velog.io/@annaleeee/%EC%9E%90%EB%A3%8C%EA%B5%AC%EC%A1%B0-%EC%97%B0%EA%B2%B0-%EB%A6%AC%EC%8A%A4%ED%8A%B8-Linked-List
  
