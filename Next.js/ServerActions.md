## Server Actions
- Server Actions
  - server action 함수를 폼 action에 입력
  - actions 파일을 만들고 import로 가져옴 (모듈 레벨 방식)
    - actions - formData를 DB에 등록 (’use server’ 사용)
      
#### [ server action을 만드는 방법 ]
- 모듈 레벨
    - server component에서 작성한 컴포넌트를 import해서 사용
- 인라인 함수 레벨

#### [ 인자로 데이터를 보내는 방법 ? ]
- 암묵적으로 폼 데이터를 전송하는 로직이 실행
- 네트워크 요청이 발생

→ form 데이터의 submit 로직을 자동화해서 대신해주는 함수
  - 자동화된건 클라이언트로 작동
