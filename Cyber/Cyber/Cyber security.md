# Cyber Security


 www의 시작(해킹과 보안)

 
# Enquire (Enquire Within upon Everything)

    Enquire 실패한 이유 !!!

    1. 기존 데이터베이스에 대한 외부 링크가 허용 x
    2. 정보를 최신 상태로 유지하는 것에 대해 너무 많은 리소스가 들었음.

# HTTP URL HTML 정의

    HTTP : HTML 문서와 같은 리소스들을 가져올 수 있도록 해주는 프로토콜
    모든 데이터 교환의 기초 클라이언트-서버 프로토콜

    URL : 네트워크 상에서 자원이 어디 있는지를 알려주기 위한 규약

    HTML : 웹 페이지를 위한 지배적인 마크업 언어
    제목, 단략, 목록 등과 같은 본문을 위한 구조적 의미를 나타내는 것뿐만 아니라 링크, 
    인용과 그 밖의 항목으롷 구조적 문서를 만들 수 있는 방법을 제공


##  HTTP Header의 구조

    GET/HTTP/1.1 

    Host:www.naver.com -> 

    Accept:text/html,*/*;

    User-Agent: Mozilla/5.0(Window Nt 6.1) AppleWebKit/537.36
    
    Referer : http://www.naver.com/

## Web Proxy Tool 이란?

    -현재 사용하고 있는 브라우조와 서바 간의 통신을 할 때 중간에 위치해서 
    브라우저(클라이언트)가 요청하고 받는 데이터를 서버로 재전송을 해주는 역할을 함


# 디지털포렌식 개요

디지털포렌식 과정

    1. 사전 준비 
    2. 증거 수집 
    3. 포장 및 이송 
    4. 분석 및 검토 
    5. 보고서 작성


# 운영체제 아티팩트

    주요 운영체제 : Microsoft, Linux, Mac OS

    
    파일시스템 로그(Filesystem Log)
    -> File I/O, 트랜잭션 등에 의해 발생.


    웹 아티팩트(Web Artifact)

    1. History 
    2. Cache
    3. Cookie
    4. Download File List
    
    
    레지스트리(Registry)

    -> 운영체제 설정 정보 등에 대한 마이크로소프트에서 개발한 데이터 베이스


    이벤트로그(Event Log)
    -> Window 운영체제 구성요소 감사 설정된 시스템의 모든 기록/데이터


# 파일 시스템 포렌식

    파일 시스템의 종류 : 디스크 | 네트워크 | (특수 용도의 파일 시스템)

    디스크 파일 시스템 : 자료 기억 장치, 특히 컴퓨터에 연결된 
    디스크 드라이브에 파일을 저장하도록 설계된 시스템이다.

    <NTFS>


    1. MBR(BR) Master Boot Record

    - 파티션 정보를 포함하는 영역
    - 파티션이 나뉘어진 경우만 존재
    - 디스크 0번 섹터(512Byte)에 위치

    <3가지 단위로 나뉨>

    Boot Code -> (446Btye)
    Partition Table Entry -> (16 x 4 = 64Byte)
    Signature -> (28Byte)


    2. VBR (Volume Boot Record)

    - 볼륨 영역의 시작위치에 존재 
    - 해당 볼륨 파일시스템의 메타데이터(저장), 부트로더 포함한다.


    3. MFT (Master File Table)

    - 파일 위치, 속성, 시간정보, 이름, 크기 등의 메타데이터 저장
    - 파일, 디렉토리 수에 따라 동적할당


# 메모리 포렌식(임시저장)

    휘발성 -> RAM 공간으로 이동.

    - Process
    - Networking
    - Logon
    - Resource
    - ClipBoard
    - File_Object

    프로세스 메모리 영역을 정해진 포맷에 따라서 저장을 한다.





    










    

    



    
    
    
    








