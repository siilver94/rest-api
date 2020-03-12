# Project : Rest API

## 프로젝트 소개


웹으로 간단한 질답을 낼 수 있는 형태를 **restAPI** 를 사용하여 **Restful** 하게 **PostMan(clinet)**, **JAVA(server)** 를 사용하여 만들기.


## Rest API 란?


- REST API에 REST는 Representational State Transfer의 약자로 소프트웨어 프로그램 아키텍처의 한 형식입니다.

- REST api의 등장은 2000년도에 HTTP의 주요 저자 중 한 사람인 로이 필딩이 그 당시 웹(HTTP) 설계의 우수성에 비해 제대로 사용되어지지 못하는 모습에 안타까워하며 웹의 장점을 최대한 활용할 수 있는 아키텍처로써 REST를 발표 하였습니다.

- REST is non – standard.

- RESTful WebService : REST 규칙을 따르는 웹 서비스 구현 방식 입니다.

- 현재의 아키텍쳐가 웹의 본래 설계의 우수성을 많이 사용하지 못하고 있다고 판단했기 때문에, 웹의 장점을 최대한 활용할 수 있는 분산 하이퍼미디어 시스템(예:웹) 을 위한 아키텍쳐 스타일의 API 입니다.

- HTTP 통신에서 어떤 자원에 대한 CRUD 요청을 Resource와 Method로 표현하여 특정한 형태로 전달하는 방식 입니다.

## Architecture Style 이란?

제약 조건들의 집합이고 이것들을 모두 지켜야 REST 를 따른다 라고 할 수 있다.
REST 는 아키텍쳐 스타일이면서 동시에 하이브리드 아키텍쳐 스타일임, 아키텍쳐 이면서 아키텍쳐의 집합이기 때문이다.


### RESTful 하기위한 아키텍쳐 제약 조건

- **client-server(서버-클라이언트 구조)**: Rest API에서 자원을 가지고 있는 쪽이 서버, 자원을 요청하는 쪽이 클라이언트에 해당합니다. 서버는 API를 제공 합니다.

- **Stateless,(무상태성 서버)** : Rest API는 세션정보나 쿠키정보를 활용하여 작업을 위한 상태정보를 저장 및 관리하지 않습니다. 이러한 무상태성때문에 Rest API는 서비스의 자유도가 높으며, 서버에서 불필요한 정보를 관리하지 않으므로 구현이 단순합니다. 이러한 무상태성은 서버의 처리방식에 일관성을 부여하고, 서버의 부담을 줄이기 위함 입니다.

- **Cacheable(캐시 가능)** : Rest API는 결국 HTTP라는 기존의 웹표준을 그대로 사용하기 때문에, 웹의 기존 인프라를 그대로 활용할 수 있습니다. 그러므로 Rest API에서도 캐싱 기능을 적용할 수 있는데, HTTP 프로토콜 표준에서 사용하는 Last-Modified Tag 또는 E-Tag를 이용하여 캐싱을 구현할 수 있고, 이것은 대량의 요청을 효율적으로 처리할 수 있게 도와줍니다.

- **uniform interface(일관된 인터페이스)** :  Resource(URI)에 대한 요청을 통일되고, 한정적으로 수행하는 아키텍처 스타일을 의미합니다. 이것은 요청을 하는 Client가 플랫폼(Android, Ios, Jsp 등) 에 무관하며, 특정 언어나 기술에 종속 받지 않는 특징을 의미합니다. 이러한 특징 덕분에 Rest API는 HTTP를 사용하는 모든 플랫폼에서 요청 가능하며, Loosely Coupling(느슨한 결함) 형태를 갖게 되었습니다 .

- **self-descriptive messages(메시지가 스스로를 설명 주소나, content type 필요)** : Rest API는 요청 메세지만 보고도 이를 쉽게 이해할 수 있는 자체 표현 구조로 되어있습니다. 아래와 같은 JSON 형태의 Rest 메세지는 http://localhost:8080/insertBoardInfo 로 게시글의 제목, 내용을 전달하고 있음을 손쉽게 이해할 수 있습니다.   *(요즘 rest 에서 거의 모두 지키지 못하고 있음.)

- **Hypermedia as the engine of application stat(HATEOAS)** : 애플리케이션의 상태는 Hyperlink를 이용해 전이되어야 한다.  *(요즘 rest 에서 거의 모두 지키지 못하고 있음.)

