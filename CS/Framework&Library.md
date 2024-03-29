## 프레임워크 vs 라이브러리
- 프레임워크
    - 개발자가 개발을 쉽게 할 수 있도록 뼈대 제공
    - 소프트웨어의 구체적인 부분에 해당하는 설계와 구현을 재사용이 가능하게끔 상호 협력하는 클래스와 인터페이스의 집합
    - Java - Spring / Python - Django / Android …
- 라이브러리
    - 개발에 필요한 것들을 미리 구현해놓은 도구
    - 재사용이 가능한 기능을 미리 구현해놓고 필요한 곳에서 호출하여 사용 가능하도록 만들어진 집합
    - C++ - STL / JQuery, React.js / Node.js - npm …

#### [ ‘제어 흐름’의 권한이 어디에 있는가 ]
  - 라이브러리
      - 개발자가 필요한 기능을 원할 때 호출
  - 프레임워크
      - 스스로 제어 흐름의 주도성을 가짐
      - 프레임워크가 개발자를 호출
          - 정해진 프로그램의 틀에 맞게 개발자가 필요한 기능을 입력
