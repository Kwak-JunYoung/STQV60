- [[TLB]]는 Fully-Associative한 방식으로 관리된다.
	- Entry가 버퍼 내부 무작위 장소에 배치될 수 있다.
- 일반적인 TLB는 32, 64, 128개의 entry를 가질 수 있다.
- HW는 모든 [[TLB]] 내부 전체를 탐색하여 원하는 translation을 탐색한다.

![[TLB Entry.png]]

Other bits
- Valid Bits
- Protection Bits
- Address-Space Identifier
- Dirty Bit

