그룹화 컬럼들에 대한 개별적 집계 및 소계를 생성해주는 함수.
- 각 컬럼별 [[GROUP BY]] 집계가 필요한 경우 [[GROUP BY]]를 여러번 [[UNION ALL]] 할 필요 없이 한 번의 [[GROUP BY]]로 생성 가능
- [[ROLLUP]] 처럼 계층형 구조가 아닌 수평적 구조이지만 사용하기에 따라 [[ROLLUP]]과 같은 결과 도출 가능
-  NULL 값을 포함한 별도의 행이 추가되지 않습니다.

###### 예시
```
GROUPING SETS(SALE_DT)
SALE_DT에 대한 집계 생성 (GROUP BY문에 SALE_DT만 사용한 것과 결과 같음)

GROUPING SETS(SALE_DT, ITEM_NM)
SALE_DT에 대한 집계, ITEM_NM에 대한 집계 생성

GROUPING SETS(SALE_DT, ())
SALE_DT에 대한 소계(총계) 생성
```