- **Layered system(계층구조)** : Rest API의 서버는 다중 계층으로 구성될 수 있으며 보안, 로드 밸런싱, 암호화 등을 위한 계층을 추가하여 구조를 변경할 수 있습니다. 또한 Proxy, Gateway와 같은 네트워크 기반의 중간매체를 사용할 수 있게 해줍니다. 하지만 클라이언트는 서버와 직접 통신하는지, 중간 서버와 통신하는지 알 수 없습니다.

- **Cold-on-demand(optional)** : 서버에서 코드를 클라이언트로 보내서 실행 할 수 있어야 한다. (JavaScript)

## RestAPI 개념


**Server** 쪽에 **Client** 가 어떤 것을 **URL** 을 통해 **request**를  했을 때 그 resource 를 **response** 받고, **받는 타입(XML, JSON)** 을 선택 가능하고 그것을 **Representation** 이라고 한다.

Application은 Resource 를 받으면 그 결과 값을 보여 주기 위해 화면에 뿌려 주는데, 그렇게 되면 상태 값이 바뀌게 된다.

그래서 Rest 는 **representation** 을 주고 받는다(Transfer) 
라고 하여 **Representational State Transfer(REST)API** 라고 한다.


![Untitled](https://user-images.githubusercontent.com/57824945/76495089-85648800-6479-11ea-9e21-f869fdbc1097.png)

### 
### 
## REST의 장단점

- **장점** : HTTP 프로토콜의 인프라를 그대로 사용하므로 REST API 사용을 위한 별도의 인프라를 구출할 필요가 없다. HTTP 표준 프로토콜에 따르는 모든 플랫폼에서 사용이 가능하다. Hypermedia API의 기본을 충실히 지키면서 범용성을 보장한다. REST API 메시지가 의도하는 바를 명확하게 나타내므로 의도하는 바를 쉽게 파악할 수 있다. 여러가지 서비스 디자인에서 생길 수 있는 문제를 최소화한다. 서버와 클라이언트의 역할을 명확하게 분리한다.


- **단점** : 표준이 존재하지 않는다.사용할 수 있는 메소드가 4가지 밖에 없다. HTTP Method 형태가 제한적이다.브라우저를 통해 테스트할 일이 많은 서비스라면 쉽게 고칠 수 있는 URL보다 Header 값이 왠지 더 어렵게 느껴진다. 구형 브라우저가 아직 제대로 지원해주지 못하는 부분이 존재한다. PUT, DELETE를 사용하지 못하는 점pushState를 지원하지 않는 점.


### REST 가 필요한 이유

- 애플리케이션 분리 및 통합

- 다양한 클라이언트의 등장

- 최근의 서버 프로그램은 다양한 브라우저와 안드로이폰, 아이폰과 같은 모바일
디바이스에서도 통신을 할 수 있어야 한다.

- 이러한 멀티 플랫폼에 대한 지원을 위해 서비스 자원에 대한 아키텍처를 세우고
이용하는 방법을 모색한 결과, REST에 관심을 가지게 되었다.

### SmartArt 가 있는 두 개의 내용 레이아웃

- **Server-Client(서버-클라이언트 구조)**

자원이 있는 쪽이 Server, 자원을 요청하는 쪽이 Client가 된다.

REST Server: API를 제공하고 비즈니스 로직 처리 및 저장을 책임진다.

Client: 사용자 인증이나 context(세션, 로그인 정보) 등을 직접 관리하고 책임진다.

서로 간 의존성이 줄어든다.

- **Stateless(무상태)**

HTTP 프로토콜은 Stateless Protocol이므로 REST 역시 무상태성을 갖는다.

Client의 context를 Server에 저장하지 않는다.

- 즉, 세션과 쿠키와 같은 context 정보를 신경쓰지 않아도 되므로 구현이
단순해진다.Server는 각각의 요청을 완전히 별개의 것으로 인식하고 처리한다.각
API 서버는 Client의 요청만을 단순 처리한다.즉, 이전 요청이 다음 요청의 처리에
연관되어서는 안된다.물론 이전 요청이 DB를 수정하여 DB에 의해 바뀌는 것은
허용한다.Server의 처리 방식에 일관성을 부여하고 부담이 줄어들며, 서비스의
자유도가 높아진다.Cacheable(캐시 처리 가능)웹 표준 HTTP 프로토콜을 그대로
사용하므로 웹에서 사용하는 기존의 인프라를 그대로 활용할 수 있다.
