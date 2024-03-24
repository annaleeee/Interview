## require vs import
** 모듈 키워드 : 외부 파일이나 라이브러리를 불러올 때 사용하는 키워드
- require
  - node.js에서 사용하고 있는 CommonJS
  - 파일에 들어있는 곳에 남아 있음
      - 프로그램의 어느 지점에서나 호출 가능

  ```tsx
  /* CommonJS  */
  const name = require('./module.js');
  ```

- import
  - ES6( ES2015 )에서 도입된 키워드
  - 항상 맨 위로 이동
      - 파일 시작 부분에서만 실행 가능
  - 사용자가 필요한 모듈 부분만 선택하고 로드
      - require 보다 성능이 우수하고 메모리 절약 가능
