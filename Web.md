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