## interface vs type
- interface
  - extends 키워드를 이용하여 확장
  - 선언적 확장 가능
    - 같은 이름의 interface를 선언하면, 자동으로 확장
  - 객체의 타입 설정할 때 사용, 원시 자료형에는 사용 불가능
  - computed property name 사용 불가능
    - 단순히 타입 검사 및 추론을 위한 목적으로 사용되기 때문에
- type
  - & 기호를 이용해서 확장
  - 선언적 확장 불가능
  - 단순한 원시값, 튜플, 유니온 타입 선언 시 사용하는 것이 좋음
  - computed property name 사용 가능
  
