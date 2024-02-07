```
#include <stdlib.h>

void *calloc (size_t num, size_t size)
```

[[Heap]]에 [[Memory]]를 할당하고 리턴 전에 0으로 초기화
- Argument
	- size_t num: 할당할 블럭의 수
	- size_t size: 각 블럭의 크기
- Return
	- Success: calloc으로 할당된 [[Memory]] 공간을 가리키는 void type pointer
	- Fail: null pointer

