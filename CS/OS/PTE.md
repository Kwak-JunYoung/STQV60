[[Page table]] Entry

[[Page table]]의 각 항목.

### Common Flags of [[PTE]]
- Valid Bit
	- 해당 [[PTE]]가 유효한지 여부를 나타냄.
- Protection Bit
	- r, w, x 권한에 대한 정보를 담음
- Present Bit
	- 이 Page가 Disk에 있는지 물리적 [[Memory]]에 있는지 나타냄.
- Dirty Bit
	- 이 Page가 [[Memory]]로 불려온 이래로 수정된 적이 있는지 나타냄.
- Reference Bit(Accessed Bit)
	- 이 Page가 접근된 적 있는지 나타냄

![[x86 PTE.png]]
An x86 PTE

- P: Present Bit
- R/W: Read/Write Bit
- U/S: Supervisor
- A: Accessed Bit
- D: Dirty Bit
- PFN: Page Frame Number
- PWT, PCD, PAT: 생략

