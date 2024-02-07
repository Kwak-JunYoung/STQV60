```
#include <stdlib.h>

void *realloc(void *ptr, size_t size)
```

[[Memory]] 블럭의 사이즈를 변경한다
- Argument
	- void* ptr: malloc, calloc, realloc을 통해 할당된 [[Memory]] block을 가리키는 Pointer
	- size_t size: 그 [[Memory]] 블럭의 새로운 사이즈 (byte 단위)
- Return
	- Success: 그 [[Memory]] 블럭을 가리키는 void type pointer
	- Fail: Null pointer