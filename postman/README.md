## Postman 이란?

<br/>

````
A powerful GUI platform to make your API development faster & easier, from building API requests through testing, documentation and sharing.
````

Postman은 개발한 API를 테스트하고, 테스트 결과를 공유하여 API 개발의 생산성을 높여주는 플랫폼입니다.

Postman을 간단한 tool이 아닌 플랫폼으로 소개하는 이유는 직접 사용해 본다면 느껴지는데, API 테스트뿐만

아니라 작년에 업데이트된 버전부터는 Collection Sync, API Monitoring 등 팀원들이 협업하는데 도움을 주는 기능이 추가되었습니다. 

단, Team Library 기능은 30일 trial version 사용 이후에는 유료로 사용해야 합니다. 

*출처 : https://www.getpostman.com/pricing*

## Postman 설치
공식 홈페이지에서 다운받아 설치하며, 이메일 주소로 가입하거나 구글 계정을 이용하여 로그인할 수 있습니다. 

(Sync 기능을 위해 로그인하여 사용할 것을 추천드립니다.)


## Postman 사용법

가장 많이 사용하는 query string이 포함된 GET 방식의 호출과 JSON이 사용된 POST 방식의 호출을 샘플로 설명하겠습니다.

- Query string이 포함된 GET 방식의 호출


URI에 query string을 포함한 GET 방식으로 호출하는 경우에는 URI에 입력한 키와 값이 URI 입력칸 밑에 [key]와 [value]로 추가되고,
API를 호출한 결과는 하단의 [Body] 영역에 출력됩니다.


## Postman 활용 방법

위의 방법만 사용한다면 Postman 외에도 많은 Testing tool이 있습니다. 
가장 많이 사용하게 될 `Collections`, `Code generate`, `Manage environments`, `Interceptor` 4가지 기능입니다.


- **1. Collections** (https://www.getpostman.com/docs/collections)
- 
Collections will take your productivity to the next level.

설명 그대로 생산성을 한 단계 높여주는데 큰 역할을 합니다.
Postman에서 사용하는 Bookmark 기능으로, 사용법도 매우 간단합니다.

- **2. Code generate** (https://www.getpostman.com/docs/code_snippets)
- 
Postman의 Code generate 기능을 사용하면 다양한 언어별로 해당 API를 호출하는 source code를 생성해줍니다.

- **3. Manage environments** (https://www.getpostman.com/docs/environments)
API를 개발하다 보면 local, development, production 환경마다 각각 다르게 호출해야 하는 경우가 생깁니다.
일반적으로 hostname이 다른 경우가 많습니다.

- **4. Interceptor** (https://www.getpostman.com/docs/capture)
- 
Interceptor 기능은 chrome 브라우저를 이용하여 브라우저 내에서 발생한 Request를 자동으로 Postman History에 등록해주는 기능입니다.

https://chrome.google.com/webstore/detail/postman-interceptor/aicmkgpgakddgnaphhhpliifpcfhicfo 에서 확장 프로그램을 설치한 뒤 
 Chrome 우측 상단에서 Request Capture를 활성화합니다. 이후 Postman Application의 [Interceptor] 아이콘을 클릭하여 활성화합니다.
