식별자

### 분류
- 대표성 여부
	- [[Primary Identifier]]
	- [[Alternate Identifier]]
- 스스로 생성 여부
	- [[Internal Identifier]]
	- [[Foreign Identifier]]
- 속성의 수
	- [[Single Identifier]]
	- [[Composite Identifier]]
- 대체 여부
	- [[본질 Identifier]]
	- [[인조 Identifier]]

### Identifier & Non-Identifier
|항목|식별자 관계|비식별자 관계|
|---|---|---|
|목적|강한 연결관계 표현|약한 연결관계 표현|
|자식 주식별자 영향|자식 [[Primary Identifier]]의 구성에 포함됨 |자식 일반 속성에 포함됨|
|표기법|실선 표현|점선 표현|
|연결 고려사항|- 반드시 부모 [[Entity]]에 종속<br><br>- 자식 [[Primary Identifier]] 구성에 부모 [[Primary Identifier]] 포함 필요<br><br>- 상속받은 [[Primary Identifier]] 속성을 타 [[Entity]]에 이전 필요 |- 약한 종속관계<br><br>- 자식 [[Primary Identifier]] 구성을 독립적으로 구성<br><br>- 자식 [[Primary Identifier]] 구성에 부모 [[Primary Identifier]] 부분 필요<br><br>- 상속받은 [[Primary Identifier]] 속성을 타 [[Entity]]에 차단 필요<br><br>- 부모쪽의 관계 참여가 선택 관계 |


