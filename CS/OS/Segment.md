특정 길이를 가진 주소 공간의 일정 부분
- [[Stack]], [[Heap]], [[Code]] 등이 이에 해당.
- 각각 [[Base]], [[Bounds]]가 있음

### Referring to Segment
- Explicit approach
	- 주소 공간을 가상 주소의 MSB 몇 개를 기준으로 나눈다.
	- ![[Segment&Offset.png]]

### Referring to [[Stack]] segment
- [[Stack]]는 반대로 자란다.
- HW가 특정 segment가 어떤 방향으로 자라는지 확인한다.
- 1: 정방향
- 0: 역방향

| Segment | Base | Size | Grows Positive? |
| --------- | ----- | ---- | ---------------- |
| Code | 32K | 2K | 1 |
| Heap | 34K | 2K | 1 |
| Stack | 28K | 2K | 0 |

### Support for sharing
- Segment는 주소 공간끼리 공유될 수 있다
- 이를 위해 HW의 지원 하에 Protection bit을 사용한다
    - r, w, x를 나타냄
