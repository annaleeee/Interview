## React-Query
#### [ 공식문서 ]
- fetching, caching, 서버 데이터와의 동기화를 지원해주는 라이브러리’
  - fetching
    - 데이터를 서버로부터 가져오는 중인지를 나타내는 상태
      - 비동기 데이터를 요청하고 받아오는 동안의 상태를 추적하는 데 사용됨
  - caching
    - 특정 데이터의 복사본을 저장하여 이후 동일한 데이터의 접근 속도를 높임
      - 서버의 부담을 줄여줌
     
- React-Query
  - React 애플리케이션에서 비동기 데이터를 효과적으로 관리하기 위한 도구
    - React 애플리케이션에서 데이터를 관리하고 처리하기 위한 라이브러리
  - 데이터를 불러오고 캐싱하며, 서버 데이터와의 동기화 및 업데이트 하는 작업을 개발자가 쉽고 간단하게 할 수 있도록 도와주는 라이브러리
  - 데이터 캐싱, 리프레시 로직, 에러 핸들링과 같은 기능들을 내장하고 있어서 데이터 관리 코드를 단순화하고 중복을 최소화 함

#### [ 장점 ]
- 캐싱
- get을 한 데이터에 대해 update를 하면 자동으로 get을 다시 수행
- 데이터가 오래 되었다고 판단하면 다시 get
- 동일 데이터를 여러 번 요쳥할 경우, 한 번만 요청함
- 무한 스크롤 (Infinite Queries)
- react hook과 사용하는 구조가 비슷함
- 비동기 과정을 선언적으로 관리할 수 있음
