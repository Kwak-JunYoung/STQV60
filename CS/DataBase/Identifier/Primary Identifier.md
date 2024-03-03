[[Entity]] 내에서 각 [[Occurrence]]를 구분할 수 있는 구분자이며, 타 [[Entity]]와 참조관계를 연결할 수 있는 [[Identifier]]

### 특징
- [[유일성]]
- [[최소성]]
- [[불변성]]
- [[존재성]]

### 고려사항
- [[Primary Identifier]]에 의해 [[Entity]] 내에 모든 [[Instance]]들이 유일하게 구분되어야 한다.
- [[Primary Identifier]]를 구성하는 [[Attribute]]의 수는 유일성을 만족하는 최소의 수가 되어야 한다.
- 지정된 [[Primary Identifier]]의 값은 자주 변하지 않는 것이어야 한다.
- [[Primary Identifier]]가 지정이 되면 반드시 값이 들어와야 한다.