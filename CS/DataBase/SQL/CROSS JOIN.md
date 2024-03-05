Table 간 JOIN 조건이 없는 경우 생길 수 있는 모든 데이터의 조합을 말한다. 결과는 양쪽 집합의 M\*N 건의 데이터 조합이 발생한다.
Cartesian Product

예시
```
SELECT ENAME, DNAME
FROM EMP, DEPT
ORDER BY ENAME;

SELECT ENAME, DNAME
FROM EMP CROSS JOIN DEPT
ORDER BY ENAME;
```
