# Command 모음

- ### Window
  - Path, 환경 변수 설정 후 실행하기
    ```text
    **Path 환경 변수 설정 방법**
    고급시스템 설정 > 환경변수 > 시스템 변수 > path 에서 
    C:\Program Files\Java\jdk1.8.0_144\bin  경로 추가
    ```
  > 왜 Path 환경 변수 설정 하는가?  
  > 우리가 컴파일하고 실행하는 자바의 프로그램이 어디 있는지 알아야    
  > 그 프로그램으로 컴파일도 하고 실행도 하는 것

  - 명령어 모음 (+java)
    ```shell
    echo %path% : 현재 설정되어 있는 환경 변수를 보여준다.

    cd\ : change directory  폴더 이동 (여기서  dir 이란 폴더라고 생각하면 됨)

    md\ : make directory 폴더 생성

    dir : 디렉터리에 있는 파일과 하위 디렉터리 목록을 보여줌

    javac 파일.java : 파일.java 를 컴파일 함

    java 파일.java : 파일.java를 console에 실행함  (실행될 .class 파일이 존재 해야 되고, 파일 확장자는 생략 가능하다. 파일 확장자를 생략하는 이유 는 .class 를 명령어로 인식함)

    %(식별자)% : 식별자에 참조된 값을 불러와라

    . : 현재 directory

    . .  : 부모 directory

    move 파일명 .\폴더** :

    javac -d . (파일이름).java : 컴파일할때, 패키지가 있다면 현재 dir 안에 만들어라

    javap : 컴파일 분석 명령어 / Type 확인
    ```

- ### linux
  - 명령어 모음
    ```shell
    pwd

    cd [PATH]

    ls 

    ls -al : 숨긴파일까지 모두 보기

    mkdir [folder name] 

    rm -rf [folder name] : rf 폴더안에 다른 폴더 파일들을 순회하면서 강제로 지움

    --version : 버전 확인 (node --version , npm --version , ....)
    ```

- ### npm
  - 명령어 모음
    ```shell
    sudo npm install -g yarn  : sudo 관리자로 접근

    # package.json 있는 위치에서  (중요)
    yarn install : 목록에있는 라이브러리 모두 설치

    # Next.js 관련 커맨드
    yarn dev : default port 3000 server start
    yarn dev -p 3001 : port 3001 server start
    ```