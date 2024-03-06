- 일반적으로 RATIO_TO_REPORT(A) OVER(PARTITION BY B)라고 하는데, 그럼 그 row의 A가 B로 group by했을 때 어느정도 비율에 속하는지 나타냄.

| Region | Revenue |
| ------ | ------- |
| A      | 500     |
| B      | 700     |
| C      | 800     |
| D      | 600     |
```SQL
SELECT Region, Revenue,
       RATIO_TO_REPORT(Revenue) OVER () AS Revenue_Ratio
FROM Sales;
```

| Region | Revenue | Revenue_Ratio    |
| ------ | ------- | ---------------- |
| A      | 500     | 0.192 (500/2600) |
| B      | 700     | 0.269 (700/2600) |
| C      | 800     | 0.308 (800/2600) |
| D      | 600     | 0.231 (600/2600) |
