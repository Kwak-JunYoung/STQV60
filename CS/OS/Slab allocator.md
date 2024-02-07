고정 크기의 미리 할당된 [[Memory]] 블록을 사용하여 [[Memory]] 할당 및 해제를 관리하는 방식입니다. 각 크기의 [[Memory]] 블록을 "Slab"이라는 단위로 관리하며, Slab은 특정 크기의 [[Memory]] 블럭을 일괄로 할당합니다.

일반적으로 다음과 같은 특징을 가집니다:
1. [[Memory]] 블록 크기에 따라 Slab을 생성하고 유지합니다.
2. 할당 요청이 들어오면 해당 크기의 Slab에서 [[Memory]] 블록을 할당합니다.
3. [[Memory]] 해제 시 [[Memory]] 블록을 다시 Slab으로 반환합니다.

Slab Allocator는 [[Memory]] 할당 및 해제를 빠르게 수행하고, 내부 단편화를 최소화합니다. 주로 운영 체제의 커널 또는 [[Memory]] 관리 시스템에서 사용됩니다.

- 자주 요청될 법한 몇 개의 object cache를 할당한다
- 그 cache가 free space가 부족하다면 더 일반적인 [[Memory]] allocator로부터 [[Memory]]를 요청한다