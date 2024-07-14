<details>
  <summary>Get 과 Post 방식 차이점에 대해서 설명해주세요.</summary>
  </br>
<pre>
    <table>
        <thead>
            <tr>
                <th>특징</th>
                <th>GET</th>
                <th>POST</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>데이터 전송 방식</td>
                <td>URL에 쿼리 스트링으로 전송</td>
                <td>HTTP 본문에 포함하여 전송</td>
            </tr>
            <tr>
                <td>데이터 크기 제한</td>
                <td>있음 (보통 2048자 이내)</td>
                <td>없음 (서버/브라우저 설정에 따름)</td>
            </tr>
            <tr>
                <td>보안</td>
                <td>낮음 (URL에 데이터가 노출됨)</td>
                <td>상대적으로 높음 (본문에 데이터 포함, SSL/TLS 필요)</td>
            </tr>
            <tr>
                <td>캐싱</td>
                <td>가능</td>
                <td>불가능</td>
            </tr>
            <tr>
                <td>목적</td>
                <td>데이터 조회 (Read)</td>
                <td>데이터 생성/업데이트 (Create/Update)</td>
            </tr>
        </tbody>
    </table>
</pre>
</details>

<br/>

<details>
  <summary>REST API에 대해서 설명해주세요.</summary>
  </br>
<pre>
REST API는 Representational State Transfer (REST) 아키텍처 스타일을 기반으로 한 애플리케이션 프로그래밍 인터페이스 (API)입니다. REST API는 클라이언트와 서버 간의 통신을 단순화하고, HTTP 프로토콜을 사용하여 요청과 응답을 주고받습니다.

주요 개념:
1. 자원 (Resources):
- 자원은 API가 관리하는 데이터입니다. 예: 사용자, 게시물, 제품.
- 각 자원은 고유한 URI (Uniform Resource Identifier)로 식별됩니다.

2. HTTP 메서드 (HTTP Methods):
- GET: 서버에서 자원을 조회합니다.
- POST: 서버에 새 자원을 생성합니다.
- PUT: 서버의 기존 자원을 업데이트합니다.
- DELETE: 서버에서 자원을 삭제합니다.
- PATCH: 서버의 자원을 부분적으로 업데이트합니다.

3. 상태와 무상태성 (Statelessness):
- REST API는 무상태(stateless) 방식으로 동작합니다. 각 요청은 독립적이며, 서버는 클라이언트의 이전 요청 정보를 저장하지 않습니다. 모든 필요한 정보는 요청에 포함되어야 합니다.

4. 표현 (Representation):
- 자원은 다양한 형식(JSON, XML 등)으로 표현될 수 있으며, 클라이언트와 서버 간에 데이터를 주고받을 때 사용됩니다.
- JSON이 가장 널리 사용되는 형식입니다.

5. URI 설계:
- 자원 경로를 명확하게 표현하고, RESTful 원칙에 따라 설계합니다. 예:
- 사용자 목록: GET /users
 - 특정 사용자 조회: GET /users/{userId}
 - 새 사용자 생성: POST /users
 - 사용자 업데이트: PUT /users/{userId}
 - 사용자 삭제: DELETE /users/{userId}

REST API의 장점:
- 단순성과 일관성: HTTP 프로토콜을 사용하여 클라이언트와 서버 간의 상호작용이 단순하고 일관성 있게 이루어집니다.
- 확장성: REST API는 확장성이 뛰어나고, 클라이언트와 서버가 독립적으로 개발되고 배포될 수 있습니다.
- 유연성: 다양한 형식의 데이터 전송을 지원하며, 특정 기술에 종속되지 않습니다.
</pre>
</details>