- 주소공간을 page라는 단위로 쪼개는 것
	- [[Segmentation]]과의 차이
	- Page는 고정된 단위, [[CS/OS/Segment]]는 그 크기가 다양함
	- Page는 물리적 단위, [[CS/OS/Segment]]는 논리적 단위.
- 물리적 [[Memory]] page frame으로 쪼개진다
- Virtual Address를 Physical Address로 번역하기 위한 [[Page table]]이 [[Process]]마다 필요하다

### Advantages of paging
- Flexibility
	- 주소 공간의 추상화를 효과적으로 지원한다.
- Simplicity
	- Free-space를 관리하기 쉬워진다.
		- [[Free List]]를 유지보수 하기 쉽다.

### [[Address Translation on Paging]]

### [[Paging is too slow]]

