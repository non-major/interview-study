# REST API란 무엇인지 설명해주세요.

## 답변

REST API는 'REST하게 클라이언트와 서버간에 데이터를 주고받는 방식'인데, 여기서 REST란 HTTP URI를 통해 자원을 명시하고, HTTP메소드(POST, GET, PUT, DELETE)를 통해 해당 자원(URI)에 대한 CRUD Operation을 적용하는 것입니다.

### REST 원칙

1. 균일한 인터페이스(Uniform interface) : 요청이 어디에서 오는지와 무관하게, 동일한 리소스에 대한 모든 API 요청은 동일하게 보여야 합니다
2. 클라이언트-서버 디커플링(client/server decoupling) : 클라이언트와 서버 애플리케이션은 서로 간에 완전히 독립적이어야 합니다.
3. 무상태(Statelessness) : 서버 애플리케이션은 클라이언트 요청과 관련된 데이터를 저장할 수 없습니다.
4. 계층화 시스템(Layered system) : 호출과 응답이 서로 다른 계층을 통과합니다.
5. 캐시 가능성(Cacheability) : 리소스를 클라이언트 또는 서버측에서 캐싱할 수 있어야 합니다.
6. 온디맨드 코드(Code on demand) : 일반적으로 정적 리소스를 전송하지만, 특정한 경우에는 응답에 실행 코드를 포함할 수도 있습니다.

참고사이트  
https://www.ibm.com/kr-ko/cloud/learn/rest-apis
