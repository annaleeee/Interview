## 인터럽트 ( Interrupt )
- 인터럽트
  - 정상적인 프로그램 실행 도중에 방해하여 일시 중단하고, 발생된 상황을 처리한 후 실행중이던 작업으로 복귀하여 계속 처리함
- 종류 ( 크게 외부, 내부로 나뉨 )
  - 외부 인터럽트
      - 전원 이상, 입출력 인터럽트, 기계 착오 …
      - 자원 할당 시간이 끝난 경우
  - 내부 인터럽트
      - 잘못된 명령이나 잘못된 데이터를 사용할 때 발생
      - 프로그램 검사 인터럽트
      - 하드웨어 고장
  - 소프트웨어 인터럽트
      - 프로그램 처리 중 명령의 요청에 의해 발생
      - 감시 프로그램인 SVC (SuperVisor Call) 호출
        
#### [ 동작 순서 ]
  - 인터럽트 요청 → 프로그램 실행 중단 → 현재 프로그램 상태 보존 → 인터럽트 처리루틴 실행 → 인터럽트 서비스 루틴 실행 → 상태복구 → 중단된 프로그램 실행 재개
