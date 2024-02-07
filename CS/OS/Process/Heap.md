프로그래머가 직접 공간을 할당([[malloc()]])/해제([[free()]]) 하는 [[Memory]] 영역

Heap의 끝 부분을 [[break]]라고 한다.

### Growing the [[Heap]]
- 대부분의 allocator는 소규모의 heap으로 시작해서 OS가 그 용량이 부족하다 판단하면 충당하는 식으로 작동한다.
![[Pasted image 20240124103202.png]]
Q) Address space상에선 인접한 공간에 [[Memory]]를 추가했는데, 왜 physical memory 상에선 떨어져있나요
A) 그냥 랜덤이다.