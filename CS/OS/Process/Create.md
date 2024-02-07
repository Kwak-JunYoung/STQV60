- 새로운 [[Process]]를 생성한다.
- 새로이 생성된 [[Process]]는 자신만의 [[Memory]] 공간, 레지스터, PC를 가지고 있다.

### Process
1. Program code를 [[Memory]], [[Process]]의 주소 공간에 load한다.
    - Program은 처음엔 ELF(Executable & Linkable Format)형태로 disk에 존재한다.
    - OS는 [[Process]]를 ‘게으르게’ 로드한다.
        - 코드의 조각, 데이터를 한번에 다 불러오는 게 아니라 필요할 때마다 불러옴.
        
2. Program의 run-time [[Stack]]이 할당됨
    - [[Stack]]을 argument(argc, argv)를 활용해 초기화한다
    
3. Program의 [[Heap]]이 생성됨.
    - malloc()을 통해 명백하게 요청된 동적 데이터를 위해 쓰임
    - free()를 활용하여 제거된다.
    
4. 다른 Initialization 작업을 수행한다
    - I/O setup
        - Standard input, output, error
    
5. 프로그램의 시작점인 main()부터 프로그램 돌기 시작
    - OS는 CPU의 통제권을 새로이 생성된 Process에 넘긴다