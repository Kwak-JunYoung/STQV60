1. [[Free List]]를 순회하며 request를 수용할 수 있는 첫 번쨰 free chunk를 찾는다
2. Request만큼의 [[Memory]]를 사용하고 남는 건 다시 [[Free List]]에
3. 다음에 이 방식을 쓸 때 그 전에 탐색하던 지점부터 다시.

