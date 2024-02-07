[[Job]]이 I/O 작업을 요청하면
- [[Job]]은 그 작업이 끝 날 때까지 [[Blocked]] 상태가 된다.
- [[Scheduler]]는 CPU에 다른 [[Job]]을 스케쥴 해야한다.

I/O가 끝나면
- [[Interrupt]]가 발생한다.
- [[Process]]가 [[Blocked]]에서 [[Ready]] 상태가 된다.