# Node.js 프로그래밍 기초

### 노드로 만들 수 있는 대표적인 서버와 용도

-   서버는 왜 필요할까?

        API란 프로그램을 쉽게 제작할 수 있게 미리 만들어 놓은 것들의 모음이다.
        다른 곳에 있는 단말에 데이터를 달라고 요청하는 프로그램을 클라이언트라고 한다.
        다른 곳에서 요청받은 명령을 처리해 주는 프로그램을 서버라고 한다.
        프로토콜이란 데이터를 서로 어떤 형태로 주고받을 것인지를 정한 것으로 간단하게 데이터의 형태라고 생각하면 된다.


-   대표적인 서버 유형은 어떤 것이 있을까?

        채팅 서버
        위치 기반 서비스 서버
        모바일 서버
        JSON-PRC 서버
        웹 서버

-   웹 서버의 기능은 무엇일까?

        웹 문서 조회
        파일 업로드, 다운로드
        로그인, 회원가입

-   채팅 서버의 중요한 기능은 무엇일까?

        친구 목록 보여주기
        일대일 채팅하기
        그룹 채팅하기

-   JSON-RPC 서버의 중요한 기능은 무엇일까?

        서버 쪽에 함수를 만들어 두고 클라이언트에서 함수를 호출하듯이 데이터를 요청하면 응답하는 서버이다.
        JSON은 어떤 형식으로 데이터를 주고 받을지를 정해 노은 표준 데이터 포맷이다.
        RPC 방식으로 데이터를 주고 받는다.
        데이터를 요청하고 응답을 받아 처리하는 데 에이잭스 방식이 아닌 JSON-RPC를 사용하기도 한다.
                웹에서 데이터 요청
                앱에서 데이터 요청

-   위치 기반 서비스 서버의 중요한 기능은 무엇일까?

        데이터 요청
        가까운 위치 찾기
        영역 내의 위치 찾기

-   모바일 서버의 중요한 기능은 무엇일까

        모바일 웹으로 사이트 열기
        단말 정보관리하기
        공지 메시지 받기

### 노드에 대해 알아보고 개발 도구 설치하기

-   노드란 무엇일까?

        노드는 자바스크립트를 이용해서 서버를 만들 수 있는 개발 도구입니다.
        하나의 요청 처리가 끝날 때까지 기다리지 않고 다른 요청을 동시에 처리할 수 있는 비동기 입출력 방식을 적용했다.
        프로그램에서 해당 파일의 내용을 처리할 수 있는 시점이 되면 콜백함수가 호출된다.
        먼저 메이인이 되는 자바스크립트의 파일의 일부 코드를 떼어 별도의 파일로 만들 수 있는데 이것을 모듈이라고 부른다.

                다음과 같은 특징을 갖느다.
                모듈과 패키지
                비동기 입출력
                이벤트 기반 입출력

-   개발 도구 설치하기

        브라켓 설치
        크롬 브라우저 설치
        노드 설치

### 노드 간단하게 살펴보기

- 첫 번재 노드 프로젝트 만들기

        자바스크립트 파일 만들어 실행하기
        브라켓의 확장 기능 설치하고 브라켓에서 노드 프로그램 실행하기
        노드 셸에서 직접 코드 입력하고 실행하기

- 콘솔에 로그 뿌리기

        콘솔 객체는 전역 객체라고 부르며 필요할 때 코드의 어느 부분에서나 사용할 수 있다.
                console : 콘솔창에서 결과를 보여주는 객체
                process : 프로세스의 실행에 대한 정보를 다루는 객체
                exports : 모듈을 다루는 객체

- 프로세스 객체 간단하게 살펴보기

        argv : 프로세스를 실행할 때 전달되는 파라미터 정보
        env : 환경 변수 정보
        exit() : 프로세스를 끝내는 메소드

- 노드에서 모듈 사용하기

        export에는 속성을 추가할 수 있어 여러개의 변수나 함수를 각각의 속성으로추가할 수 있다.
        module.exports는 하나의 변수나 함수 또는 객체를 직접 할당한다.
        다른 사람이 만들어 둔 모듈을 외장 모듈이라고 한다.

- 간단한 내장 모듈 사용하기

        미리 포함되어 있는 모듈을 내장 모듈이라고하며, 개발자가 직접 만들어 올린 모듈을 외장 모듈이라고 한다.
        외장 모듈은 npm으로 설치해야 하지만 내장 모듈은 바로 사용할 수 있다.
                os 모듈
                        hostname 
                        totalmem 
                        freemem
                        cpus 
                        networkinterfaces
                path 모듈
                        join 
                        dirname 
                        basename 
                        extname

### 노드의 자바스크립트와 친해지기

