- 가상 주소의 2개의 구성 요소
    
    - VPN: Virtual Page Number
    - Offset: Offset within the page
    
    ![[Virtual Address in Paging.png]]
    
    - VPN: 01 ⇒ 2nd page of VA space
    - Offset: 0101 ⇒ 5th byte
    - VPN은 [[Page table]]에 의해서 PFN으로 바뀐다(Page Frame Number)