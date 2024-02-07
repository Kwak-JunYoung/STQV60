- HW는 가상 주소를 물리적 주소로 바꾼다
    - 정확히 말하면 MMU([[Memory]] Management Unit)가 함
- OS는 그 HW의 설정에 있어 특정 시점에 연루되어야 한다
    - OS는 신중한 관여를 위해 [[Memory]] 관리를 잘 해야한다?

## Example
### C언어
```
#include <stdio.h>

void func() {
	int x;
	x = x + 3;
}
```
1. [[Memory]]로부터 값을 불러온다
2. 그 값에 3을 더한다.
3. 값을 다시 [[Memory]]에 넣는다.

### Assembly code
```
128 : movl 0x0(%ebx), %eax ; load 0+ebx into eax
132 : addl $0x03, %eax     ; add 3 to eax register
135 : movl %eax, 0x0(%ebx) ; store eax back to mem
```

- x의 주소가 ebx register에 있었다고 가정하자.
1. 그 주소(ebx)의 값을 eax register로 로드 
2. eax register에 3을 더한다.
3. eax의 값을 [[Memory]]에 저장한다.

![[Address Translation Example.png]]
1. Fetch instruction at address 128
2. Execute this instruction (load from address 15KB)
3. Fetch instruction at address 132
4. Execute this instruction (no memory reference)
5. Fetch the instruction at address 135
6. Execute this instruction (store to address 15 KB)
---

## [[Base and bounds]]

### [[Address Translation on Segmentation]]

### [[Address Translation on Paging]]


 
