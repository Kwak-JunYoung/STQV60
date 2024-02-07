[[Memory]] 할당 라이브러리가 [[Heap]]을 초기화하고 [[Free List]]를 초기화한다.

```
typedef struct __node_t {
	int size;
	struct __node_t *next;
} nodet_t;

// mmap() returns a pointer to a chunk of free space
node_t *head = mmap(NULL, 4096, PROT_READ|PROT_WRITE, MAP_ANON|MAP_PRIVATE, -1, 0);
// PROT_READ|PROT_WRITE: 읽기 쓰기 권한 부여
// MAP_ANON|MAP_PRIVATE: 익명 메모리 매핑
// -1: FD
// 0: Offset

head->size = 4096 - sizeof(node_t);
// 빼는 이유는 구조체가 block의 크기에 포함되기 떄문

head->next = NULL
```


![[Free_list_init.png]]

### Allocation
- Memory 덩어리가 요청된다면, 라이브러리가 그 요청을 수용할 수 있는 공간을 [[Free List]]에서 찾는다.
- 아래는 ptr = malloc(100)을 통해 100byte를 요청한 것.
	- 하나의 free chunk로부터 108 byte를 할당한다
	- 하나의 free chunk가 4088 byte에서 108byte 줄어든 3980byte가 된다.

![[Memory Allocation.png]]

