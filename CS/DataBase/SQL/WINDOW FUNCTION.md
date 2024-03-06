SQL에서 WINDOW FUNCTION은 데이터 집계 및 분석을 위해 사용되는 함수입니다. 이 함수들은 특정 윈도우(또는 그룹)에 대해 계산되며, 윈도우는 행의 서브셋을 나타냅니다. 일반적으로 GROUP BY와 함께 사용되지만, GROUP BY로는 해결하기 어려운 복잡한 집계 및 분석 작업을 수행할 때 유용합니다.

일반적으로 WINDOW FUNCTION은 다음과 같은 용도로 사용됩니다.

1. **집계 함수 (Aggregation Functions):** COUNT, SUM, AVG 등의 집계 함수를 사용하여 윈도우 내 데이터를 집계할 수 있습니다.
2. **순위 함수 (Rank Functions):** ROW_NUMBER, RANK, DENSE_RANK 등을 사용하여 특정 기준에 따라 결과 집합의 행을 순위로 분류할 수 있습니다.
3. **비율 및 백분율 함수 (Ratio and Percentile Functions):** CUME_DIST, PERCENT_RANK 등을 사용하여 각 행의 순위에 따른 백분율 값을 계산할 수 있습니다.
4. **이동 함수 (Window Frame Functions):** LEAD, LAG, FIRST_VALUE, LAST_VALUE 등을 사용하여 현재 행을 기준으로 이전 행이나 다음 행의 값을 가져올 수 있습니다.

이러한 WINDOW FUNCTION은 많은 데이터베이스 시스템에서 지원되며, 데이터 분석 및 비즈니스 인텔리전스 분야에서 다양한 용도로 활용됩니다.

- [[PARTITION BY]]와 [[GROUP BY]]는 의미적으로 유사하다.
- [[PARTITION BY]] 절이 없으면 전체 집합을 하나의 partition으로 정의한 것과 동일하다
- [[WINDOW FUNCTION]] 함수 적용 범위는 partition을 넘을 수 없다