- 데이터를 연속적인 비트 스트림으로 처리하는 암호화 기술.
- 평문(plain text)의 각 비트를 순차적으로 처리하여 암호문(ciphertext)을 생성하며, 이 과정에서 비트별로 키를 사용하여 변환을 수행.
- **장점**
	- 스트림 암호화는 빠른 속도와 실시간 처리가 가능함
	- 비트 단위로 데이터를 처리하기 때문에 작은 메모리와 처리 능력을 요구함.
- **단점**
	- 키 스트림이 사전에 미리 생성되어야 함
	- 키 스트림의 재사용이 보안상 위험할 수 있으므로 키 스트림의 안전한 관리가 필요함.
- 통신 프로토콜이나 데이터 스트리밍에서 주로 사용됨.

- [[LFSR]]
- [[RC4]]
- [[ChaCha20]]
