SQL에서 `LAG` 함수는 동일한 결과 집합 내에서 이전 행의 데이터에 접근할 수 있는 윈도우 함수입니다. 특히 결과 집합 내에서 이전 행의 값을 가져오는 기능을 제공합니다.

`LAG` 함수의 구문은 다음과 같습니다:

```sql
LAG(컬럼_이름, 오프셋, 기본값) OVER (파티션_절 ORDER BY 정렬_절)
```

- `컬럼_이름`: 이전 행의 값을 가져오려는 열입니다.
- `오프셋`: 현재 행으로부터 이전 값을 찾기 위해 뒤로 이동해야 할 행의 수입니다. 이는 선택적인 매개변수이며 기본값은 1로, 이전 행을 의미합니다.
- `기본값`: 이전 행이 없을 경우 반환할 값을 지정합니다. 지정하지 않으면 기본적으로 `NULL`이 반환됩니다.
- `파티션_절`: (선택적) 결과 집합을 그룹으로 나누는 방법을 지정합니다.
- `정렬_절`: 각 파티션 내의 행 순서를 지정합니다.

다음은 `LAG` 함수의 사용 예시입니다:

예를 들어 `date`와 `revenue` 열을 가진 `sales` 테이블이 있고, 각 날짜별 매출 감소율을 계산하려고 합니다:

```sql
SELECT 
    date,
    revenue,
    LAG(revenue) OVER (ORDER BY date) AS prev_day_revenue,
    revenue - LAG(revenue) OVER (ORDER BY date) AS revenue_decrease
FROM 
    sales;
```

이 쿼리는 날짜, 매출액, 이전 날의 매출액(`prev_day_revenue`), 그리고 하루 동안의 매출 감소량(`revenue_decrease`)을 반환합니다.