### Software Stack

- OS는 HW를 application을 위해 유용한 형태로 바꾸는 SW.

### Mode
- [[User]]
- [[Kernel]]

### 프로그램이 돌면 무슨 일이 일어나는가?

- 프로그램이 instruction들을 실행한다
    - Processor가 memory로부터 instruction을 가져온다
    - Decode: 이게 뭔 instruction인지 해석한다
    - Execute: 그 instruction 실행
    - 위 단계 반복
- OS는 **프로그램을 memory에 로드한다?**
- OS는 **프로그램이 이상하게 동작할 때 이 프로그램을 끈다?**

### 많은 프로그램이 동시에 돌면 무슨 일이 일어나는가?

- 2개의 프로그램이 하나의 메인 [[Memory]]를 공유한다
    - A가 B의 데이터를 변질시킬 수 있다
    - **내 데이터가 어디 있는지 어떻게 알 수 있는가?**
- 2개의 프로그램이 processor를 소규모로 공유한다
    - **Core의 수가 program의 수보다 적으면, 어떤 프로그램이 processor를 사용할지 누가 정하는가? ⇒ OS**
    - **어느 프로그램이 무슨 core에서 도는지 누가 정하는가? ⇒ OS**

## OS: Operating System

- Program 돌리는 걸 용이하게 한다
- 프로그램간의 [[Memory]] 공유
- 장치들과 프로그램의 상호작용을 가능케 한다
- OS는 시스템이 올바르고 효율적으로 동작하게 할 책임이 있다

### Three pieces

- [[Virtualization]]
- [[Concurrency]]
- [[Persistence]]

### OS의 역할
- 리소스 할당
    - 리소스를 관리한다.
    - 리소스의 올바르고 효율적 사용을 위해 request간의 충돌을 중재한다
- Control program
    - 컴퓨터의 오용과 에러들을 막기 위해 program의 실행을 관리한다.

### System Calls
- System call은 프로그램이 OS에게 자신이 하고싶은 것을 전달하게 한다.
    - System은 OS와 Application 사이의 interface
    - Application | Systems | OS | HW

### OS와 APP간의 상호작용

![[OS_APP.png]]

![[OS_APP2.png]]

### Design Goals

- 추상화
    - 시스템을 쉽고 편리하게 만들기
- 고성능
    - OS의 업무 부담 줄여주기
    - OS는 업무 부담을 덜 느끼며 추상화를 제공하기 위해 노력해야한다
- Application 간 보호
    - Isolation
- 의존성
    - OS는 계속 돌아야 한다
- Energy-efficiency
- Security
- Mobility

### [[Data structures]]


### How to efficiently virtualize the CPU with control?
- OS는 time-sharing 기법을 통해 그 CPU 리소스를 나눠야 한다
- 이슈
    - 성능: System에 부담을 주지 않고 추상화를 구현하는 방법?
    - 관리: CPU에 대한 통제권을 유지하면서 [[Process]]를 효율적으로 돌리는 방법?