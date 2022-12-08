### http
- HTTP(Hyper Text Transfer Protocol)란 서버/클라이언트 모델을 따라 데이터를 주고 받기 위한 프로토콜이다.
- HTTP는 애플리케이션 레벨의 프로토콜로 TCP/IP 위에서 작동한다.
- HTTP는 상태를 가지고 있지 않는 Stateless 프로토콜이며 Method, Path, Version, Headers, Body 등으로 구성된다.
- HTTP는 암호화가 되지 않은 평문 데이터를 전송하는 프로토콜이었기 때문에, 이를 해결하고자 HTTPS가 등장하게 되었다.
***
### https
- HTTPS(Hyper Text Transfer Protocol Secure)란 HTTP에 데이터 암호화가 추가된 프로토콜이다.
- 네트워크 상에서 중간에 제 3자가 정보를 볼 수 없도록 암호화를 지원하고 있다.
- HTTPS는 대칭키 암호화 방식과 비대칭키 암호화 방식을 모두 사용하고 있다.
***
### 대칭키 암호화 vs 비대칭키 암호화
1. 대칭키 암호화
- 클라이언트와 서버가 동일한 키를 사용해 암호화/복호화를 진행함
- 키가 노출되면 매우 위험하지만 연산 속도가 빠름
2. 비대칭키 암호화
- 1개의 쌍으로 구성된 공개키와 개인키를 암호화/복호화 하는데 사용함
- 키가 노출되어도 비교적 안전하지만 연산 속도가 느림
***
### http vs https
- http는 암호화가 추가되지 않았기 때문에 보안에 취약한 반면, https는 안전하게 데이터를 주고 받을 수 있다.
- https는 암호화/복호화 과정이 필요하기 때문에 http에 비해 상대적으로 속도가 느리다.
- http는 노출이 되어도 괜찮은 단순한 정보 조회 등을 처리할 때 사용한다.
- https는 개인 정보와 같은 민감한 데이터를 주고 받아야 할 때 사용한다.