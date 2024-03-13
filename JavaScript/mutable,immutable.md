## mutable vs immutable
: 자바스크립트 배열에 요소를 추가하는 방식
- `mutable`
    - 변할 수 있음
    - 참조타입
        - 객체의 번지를 참조하는 타입
        - 메모리 번지 값을 통해 객체를 참조하는 타입
    - 해당 데이터 주소를 찾아서 값을 변경함 <br>
        -> 원본데이터를 변화시키려는 속성
    - 배열 메서드
        - `Array.pop( )`, `Array.push( )`, `Array.splice( )`, `Array.sort( )` …
- `immutable`
    - 불변 (변할 수 없음)
    - 원시타입
        - 실제 데이터 값을 저장하는 타입 (정수, 실수, 문자 …)
    - 해당 데이터 주소와 별개의 새로운 주소에 값이 할당 <br>
        -> 원본데이터를 유지하려는 속성
    - 문자열 메서드
        - `String.slice( )`, `String.replace( )`, `String.split( )`
    - 배열 메서드 (concat)
        - `Array.concat( )` : 배열을 합쳐주는 메서드
    - spread(…) 문법
    
#### [불변성을 지켜야 하는 이유?]

- 성능 향상 위해서
    - 객체가 미래에 변할 계획이 없을 때
    - 불변성을 지키지 않으면, 데이터가 바뀌어가는 변화의 흐름을 쫓아가기 어려울 뿐더러 원본 객체를 손상시켜 예상치 못한 버그 유발 가능
    
    → 예측 가능하고 신뢰할 수 있는 코드의 발판
    
- 메모리 사용을 줄이기 위함
    - 전체 객체를 복사하지 않고 객체 참조를 만듦
- Thread-safety (스레드끼리 자원 공유할 때 안전)
    - 여러 개의 스레드가 서로 간섭하지 않고 같은 객체 참조 가능

#### [불변성을 유지하려면?]
- 불변성
    - 객체가 생성된 이후 그 상태를 변경할 수 없는 것
        - 객체의 프로퍼티를 변경할 수 없다는 것
#### - 불변성 유지 방법
1) Spread Operator (ES6)
    - `…obj`를 사용하여 obj의 모든 프로퍼티를 복사
2) Object.assign
    - `Object.assign( )`을 사용하여 obj의 모든 프로퍼티를 복사
  
    → depth가 깊어지면, 위의 방법들은 코드가 길어짐
    
    → 객체 내부의 객체는 복사되지 않음 (Shallow Copy)
    
    ⇒ immer 라이브러리를 사용하면, 복잡한 코드 없이 불변성 유지 가능
  
3) immer(immer)
    - immer의 `produce( )`를 사용하여 obj의 모든 프로퍼티를 복사
    - immer 설치
        - npm i immer
    - immer 사용
        
        ```jsx
        import produce from 'immer'; // import
        const coke = {
            name: 'coca',
            fake: {
                name: 'pepsi',
            }
        }
        
        const new_coke = produce(coke, (draft) => {
            draft.name = 'pepsi';
            draft.fake.name = 'coca';
        });
        console.log(coke.name,coke.fake.name);
        console.log(new_coke.name,new_coke.fake.name);
        
        //"coca" "pepsi"
        //"pepsi" "coca"
        ```
