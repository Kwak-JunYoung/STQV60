```
#include <stdlib.h>

void* malloc(size_t size)
```
[[Heap]]에 [[Memory]] 공간을 할당한다
- Argument
	- size_t size: [[Memory]] 블럭의 크기(byte 단위)
	- size_t는 unsigned 정수 타입
- Return
	- Success: malloc으로 할당된 [[Memory]] 블럭을 가리키는 void type pointer
	- Fail: null pointer

### 사용하는 System Call
- [[brk]]
- [[mmap]]