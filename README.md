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






