- 하나의 queue에 스케쥴되어야 하는 모든 [[Job]]들을 집어넣는다.
- CPU가 그 하나의 queue로부터 다음에 실행되어야 할 [[Job]]을 고른다.
- 문제점
	- Scalability
		- CPU가 Queue에 접근할 때 lock을 걸고 접근해야 다른 CPU와 사고가 발생하지 않는다.
	- [[Cache Affinity]]
		- 이것을 보전하는 것으로 성능 향상을 꾀할 수 있으나, 구현하는 것은 까다롭다