- 자바스크립트의 객체와 함수 이해하기
        자바나 C언어와 같은 타입 기반의 언어는 메모리를 절약하기 위해 정수와 문자열을 만들 때 다른 크기의 변수 상자를 만들고 변수 앞에 형을 지정한다.
        자바스크립트는 모든 변수를 var 키워드로 선언하고 사용한다.
                자바스크립트 자료형
                        Boolean
                        Number
                        String
                        undefined
                        null
                        Object
        객체 안에 들어 있는 속성의 이름은 하나의 변수로 생각할 수 있으며, 변수의 이름과 변수 값 또는 속성의 이름과 속성 값이라는 형태로 조합됩니다.
        함수를 변수에 할당하는 과정에서 함수의 이름이 삭제되어 function 키워드 뒤에 곧바로 소괄호가 붙는 형태로 만들어지는데 이것을 익명함수라고 한다.
        함수를 익명 함수로 변수에 할당할 때는 함수를 선언하는 선언문이 아니라 일반 수식처럼 표현식이 되므로 가장 마지막에 세미콜론을 붙여 주는 것이 좋다.
        
- 배열 이해하기 
        배열은 여러 개의 데이터를 하나의 변수에 담아 둘 수 있어서 자주 사용되며, 배열 안에 들어 있는 요소들은 대괄호를 이용해서 접근할 수 있다.
        for문과 foreach 문 사용이 가능하다.
                배열 속성/메소드
                        push
                        pop
                        unshift
                        shift
                        splice
                        slice

- 콜백 함수 이해하기
        
        자바스크립트의 변수에는 숫자나 문자열 같은 데이터, 그리고 중괄호를 이용해 만든 객체뿐 아니라 함수도 할당할 수 있다.
        함수를 파라미터로 전달하는 경우는 대부분 비동기 프로그래밍 방식으로 코드를 만드는 것이다.
        파라미터로 전달되는 함수를 콜백함수라고 한다.
        콜백 함수는 함수가 실행되는 중간에 호출되어 상태 정보를 전달하거나 결과 값을 처리하는데 사용된다.
        함수 안에서 새롱룬 함수를 만들어 반환하는 경우에는 예외적으로 변수 접근을 허용하는 데 이것을 클로저라고 부른다.

- 프로토타입 객체 만들기
        
        함수에 여러가지 기능과 속성이 추가되면서 객체 지향 언어에서 객체의 원형인 클래스를 만들고, 그 클래스에서 새로운 인스턴스 객체를 여러 개 만들어내듯이 자바스크립트에서도 객체의 원형을 정의한 후 그 원형에서 새로운 인스턴스 객체를 만들어 낼 수 있습니다.
        함수 중에서 new 연산자로 호출되는 함수는 객체를 만들기 위한 함수로 분류되며, 이러한 함수를 생성자라고 한다.
        새로운 인스턴스 객체를 만들도록 정의한 객체를 프로토타입 객체라고도 부르는데, 일반저긴 함수와 구별해서 이해할 수 있어야 한다.


### 노드의 기본 기능 알아보기

- 주소 문자열과 요청 파라미터 다루기
        
        parse() : 주소 문자열을 파싱하여 URL 객체를 만들어 줍니다.
        formate() : URL 객체를 주소 문자열로 변환합니다.
        URL 객체의 속성을 보면 주소 문자열의 여러 가지 정보가 포함되어 있다.
        stringfy() : 요청 파라미터 객체를 문자열로 변환합니다.

- 이벤트 이해하기

        on(evnet,listener) : 지정한 이벤트의 리스너를 추가
        once(event, listener) : 지정한 이벤트의 리스너를 추가하지만 한 번 실행한 후에는 자동으로 리스너가 제거
        removeListener(envet, listener) : 지정한 이벤트에 대한 리스너를 제거

- 파일 다루기
        파일을 읽어 들이거나 쓰기
                
                fs 모듈을 사용한다.
                readFile(filename, enconding, callback)
                readFileSync(filename, encoding)
                writeFile(filename, data, encoding='utf', callback)
                writeFileSync(filename, data, encoding='utf8')

        파일을 직접 열고 닫으면서 읽거나 쓰기
                
                open(path, flags, mode, callback)
                read(fd, buffe, offset, length, position, callback)
                write(fd, buffer, offset, length, position, callback)
                close(fd, callback)
                flag : r, w, w+, a+

        버퍼 객체 사용하는 방법 알아보기
                
                toString() : 문자열을 확인
                isBuffer() : 버퍼인지 확인
                copy() : 버퍼 객체 복사
                concat() : 두개의 버퍼를 하나로 붙여서 새로운 버퍼 객체를 만들 때
                
        스트림 단위로 파일 읽고 쓰기        
                
                createReadStream(path, options)
                createWriteStream(path, options)

        http 모듈로 요청받은 파일 내용을 읽고 응답하기
                
                스트림을 서로 연결하는 방법은 웹 서버를 만들고 사용자의 요청을 처리할 때 유용하다.        

        fs 모듈로 새 디렉터리 만들고 삭제하기
                
                fs 모듈은 그 밖에도 파일과 디렉터리를 다루는 여러 가지 메소드를 포함하고 있다.
                mkdir
                rmdir

        로그 파일 남기기
                여러 가지 로그 모듈 중에서 winston 모듈로 로그를 남기는 방법이 있다.     
                winston 모듈로 만드는 로거는 transport라는 속성 값으로 여러 개의 설정 정보를 전달할 수 있다.
                

                
