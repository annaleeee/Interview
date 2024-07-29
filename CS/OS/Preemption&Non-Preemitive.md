## 선점형 스케줄링 vs 비선점형 스케줄링
- 선점형 ( Preemption ) 스케줄링 <br>
  - 하나의 프로세스가 CPU를 점유하고 있을 때 다른 프로세스가 CPU를 빼앗아 차지 가능
  - 대화식 시분할 시스템이나 실시간 시스템에서 사용
    - FIFO
    - SJF
    - RR (Round Robin)
      - CPU 사용 시간을 시간 단위로 일정하게 할당
    - 우선순위
      - 에이징 기법 사용
        - 자원이 할당되기를 기다린 시간에 비례하여 우선순위를 한 단계씩 높여주는 방법
- 비선점형 ( Non-Preemitive )
  - 특정한 프로세스의 작업이 끝날 때까지 CPU를 독점하는 기법