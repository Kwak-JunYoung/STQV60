[[Job]]을 실행하는 단위 시간

timer-interrupt 주기의 배수여야 한다.

길 때
- 장점: Context switching에 소모되는 비용을 줄일 수 있습니다
- 단점: response time 측면에서 좋지 않습니다.

짧을 때
- 장점: Response time 측면에서 강세를 보입니다
- 단점: Context switching이 자주 발생할 수 있어 이에 수반되는 비용이 많이 발생할 수 있습니다.