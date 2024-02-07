물리적 [[Memory]] byte의 배열이다

프로그램은 자신의 모든 데이터 구조를 [[Memory]]에 저장한다
- Read [[Memory]] (load)
	- 데이터에 접근할 수 있는 주소를 특정한다
- Write [[Memory]] (Store)
	- 특정된 그 주소에 쓸 데이터를 특정한다

각 [[Process]]는 자신만의 가상 [[Memory]] 주소에 접근한다
- OS는 주소 공간을 물리적 [[Memory]] 할당한다
- 하나의 돌고 있는 프로그램에서의 [[Memory]] 참조는 다른 [[Process]]의 [[Memory]] 공간에 영향을 주지 않는다.
- 물리적 [[Memory]]는 공유된다. 이는 OS에 의해서 관리된다.

Efficiency, Control을 위해 [[LDE]] 전략을 취한다.

### OS Issues for memory virtualizing
- 프로세스가 시작될 때
	- OS가 이 [[Process]]를 위해 할당할 수 있는 [[Memory]] 공간을 [[Free List]]에서 찾는다.
- [[Process]]가 종료될 때
	- [[Memory]]를 다시 [[Free List]]에서 찾는다
- Context switch가 발생할 때
	- 기존에 돌던 [[Process]]의 context([[Base register]], [[Bounds register]])를 PCB에 저장해야 한다.


