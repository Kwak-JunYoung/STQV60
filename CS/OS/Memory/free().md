```
#include <stdlib.h>

void free(void* ptr)
```

malloc으로 할당된 [[Memory]] 공간을 풀어준다
- Argument
	- void* ptr: malloc으로 할당된 [[Memory]] 블럭을 가리키는 포인터
	- 그 크기에 대한 파라미터를 받지 않는다.
- Return
	- 없음

```
ptr = malloc(20);
```


![[malloc_result.png]]

[[Header]]에 그 용량에 대한 정보를 담고 있기에, 따로 size parameter가 필요하지 않다.


### Free space with chunks allocated
![[Free_with_chunks.png]] ![[Pasted image 20240124100852.png]]

- 예시: free(sptr)
	- 100byte의 덩어리가 다시 [[Free List]]로 들어간다
	- [[Free List]]는 작은 덩어리부터 시작될 것

![[Pasted image 20240124101818.png]]




