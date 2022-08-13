KakaoBot-SourcePuller - EunHyeokJung
======================

made by EunHyeokJung
Last Update 2022.08.14

## 이게 뭔데

> Android Noti service를 이용한 챗봇은 모바일 앱을 통해 동작하기에, 많은 챗봇 개발자들이 PC에서 코드를 작성한 후 모바일에 수동으로 옮겨야만 했습니다. 많은 개발자들이 유선으로 기기 연결, Github actions 사용 등 여러가지 방법을 제시했지만 분명하게 불편한 점이 존재했습니다.
>
> 이 챗봇은 다음 조건을 만족하면서 PC의 소스를 챗봇으로 손쉽게 옮길 수 있도록 도와줍니다.  
>- 원격으로 접근 가능
>- 세팅이 초보자에게도 어렵지 않음
>- 한번 세팅 후 유지보수가 필요하지 않음

## 동작 방식

1. 사용자가 IDE에서 ftp로 연결된 서버의 source.txt에 원하는 소스 업로드
2. 명령어로 봇기기에서 자동으로 source.txt 파일 접근 후 적용 여부 질답
3. 적용을 허가하면 지정된 챗봇에 자동 적용 및 컴파일(선택)

ex)
![image](https://user-images.githubusercontent.com/69712631/184504799-fc75ae26-ec08-4345-a5f1-638d5eb6c2ba.png)


## 명령어 목록

###### $은 입력(메시지 전송)을 나타내기 위함입니다. 명령어 접두사가 아닙니다.


### [디폴트 스크립트]

1. 디폴트 스크립트 변경

    ```
    $ hpull default abc.js
    ```
    abc.js를 디폴트 스크립트로 지정합니다.
    디폴트 스크립트는 hpull run 커맨드에 스크립트 이름을 인자로 주지 않았을 경우 사용됩니다.

2. 디폴트 스크립트 확인

    ```
    $ hpull -default
    ```
    현재 디폴트 스크립트의 이름을 확인합니다.


### [리로드(컴파일)]

1. 자동 컴파일 여부 변경

    ```
    $ hpull relaod
    ```
    소스 적용시 자동 컴파일 여부를 바꿉니다.
    ##### True일 경우 False로, False일 경우 True로 변경합니다.
    
2. 자동 컴파일 여부 변경

    ```
    $ hpull -relaod
    ```
    소스 적용시 자동 컴파일 여부를 확인합니다.


### [소스 다운로드 및 적용]

1. 소스 다운로드

    - 적용할 챗봇을 직접 지정할 때
    
    ###### '.js'는 생략할 수 있습니다.
    ```
    $ hpull run test.js
    ```
    
    ```
    서버 상태 & 스크립트 파일 확인중...
    서버 파일을 정상적으로 불러왔습니다.
    'test.js'에 적용할까요? (y/n)
    ```
   
    - 디폴트로 지정된 챗봇에 적용할 때
    
    ```
    $ hpull run
    ```
  
    ```
    서버 상태 & 스크립트 파일 확인중...
    서버 파일을 정상적으로 불러왔습니다.
    'abc.js'에 적용할까요? (y/n)
    ```
   
2. 소스 적용

    - 소스 적용 진행
    
    ```
    서버 상태 & 스크립트 파일 확인중...
    서버 파일을 정상적으로 불러왔습니다.
    'abc.js'에 적용할까요? (y/n)
    ```
    ###### UpperCase 'Y'도 사용할 수 있습니다.
    ```
    $ y
    ```
    ```
    적용이 완료되었습니다.
    자동 컴파일이 완료되었습니다.
    ```
  
    - 소스 적용 취소
    
    ```
    서버 상태 & 스크립트 파일 확인중...
    서버 파일을 정상적으로 불러왔습니다.
    'abc.js'에 적용할까요? (y/n)
    ```
    ###### UpperCase 'N'도 사용할 수 있습니다.
    ```
    $ n
    ```
    ```
    소스 적용이 취소되었습니다.
    ```


### [도움말 및 명령어 목록]

###### 전체 보기로 출력됩니다.

```
$ hpull help
```
```
KakaoBot-SourcePuller 도움말
_____________________________
전체보기                    >
```
    

