Translation Look-Aside Buffer

[[MMU]]의 한 부분

[[Page table]]의 cache 역할 수행.
- 인기 있는 PTE를 담은 곳

![[Address Translation with MMU.png]]

### Who handles the TLB Miss?
- [[CISC]]에선
	- HW가 담당한다.
	1. HW가 page table을 순회한다.
	2. 올바른 [[PTE]]를 찾는다
	3. Translation 결과를 얻는다
	4. Update를 수행한다
	5. Instruction을 재시도한다.
- [[RISC]]에선
	- SW가 담당한다
		- [[TLB]] Miss가 발생하면 SW가 exception을 발생시킨다
			- [[Trap Handler]]

[[TLB Entry]]

서로 다른 [[Process]]가 같은 Virtual Page를 다룰 때 실제로 사용하는 Physical Memory는 서로 다를 수 있는데, [[TLB]] Table 상에선 그걸 구분하기 어려울 수 있으므로, [[ASID]]에 대한 정보를 추가한다. 