# Cryptography

## STAGE 1  

### `암호학`

    암호학 : 제 삼자로부터 정보를 보호하는 방법에 대한 연구.
    
    핵심 연구 주제 : 키 생성, 암호화, 복호화 


## 핵심1 : 배타적 논리합과 합동

![배타적 논리합과 합동](https://cdn.discordapp.com/attachments/956190154454876183/1021313881341186099/cf46ed2979e659ac.PNG)


### `고전 암호`

    고전 암호 : 컴퓨터와 같은 고성능 연산 장치가 발명되기 전에, 비교적 간단한 기계와 손 등으로 암복호화를 수행하던 암호를 말한다.

    * 현대는 사용을 하지는 않는다.

    고전 암호는 일반적으로 치환과 전치의 방법으로 설계가 된다.


![고전암호의 종류](https://cdn.discordapp.com/attachments/956190154454876183/1021315127464689704/unknown.png)

### `단일 문자치환 암호와 카이사르 암호`


    단일 문자 치환 암호 : 평문의 각문자를 약속이된 다른 문자로
    치환하는 암호이다. 복호화를 위해서 치환의 대응 관계는 일대일 대응이다.
    Ex) 평문의 'A'가 암호문의 'B'로 치환된다면 평문의 다른 어떤 문자도 'B'로 치환되지 않는다.


    카이사르 암호 : 평문의 각 알파벳을 일정한 거리만큼 밀어서 다른 알파벳으로
    치환하는 것이다.
    (송신자와 수신자가 몇 칸을 밀 것인지를 사전에 합의해야 통신이 이뤄질 수 있다.)

    
    카이사르 암호는 알파벳을 밀어낸 횟구만 알면 해독이 가능하다.
    알파벳은 총 26개로 가능한 키의 갯수는 26개이다.

    암호학에서 가능한 모든 키의 집합을 키 공간이라고 하는데 
    위 내용을 토대로 카이사르 암호에서 키 공간의 크기는 26으로 지정되어있다.


![수식으로 표현한 카이사르 암호](https://media.discordapp.net/attachments/956190154454876183/1021314953858273341/unknown.png)

    예시로 3번을 밀어내는 카이사르 암호를 도식화한 것.
    BEEF -> EHHI 가 된다.

![카이사르 3번 밀어냄](https://cdn.discordapp.com/attachments/956190154454876183/1021315542436552716/unknown.png)


### `춤추는 인형과 코드북 암호`



    춤추는 인형 암호처럼 모든 알파벳을 서로 다른 기호와 무작위로 일대일
    대응시켜서 치환하면 키 공간의 크기는 26!이 됩니다. (공간이 부족함)

    단점 : 언어가 지닌 통계적 특성이 유지된다.

    예로는 영어 문장에서는 e가 가장 많이 사용이 된다. 
    따라서 단일 치환 암호가 적용된 어떤 암호문에서 b가 가장 많이 등장하면
    b는 e가 치환된 것이라 추측할 수 있다.


![접근방식](https://cdn.discordapp.com/attachments/956190154454876183/1021317181797040198/unknown.png)


### `다중 문자 치환 암호`



    다중 문자 치환 암호 : 단일 문자 치환 암호와는 달리, 평문의 한 문자가
    암호문에서 여러 종류의 문자로 치환될수 있습니다.

    대표적인 다중 문화 치환 암호 : 비제네르 암호

![비네제리 표와 암호](https://cdn.discordapp.com/attachments/953086095237734421/1021320518751748116/unknown.png)


### `전치 암호`

    전치 암호 : 평문을 구성하는 문자들의 순서를 재배열하여 암호문을 만든다.


### `혼돈과 확산`


    혼돈 : 암호문에서 평문의 특성을 알아내기 힘든 성질을 말한다.
    단일 치환 암호를 사용하여 같은 평문을 두 번 암호화하면 출력된 두 암호문은 서로 같다. 
    공격자는 암호문을 보고 평문이 무엇인지 유추하지는 못하더라도 암호문을 생성한 
    두 평문이 서로 같다는 것을 알 수 있다.

    그리하여서 단일 치환 암호는 혼돈 성질을 만족하지 못하는 암호 인 것이다.

![혼돈 예시](https://cdn.discordapp.com/attachments/956190154454876183/1021418043705933824/unknown.png)

+ `HELLO WORLD 서로 다른 암호이지만 3번째 문자열을 보면`
`HELLO 가 한번 더 있는 것으로 보아서 첫번째 문자열과 같은 암호인 것을 알 수 있음`


    확산 

    1. 평문의 작은 변화가 큰 변화로 이어지는 성질임.
    2. 고전 암호에서 찾아보기 힘든 성질이다.

![확산 예시](https://cdn.discordapp.com/attachments/956190154454876183/1021418733056577536/unknown.png)


+ `위 사진을 보는 것과 같이 A -> B 하나가 바뀌었지만 전체적인 암호가`
`바뀌는 것이 가장 큰 변화중 하나이다.`


### `블록암호`


    블록 암호 : 평문을 정해진 크기의 블록 단위로 암호화하는 암호.

    Ex) 블록의 크기가 4바이트라면 평문을 4바이트의 블록을 쪼개어 
    각 블록마다 암호화를 진행한다.


![블록 암호](https://cdn.discordapp.com/attachments/956190154454876183/1021732290541404200/unknown.png)


    만약 평문의 크기가 블록 크기의 배수가 아니어서 블록으로 균등하게
    쪼갤 수 없다면, 평문뒤에 데이터를 추가하는 <<패딩>>을 수행한다.

`패딩 이란?`

    평문이 블록 크기가 배수가 될 때까지 데이터를 추가하는 것을 이야기한다.
    블록 암호의 대표적인 예시는 DES와 AES가 있다.


## `대칭키 암호 시스템의 장/단점`

    장점

    1. 공개키 암호 시스템에 비해 속도가 빠르다.


    단점

    1. 송신자와 수신자가 사전에 키를 교환을 해야만 한다.
    2. 새로운 상대와 통신할 때마다 계속 키를 생성해야만 한다.(공개키는 불편함X)



### `암호의 기능`


    1. 기밀성 : 허락된 사람만이 정보를 열람할 수 있게 하는 기능을 의미한다.
      -> 허락된 사람은 일반적으로 키를 가지고 있는 사람.


    2. 무결성 : 송신자가 보낸 정보에 변조가 일어나지 않았음을 의미한다.
      -> 가로채기, 몰래 전달하기, 변조하기 등 이러한 데이터의 변화가 X


    3. 인증 : 정보를 주고 받는 상대방의 신원을 확인하는 기능을 말한다.
      -> 예로는 공인인증서가 있으면 ID와 PW를 입력하는 것도 인증 영역에 속한다.


    4. 부인 방지 : 정보를 교환한 이후에 교환한 사실을 부인할 수 없게 하는 기능을 말함.
      -> 온라인상에서 거래가 발생했을 때 돈을 수신한 쪽에서 수신한 사실을 부인 
      할 수 있다면 온라인 거래는 불가능 할 것이다.

      


















 