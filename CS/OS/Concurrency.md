### 동시성(Concurrency)의 문제

- OS는 다양한 [[Process]]를 동시에 돌린다
- 현대의 multi-threaded program들도 이 문제를 가지고 있다
- 하나의 [[Memory]]에 2개의 thread가 접근하면서, 서로 잘 번갈아가며 작동해야 하는데, 그러지 못하는 경우가 생긴다.
- 2개의 thread가 하나의 변수를 increment하는 프로그램을 돌릴 때, 100000만번 increment한다고 해서 그 결과가 100000이 되지 않는 것이 그 예시
- 만약 interrupt나 trap handling을 수행하면서 다른 interrupt가 발생한다면 OS를 통해 해결할 수 있다.
	- Interrupt processing 중에는 다른 Interrupt를 막는다
		- Queue에 적재하여 처리 대기
	- Locking scheme를 활용한다.