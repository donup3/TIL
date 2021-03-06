### 프록시
- 클라이언트로부터 받은 요청을 다른 서버에 전송
- 서버에서 보내는 응답을 받아서 클라이언트로 보냄
- 클라이언트 <------> 프록시 서버 <-------> 오리진 서버
- 프록시서버를 여러대 사용하는 것도 가능하다.
- 서버를 경유할 때마다 via 헤더 필드에 정보를 추가한다.
- 사용하는 목적: 캐시를 사용해서 네트워크 대역등을 효율적으로 사용하기 위함, 특정 웹 사이트 접근 제한
- 종류: 캐싱 프록시, 투명 프록시

### 게이트웨이 
- 클라이언트와 http 이외의 서버 사이에 위치한다.
- 클라이언트와 게이트웨이 사이를 암호화 등 안전하게 접속함으로써 통신의 안전성을 높임
- DB에 접속해 SQL 쿼리를 사용해서 데이터를 얻는 곳, 신용카드 결제 시스템과 연계 이러한 경우에 사용한다.

### 터널 
- 클라이언트와 서버 사이에 안전한 통신로를 확립한다.


### 리소스를 보관하는 캐시
- 클라이언트가 캐시 서버에 index.html GET 요청을 보내면 캐시서버가 오리진서버에 요청을 보낸다.
- 서버에서 응답을 캐시 서버에 보내며 index.html 에 대한 응답 리소스 사본을 캐시 서버에 남겨둔다.
- 클라이언트에서 다시 index.html 요청을 보내면 캐시서버에서 바로 응답해준다. 오리진서버로 리소스의 유효성 등을 확인하러 갈 때도 있다.
- 서버가 같은 요청을 매번 반복해서 처리하지 않아도 된다.
- 리소스나캐시가 오래된 것을 캐시서버가 인식하면 오리진 서버에 가서 유효성을 판단하고 리소스를 갱신한다.