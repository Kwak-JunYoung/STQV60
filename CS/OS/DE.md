Direct Execution

|OS|Program|
|---|---|
|1. Process list에 접근을 위한 entry 생성||
|2. Program을 위한 memory 할당||
|3. Memory에 program 로드||
|4. Stack을 argc/argv argument를 활용해 설정||
|5. Register 비우기||
|6. main() 실행||
||7. main() 실행|
||8. main()에서 return|
|9. Process의 memory free||
|10. Process를 process list에서 제거||