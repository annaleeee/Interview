## Decorator
- 데코레이터
  - 데코레이터는 함수로, @expression 선언문과 함께 사용
  - 클래스 선언, 메서드, 접근자, 프로퍼티 또는 매개변수에 첨부할 수 있는 특수한 종류의 선언
  - @로 시작하는 데코레이터를 선언하여 장식하면 코드가 실행( 런타임 )이 되면 데코레이터 함수가 실행되어, 장식한 멤버를 보다 강력하게 만들어 줌
  - 데코레이터 함수에는 target ( 현재 타겟 ), key ( 속성 이름 ), descriptor ( 설명 ) 전달
    - 단, 어떤 멤버를 장식했느냐에 따라 인수가 달라짐
      
  - 메소드나 클래스 인스턴스가 만들어지는 런타임에 실행됨 <br>
       ⇒ 매번 실행되지 않음
  
  - 정식 지원하는 문법이 아닌 실험적인 기능임 <br>
      → 사용하기 위해, tsconfig.json 파일에서 experimentalDecorators 속성 추가해주어야 함

  ```
    // tsconfig.json 
    {
      "compilerOptions": {
        "experimentalDecorators": true
      }
    }
  ```
