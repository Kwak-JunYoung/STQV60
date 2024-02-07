- 각 application이 자신만의 리소스가 있다고 “착각”하게 한다

- [[OS]]가 physical resource(Processor, [[Memory]], disk, …)를 가지고 그것을 추상화한다.
    - 추상체는 일반적이고, 강하며, 쓰기 쉽다
    - [[OS]]를 virtual machine이라고 표현하기도 한다.

- Application은 HW에 직접 접근할 수 없다
    - 추상화된 HW에만 접근하는 것
    - [[OS]]는 application과 HW사이에 위치하여 중개자 역할을 한다.

### CPU 추상화

- System은 다수의 가상 CPU를 가지고 있다
    - 하나의 CPU를 무한의 가까운 수의 CPU처럼 보이게 한다.

    - 많은 프로그램이 동시에 작동하는 것처럼 보이게 한다.
        - 이것이 추상화(virtualization)