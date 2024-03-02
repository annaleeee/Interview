## CORS (Cross Origin Resource Sharing)
- CORS
    - 교차 출처 리소스 공유
        - 웹 페이지가 제공하는 도메인이 아닌 다른 도메인에서 리소스를 요청
    - 브라우저는 CORS 에러를 발생시켜 악의적인 스크립트가 중요한 데이터에 접근하거나 무단 요청하지 못하도록 방지
#### [ 해결 방법 ]
  - 프록시 서버 설정
  - 서버에서 CORS 헤더를 추가하여 특정 도메인 요청을 허용
      - Access-Control-Allow-Origin: *
      - Access-Control-Allow-Methods: GET, POST, PUT, DELETE, PATCH, OPTIONS
      - Access-Control-Allow-Headers: Content-Type, Authorization
      - Access-Control-Max-Age: 86400
  - Chrome 확장 프로그램 ‘Allow CORS’ 사용
