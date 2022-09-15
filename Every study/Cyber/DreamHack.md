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

    HTTP/1.1
    
    200 OK
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








