Multi-Level Feedback Queue

우선순위가 각각 다른 queue들을 다수 활용한다.
### Rules
1. Priority(A) > Priority(B)라면, A 돌린다.
2. Priority(A) == Priority(B)라면, A와 B가 [[RR]] 방식으로 같이 돈다.
3. [[Job]]이 시스템에 들어오면, 최우선 priority를 가진다.
4. CPU사용 중지 횟수와 무관하게 주어진 사용 시간을 다 소모하면, 우선순위를 낮춘다.
5. 특정 시간이 지나면, 모든 [[Job]]들이 최고 queue로 이동한다.