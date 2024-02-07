다음 정보를 내포하고 있는 [[Memory]] 공간
- Size
	- 그 [[Memory]] 덩어리의 크기
- 더 빠른 할당 해제에 쓰이는 추가적인 포인터
- Integrity 확인을 위한 magic number
	- DEADBEEF가 쓰이기도 함
	- 변경 여부를 확인하기 위함

![[Header.png]]

[[Memory]] 할당 요청이 발생하면, 그 사이즈 + header 사이즈 만큼의 빈 공간을 찾는다

