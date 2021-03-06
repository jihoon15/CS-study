# **Web**

### #정리

---

## 웹이란 무엇인가?

<br>

- ### Network

  컴퓨터와 컴퓨터를 연결해 주는 망. <br>

- ### Internet
  통신 **프로토콜**을 이용해서 정보를 주고 받는 컴퓨터 네트워크<br>
  . . . 네트워크와 네트워크를 연결해 놓은 네트워크<br>

<br>

### Web?

<br>

World Wide Web의 줄임말로 WWW라고도 함.<br>
. . .서비스이다. 인터넷에서 제공하는 여러가지 서비스가 있는데, 그 중 가장 많이 사용하는 것이 바로 **웹 서비스**이다.
<br><br>

웹에서는 HTML 언어를 사용하여 작성된 하이퍼텍스트 문서를 웹 페이지(web page)라고 부르고, 이러한 웹 페이지들 중에서 서로 관련된 내용으로 작성된 웹 페이지들의 집합을 웹 사이트(web site)라고 한다.

웹은 이렇게 작성된 수많은 웹 페이지들이 하이퍼링크(hyperlink)를 통해 서로 연결되어 구성된다.

사용자가 웹 페이지에 포함된 하이퍼링크를 따라 다른 웹 페이지들로 계속하여 이동하는 것을 웹 서핑(web surfing)이라고 부르고, 이때 사용자가 웹 페이지를 검색하기 위해 사용하는 프로그램을 **웹 브라우저(web browser)** 라고 한다.
<br><br>

---

<br>

### Web Browser 와 Web Server

<br>
<img src="img/WEB_server.JPG"></img><br/>

<br>

웹 브라우저(Web Browser)는 인터넷을 활용하기 위해 사용하는 프로그램이다.<br>
HTML, CSS, 자바스크립트, 이미지, 폰트파일 등 **Rendering(렌더링)** 에 필요한 리소스를 서버에 요청하고 응답을 받아 화면을 구성한 뒤, 사용자에게 보여준다.

<br>

웹 서버(Web Server)는 HTTP를 통해 웹 브라우저에서 요청하는 HTML,CSS,JS 문서나 오브젝트(이미지 파일 등)을 전송해주는 서비스 프로그램이다.

<br>

---

## Web Browser

<br>

 ### Rendering(렌더링)<br><br>

 대부분의 브라우저는 렌더링을 수행하는 렌더링 엔진(Rendering Engine)을 가지고 있다.<br>
 렌더링이랑 HTML,CSS,JavaScript 등 개발자가 작성한 문서를 **브라우저에서 그래픽 형태로 출력하는 과정**을 말한다.<br><br><br>

 ### 렌더링 과정<br><br>

 **_. . .브라우저마다 차이가 있습니다._** <br>**_Google의 Web Fundamentals 문서를 참고하였습니다. https://developers.google.com/web/fundamentals?hl=ko_**<br>

 <br>

 1. DOM(Document Object Model) 과 CSSOM(CSS Object Model) 생성

>    <br>
>
> - ### DOM
>
> <br>  
>  <img src="img/WEB_Make.JPG"></img>
> <br>
> <br>
>
> - **변환**<br>
> : 브라우저가 HTML의 원시 바이트를 디스크나 네트워크에서 읽어와서, 해당 파일에 대해 지정된 인코딩(예: UTF-8)에 따라 개별 문자로 변환합니다.
> <br>
>
> - **토큰화**<br>
> : 브라우저가 문자열을 W3C HTML5 표준에 지정된 고유 토큰으로 변환합니다(예: '', '' 및 꺽쇠괄호로 묶인 기타 문자열). 각 토큰은 특별한 의미와 고유한 규칙을 가집니다.
> <br>
>
> - **렉싱**<br>
> : 방출된 토큰은 해당 속성 및 규칙을 정의하는 '객체'로 변환됩니다.
> <br>
>
> - **DOM 생성**<br>: 마지막으로, HTML 마크업이 여러 태그(일부 태그는 다른 태그 안에 포함되어 있음) 간의 관계를 정의하기 때문에 생성된 객체는 트리 데이터 구조 내에 연결됩니다. 이 트리 데이터 구조에는 원래 마크업에 정의된 상위-하위 관계도 포합됩니다. 즉, HTML 객체는 body 객체의 상위이고, **_body_** 는 **_paragraph(p)_** 객체의 상위인 식입니다.  
>  <br>
>
> **이 전체 프로세스의 최종 출력이 바로 이 간단한 페이지의 DOM(Document Object Model)이며, 브라우저는 이후 모든 페이지 처리에 이 DOM을 사용합니다.** <br>
> <br>
>
> - ### CSSOM<br><br>
>
>   <img src="img/WEB_CSSOM.JPG"></img><br>  
>    CSS 바이트가 문자로 변환된 후 차례로 토큰과 노드로 변환되고 마지막으로 'CSS Object Model'(CSSOM)이라는 트리 구조에 링크됩니다.
>   <br>  
>    <img src="img/WEB_DOM.JPG"></img><br/>**_<DOM, CSSOM 구조도>_**<br><br>
>   서버로부터 받은 HTML, CSS를 다운로드 받아 연산과 관리가 유리하도록 Object Model을 생성한다.
>
> <br>
<br><br>

2. Render Tree 생성<br>
>    <br>
>
> 1. DOM 트리의 루트에서 시작하여 표시되는 노드 각각을 트래버스합니다.<br>
>
>    > - 일부 노드는 표시되지 않으며(예: 스크립트 태그, 메타 태그 등), 렌더링된 출력에 반영되지 않으므로 생략됩니다.<br>
>    > - 일부 노드는 CSS를 통해 숨겨지며 렌더링 트리에서도 생략됩니다. 예를 들어,---위의 예시에서---span 노드의 경우 'display: none' 속성을 설정하는 명시적 규칙이 있기 때문에 렌더링 트리에서 누락됩니다.<br>
>
> <br>
>
> 2. 표시된 각 노드에 대해 적절하게 일치하는 CSSOM 규칙을 찾아 적용합니다.
> 3. 표시된 노드를 콘텐츠 및 계산된 스타일과 함께 내보냅니다.
>
>    <br>
>
> <img src="img/WEB_RenderTree.JPG"></img><br>**_<렌더 트리 구조도>_**<br>
>
> DOM Tree 와 CSSOM Tree를 이용해서 Render Tree를 생성한다.<br>
> DOM Tree와 다르게 **스타일 정보** 가 설정되어 있다.
> <br>
> . . . **실제 화면에 표현되는 노드**들로만 구성되어있다.<br>
> <br>

<br><br>

3. 자바스크립트 파싱<BR>
>  <br>
>
> 자바스크립트의 파싱은 CSS파싱과 마찬가지로 렌더링 엔진이 HTML 문서를 한줄 씩 읽어나가다 **_script태그_** 를 만나면 **자바스크립트 엔진**에 제어권을 넘기며 시작됩니다.<br>
>
> 자바스크립트 엔진은 CPU가 이해할 수 있는 저수준 언어로 자바스크립트 코드를 파싱하고,<br>
> DOM, CSSOM과 같은 AST(Abstract Syntax Tree) 생성합니다.<br>
>
> . . . **AST: _토큰에 문법적 의미과 구조를 반영한 트리형태의 자료구조_**<br>
> 그리고 AST를 기반으로 바이트코드를 생성하여 인터프리터가 실행될 수 있도록 만듭니다.<br><br>
>
> <img src="img/WEB_JS.JPG"></img><br/><br>

<br><br>

4. Layout<br>

> 생성된 Render Tree 노드들이 가지고 있는 스타일과 속성에 따라서 **브라우저 화면의 어느위치에 어느크기로 출력될지 계산하는 단계**이다.<br>
><br>

<br>

5. Paint<br>

> 요소들을 실제 화면을 그리는 단계.<br>
> . . .Layout에서 요소들의 위치와 크기, 스타일 **계산이 완료된 Render Tree 를 이용해 실제 픽셀 값을 채워넣는다.** <br>
> 이 때 텍스트, 색, 이미지, 그림자 효과등이 모두 처리되어 그려진다.<br>
> <br>

<br>


 ### Reflow(Layout), Repaint(Paint)<br>

> 자바스크립트 코드가 실행되는 과정에서 DOM과 CSSOM을 변경하는 DOM API가 사용되면 변경된 DOM과 CSSOM이 다시 렌더트리로 결합되고 레이아웃과 페인트 과정을 거쳐 다시 렌더링됩니다.<br>
>
> 이 과정을 **리플로우(reflow), 리페인트(repaint)** 라고 합니다.<br>
> <br>

---

<br>

## Web Server

<br>

### Web Server(웹서버)
<bR>

> 웹 브라우저와 같은 클라이언트로부터<br>
> HTTP 프로토콜로 요청을 받아,<br>
> HTML 문서 등과 같은 웹 페이지를 __정적__ 으로 처리해 반환하는 소프트웨어<br>
>
><br>
>
>### 하드웨어/소프트웨어적 웹서버<br>
><br>
>
>- 하드웨어 측면:<br>
>  - 웹사이트의 컴포넌트 파일들을 저장하는 컴퓨터<br>
>  - 컴포넌트 파일에는 html 문서/images/css stylesheets/JavaScript 파일 등<br>
>  - 이 컴포넌트 파일들을 최종 소비자의 디바이스에 전달함<br>
>  - 웹 서버는 인터넷에 연결되어 있고, 도메인 이름을 통해 접속될 수 있음<br>
><br>
>- 소프트웨어 측면:
>  - 웹 사용자가 어떻게 호스트 파일들에 접근하는지를 관리<br>
>  - HTTP 서버는 URL(Web address)과 HTTP의 소프트웨어 일부<br>
><br>
>
>### 기능<br>
><br>
>- 정적인 컨텐츠 제공<br>
>- WAS를 거치지 않고 바로 자원 제공<br>
>- 동적인 컨텐츠 제공을 위한 요청 전달<br><br>
>
>
<br>

### Web Server(웹 어플리케이션 서버)<br>

> DB 조회나 다양한 로직 처리를 요구하는 동적인 컨텐츠를 제공하기 위해 만들어진 Application Server<br>
> HTTP 프로토콜을 통해 컴퓨터나 장치에 애플리케이션을 수행해주는 미들웨어<br>
> Web Server + Web Container(Servlet Contatiner)<br>
>>. . .Container란 JSP, Servlet을 실행시킬 수 있는 소프트웨어<br>
>> WAS는 JSP, Servlet 구동 환경을 제공한다.<br><br>
>### 기능<br>
>- 프로그램 실행 환경과 DB 접속 기능 제공<br>
>- 여러 개의 트랙잭션 관리 기능<br>
>- 업무를 처리하는 비즈니스 로직 수행<br><br>

<br>

<img src="img/WEB_WAS.JPG"></img><br/>
___출처:https://velog.io/@dbfudgudals/was%EB%9E%80___<br>

<br>

### WEB Server 와 WAS 분리 이유<br>
<br>

- __기능을 분리__ 하여 __서버의 부하를 방지__<br>
  . . . WAS는 DB조회 등 페이지를 만들기 위한 다양한 로직을 처리하느라 바쁘다. 단순한 정적 콘텐츠를 WAS에서 제공한다면 다른 작업에 사용하는 리소스들로 인해 지연이 생겨날 수 있다. 그러므로 정적 콘텐츠는 Web Server선에서 빠르게 처리하는게 좋다.<bR><br>
- 보안강화<br>
  - SSL(Secure Socket Layer)에 대한 암복호화 처리에 Web Server 사용.
  - 공격에 대해 Web Server을 앞단에 두어 중요한 정보가 담긴 WAS(DB나 로직)까지 전파되지 못하게 한다.
<br>

<br>

---

<br>

## SPA, MPA

> MPA : Multi Page Application, 한 개의 Page로 구성된 애플리케이션<br>
> SPA : Single Page Application 여러 개(Single) Page로 구성된 애플리케이션<br>
>
> <br>
>
> ___MPA___ 는 __새로운 페이지를 요청할 때마다 정적 리소스가 다운로드__ 된다. __매번 전체 페이지가 다시 렌더링 된다.__<br>
> . . . MPA를 SSR(Server Side Rendering) 방식으로 렌더링 한다고 말한다.<br>
> <br>
> ___SPA___ 는 웹 에플리케이션에 필요한 모든 정적 리소스를 __최초 한 번__ 에 다운로드한다.<br>
> 그 이후 새로운 페이지 요청이 있을 때, 페이지 갱신에 __필요한 데이터__ 만 전달 받아서 페이지를 갱신한다.<br>
> . . . SPA를 CSR(Client Side Rendering) 방식으로 렌더링 한다고 말한다.
>
> <br>
> 
>   
>>  <br> 
>>  
>>  - ### MPA  <br>
>>  <br>
>>  <img src="img/WEB_MPA.JPG"></img><br/>
>> 
>>  ___출처:https://hanamon.kr/spa-mpa-ssr-csr-%EC%9E%A5%EB%8B%A8%EC%A0%90-%EB%9C%BB%EC%A0%95%EB%A6%AC___<br>
>> <br>
>>
>>  - 장점<br>
>>  1. __SEO__(Search Engine Optimization), 검색 엔진 최적화 관점에서 유리하다.<br>
>>  <br>
>>  . . . MPA는 완성된 형태의 HTML 파일을 서버로부터 전달받는다.<Br>
>>  따라서 검색엔진이 페이지를 크롤링하기에 적합하다.<br>
>>  <br>
>>  2. 첫 로딩이 매우 짧다.<br>
>>  <br>
>>  - 단점<br>
>>  1. 새로운 페이지를 요청할 때마다 전체 페이지를 렌더링한다.<br>
>>  2. 페이지 이동시 불필요한 템플릿도 중복해서 로딩<br>
>>  3. 서버 렌더링에 따른 부하<br>
>>  <br> 
>>
>>  - ### SPA <br>
>>  <br>
>>  <img src="img/WEB_SPA.JPG"></img><br/>
>>
>>  ___출처:https://hanamon.kr/spa-mpa-ssr-csr-%EC%9E%A5%EB%8B%A8%EC%A0%90-%EB%9C%BB%EC%A0%95%EB%A6%AC___<br>
>>  <br>
>>
>>  - 장점<bR>
>>  1. 필요한 부분만 갱신하기 때문에 네이티브 앱에 가까운 자연스러운 페이지 이동을 제공할 수 있다.<br>
>>  2. SPA는 최초 정적 리소스를 다운 받으면 데이터를 전부 저장해놓는다.<br>
>>    필요한 리소스만 부분적으로 로딩하기 때문에 성능면에서 좋다.<br>
>>  3. 서버의 템플릿 연산을 클라이언트로 분산하여 서버의 부하를 줄여준다.<br>
>>  4. 컴포넌트별로 개발하기 때문에 생산성이 증가된다.<br>
>>  <br>
>>  - 단점<br>
>>  1. 초기 구동 속도가 느리다.<br>
>>  2. SEO 관점에서 불리하다.<br>
>>  3. 보안 문제<br>
>>  . . . SSR에서는 사용자에 대한 정보를 서버측에서 세션으로 관리를 하지만 CSR 방식에서는 클라이언트측의 쿠키말고는 사용자에 대한 정보를 저장할 공간이 마땅치 않다.
>>
>> <br>
>
><br>

<br>

---

### HTTP?<br>
> 텍스트 기반의 통신 규약으로 __인터넷에서 데이터를 주고받을 수 있는 프로토콜__
<br>

클라이언트 즉, 사용자가 브라우저를 통해서 어떠한 서비스를 url을 통하거나 다른 것을 통해서 요청(request)을 하면 서버에서는 해당 요청사항에 맞는 결과를 찾아서 사용자에게 응답(response)하는 형태로 동작한다.
<br>
~~. . . HTML 문서만이 HTTP 통신을 위한 유일한 정보 문서는 아니다.~~ <br>
~~JSON 및 XML과 같은 형태의 정보도 주고 받을 수 있다.~~ 
<br>
<br>
### HTTP 특징

> - HTTP 메시지는 HTTP 서버와 HTTP 클라이언트에 의해 해석이 된다.<br>
> - TCP/ IP를 이용하는 응용 프로토콜이다.<br>
> - HTTP는 연결 상태를 유지하지 않는 비연결성 프로토콜이다. __stateless__<br>
    . . . 이러한 단점을 해결하기 위해 Cookie와 Session이 나옴.<br>
> - HTTP는 연결을 유지하지 않는 프로토콜이기 때문에 요청/응답 방식으로 동작한다.<br>

<br>

### Request
> 클라이언트가 서버에게 연락하는 것, 요청을 보낼때는 요청에 대한 정보를 담아 서버로 보낸다.

<br>

Request Method
- GET     : 자료를 __요청__
- POST    : 자료의 __생성__ 을 요청
- PUT     : 자료의 __수정__ 을 요청
- DELETE  : 자료의 __삭제__ 를 요청

<br>

### Response<br>
> 서버가 요청에 대한 답변을 클라이언트에게 보내는 것

<br>

상태 코드(Status Code)<br>
- 1XX(조건부 응답) : 요청을 받았으며 작업을 계속한다.
- 2XX(성공) : 클라이언트가 요청한 동작을 수신하여 성공적으로 처리했다.
- 3XX(리다이렉션 완료) : 클라이언트는 요청을 마치기 위해 추가 동작을 취해야 한다.
- 4XX(요청 오류) : 요청의 문법이 잘못되었거나 요청을 처리할 수 없다.(클라이언트 오류)
- 5XX(서버오류) : 서버가 유효한 요청을 수행하지 못했다.

<br>

---


## Servlet<br>
<br>

서블릿은 자바로 만들어진 프로그램을 서버에서 실행하기 위해 만들어졌다. 특히 웹 서비스 개발에 특화되어 있으며 데이터베이스 연동, 외부 서비스 연동을 통해 정적인 웹에 __동적인 정보 제공__ 을 가능하게 한다.<br>
<br>

## Why Servlet?

<br>

### CGI<br>
>Web Server는 이미 저장되어 있는 정적인 컨텐츠(Html)를 응답한다.<br>
>만약 사용자가 직접 정보를 찾거나(검색) 기록(저장)을 하려면 __웹서버의 문서를 직접 고치는 작업__ 이 필요했다.<br> 
>때문에 사용자의 입력과 요청 url에 따라 __동적으로 변하는 페이지__ 가 필요하게 되었고,<br>
>웹서버에서 동적인 처리를 담당할 표준인 CGI(Common Gateway Interface)가 등장하게 되었다.<br>

<br>

. . . CGI는 __서버와 응용 프로그램간에 데이터를 주고받기 위한 방법이나 규약__ 을 뜻한다.<br>

>1. 웹 브라우저의 HTML의 폼을 통해 요청이 웹 서버로 전달<br>
>2. 웹 서버는 요청에 들어 있는 주소가 CGI 프로그램에 대응되는지 확인<br>
>3. 대응될 경우 그 프로그램을 실행, 환경 변수와 표준 입력의 형태로 요청을 전달한다.<br>
>4. 웹 서버는 CGI 프로그램이 표준 출력으로 돌려 보낸 내용을 그대로 응답으로 돌려 준다.<br>

<br>

CGI 의 가장 큰 단점은 __멀티프로세스 방식__ 이란 것이다. 멀티프로세스 방식은 요청이 올 때 마다 프로세스를 생성한다.<br> 

. . .프로세스는 자원을 상당히 많이 차지하므로 이를 해결하기 위해 요청에 대응하여 프로세스가 아닌 __스레드__ 를 생성하는 자바의 Servlet이 등장했다.<br>

<br>




<br>

---
<br>

### Servlet<br>

>Java Servlet(자바 서블릿)은 Java를 사용하여 웹페이지를 동적으로 생성하는 서버측 프로그램 혹은 그 사양을 말하며 흔히 서블릿이라 불린다.<br>
>. . . Java 코드 안에 HTML을 포함한다.<br>
>~~. . .JSP는 HTML 문서 안에 Java 코드를 포함~~<br>

<br>

서블릿(Servlet)의 주요 특징<br>
- 클라이언트의 Request에 대해 동적으로 작동하는 웹 애플리케이션 컴포넌트<br>
- HTML을 사용하여 Response 한다.<br>
- JAVA의 스레드를 이용하여 동작한다.<bR>
- MVC 패턴에서의 컨트롤러로 이용된다.<br>
- HTTP 프로토콜 서비스를 지원하는 javax.servlet.http.HttpServlet 클래스를 상속받는다.
- UDP보다 속도가 느리다.<br>
- HTML 변경 시 Servlet을 재 컴파일해야 하는 단점이 있다.<br>

<br>

### Servlet 의 기본적인 동작<br>
<br>
<img src="img/WEB_Servlet_Process.JPG"></img><br/>

___출처 : https://gmlwjd9405.github.io/2018/10/28/servlet.html___

<br>

## Why JSP? <br>

<br>

JSP가 등장한 가장 큰 이유는 서블릿이 가진 HTML 표현상의 문제를 해결하기 위해서였다.
서블릿 프로그램 내에서 HTML을 처리하기 때문에 간단한 태그를 변경할 때 조차 __재컴파일__ 을 해야하는 문제가 있다.
<br>

- 웹 디자이너는 마음대로 화면을 수정할 수 없었고,<br>
- 비즈니스로직과 컨텐츠가 소스(서블릿)에 같이 있기 때문에 유지보수가 불편했다.<br>

<br>

이를 해결하기 위해
- 서블릿의 비즈니스 로직과 화면 기능을 분리함<Br>
  이를 통해 개발자는 로직 구현에, 디자이너는 화면 기능 구현 집중<br>
- 개발 후 재사용성과 유지보수가 수월해짐.

<br>


기존 서블릿에서는 __자바 코드를 기반__ 으로 문자열을 사용해 HTML과 js로 화면을 구현했다.<br>
JSP는 이와 반대로 __HTML, CSS, js를 기반__ 으로 JSP 요소들을 사용해 화면을 구현한다.<Br>

---

## 인증(Authentication)과 인가(Authorization)

<br>

인증이란?
> 보호된 리소스에 접근하는 것을 __허용하기 이전에__ 등록된 유저의 신원을 입증하는 과정
. . . 신원이 올바른지 검증하기 위한 과정

<br>

인가란?
> 요청된 리소스에 접근할 수 있는 __권한이 있는 인증된__ 유저인지 입증하는 과정
. . . 신원을 기반으로 인증된 주체가 특정 리소스에 접근할 수 있는 권한을 주는 것.

<br>

. . .  인증 - 접근 허용 - 인가 - 리소스 접근 권한

<br>

웹에서의 인증과 인가
- 요청 헤더
- 세션, 쿠키
- 토큰
- __OAuth__

## OAuth란?
OAuth는 인터넷 사용자들이 비밀번호를 제공하지 않고 다른 웹사이트 상의 자신들의 정보에 대해 웹사이트나 애플리케이션의 __접근 권한을 부여__ 할 수 있는 공통적인 수단으로서 사용되는, 접근 위임을 위한 개방형 표준이다.

<br>

OAuth의 장점
<Br>

대상 | 장점
---|---|
|사용자 | 서비스에 ID/PW를 안 알려준다.<br>원할 때 엑세스 토큰의 권환 취소 가능
|서비스 | 유저의 엑세스 토큰만 보유하면 된다.<br> 사용자의 ID/PW없이도 허가 받은 API 접근가능

__AccessToken__ <br>
아이디, 비밀번호가 아닌 서비스가 가진 기능을 부분적으로 허용해준다.<br>
OAuth를 통해서 획득하고 토큰을 통해 데이터를 가져오고, 수정, 삭제 기능을 수행 가능

<br>


OAuth 참여자


- Resource Server
    - Client가 제어하고자 하는 자원을 보유하고 있는 서버
    - Google, FaceBook 등
    
    <br>

- Resource Owner
    - Client가 제공하는 서비스를 통해 로그인하는 유저
    
    <Br>

- Client
    - Resource Server에 접속해서 정보를 가져오고자 하는 클라이언트(Application)

<br>

---

## 등록
<br>

~~서비스마다 상이하지만 공통적인 부분~~

Client ID
- 우리가 만들고있는 App을 식별하는 ID
- 노출 가능

Client Secret
- Cliend ID에 대한 비밀번호
- 절대로 노출되면 안된다

Authorized redirect URIs
- 리소스 서버가 권환을 부여하는 과정에서 Authorized code를 준다. 이 것을 전달받을 리다이렉트 주소
- 등록되지 않은 리다이렉트 주소에서 오는 요청은 인증을 거부함

. . . 등의 정보를 등록한다.

<br>

---
## Resource Owner의 승인

<br>

<img src="img/WEB_OAuthReg1.JPG"></img><br/>

1. 링크 클릭(ex. login with google)
2. 링크(ex
<img src="img/WEB_OAuthURL.JPG"></img><br/>)
리다이렉트를 통해 3번으로 이동
3. 로그인이 되어 있으면(안 되어있으면 로그인 요청) 정보를 확인한다(redirect url과 client id 등)
4. 어떤 권한(scope)을 허용할 것이냐?
5. 허락 한다. 
Resource Server에서 Resource Owner가 어떤 기능을 어떤 scope에 대한 작업을 동의하였다. 를 기록한다.

<br>

---

## Resource Server의 승인

<Br>

<img src="img/WEB_OAuthReg2.JPG"></img><br/>

<br>

1. Resource Owner에게 authorization code(임시 비밀번호)를 전송<br> (redirect URL에 담아서,ex https://test/callback?__code=3__ 
)
2. Client에게 authorization code가 전송된다
3. Client가 Resource Server에 직접 접속,<br>
authorization code와 client id, client secret 전송
4. Resource Server에서 자신의 기록과 일치하는지 비교한다.

<Br>

---

## Access Token 발급

<img src="img/WEB_OAuthReg3.JPG"></img><br/>

1. (authorization code 값을 지운다) accessToken을 발급하고 Client에 응답한다.
2. Client는 내부적으로 토큰을 저장한다.

---

## Refresh Token

accessToken에는 수명이있다. 수명이 다 할시에 재발급을 받아야한다.<br>
위의 Resource Owner의 승인, Resource Server의 승인, Access Token 발급 과정을 반복하지 않기 위해 사용하는 방법이다.

<br>

<img src="img/WEB_RefreshToken.JPG"></img><br/>

참고: RFC6749 https://datatracker.ietf.org/doc/html/rfc6749

*상위 과정들에 나오는 Resource Server은 참고 사진의 Resource Server와 Authorization Server을 합친 것*
<br>

*위 참고 사진의 A 과정은 Resource Server의 승인 과정의 3번에 해당하는 것 같다*

<br>

---

# WebRTC

<br>

## NAT

<br>
네트워크 주소변환(NAT)

> IP 패킷에 있는 출발, 목적지의 IP 주소와 TCP/UDP 포트 숫자 등을 바꿔 재기록하면서 네트워크 트래픽을 주고 받게하는 기술

<br>

왜 사용하는가?
- IP 주소 절약
    - 하나의 공인 IP 주소를 통해 여러대의 호스트가 인터넷에 연걸 가능.<br>
    = 하나의 공유기에 여러 대의 컴퓨터 연결, 인터넷 공유기에 NAT기능 탑재되어있음.
- 보안
    - NAT 동작의 특성상 IP를 숨길 수 있는 기능이 있다.<br>
    외부로 트래픽이 나갈 때 private IP에서 public IP로 바뀌므로 내부 네트워크를 보호할 수 있다.

    <br>

<img src="img/WEB_NAT.JPG"></img><br/>
*출처 : 위키피디아*

<Br>

## WebSocket

<br>

브라우저와 서버의 통신 = HTTP<br>

브라우저 -> 서버 Request<br>

서버 -> 브라우저 Response<br>

HTTP는 Stateless이다.<br>

request - response 이후에 통신은 끊김.<br>

request 없이는 response 도 없다<br>

-> 서버에서 브라우저로 그냥 response를 보낼 수 없다.<br>

실시간으로 데이터를 주고 받을 수 없음.<Br>
웹 소켓 등장

request - response -> open - close (connection)<Br>

<Br>

웹 소켓 서버에 접속하여 데이터 전송시 연결된 다른 사용자에게 전달된다.<br>

사용자가 많아지면 서버에 부하가 걸린다(메모리)<br>

-> __브라우저와 서버가 아닌, 브라우저와 브라우저끼리 연결하자..! = WebRTC__

<br>

WebRTC란?

<br>

> Web Real-Time Communication<br>
> 웹 app 및 사이트들이 별도의 SW 없이 __중간자 없이__ 텍스트, 오디오, 영상 등의 데이터를 브라우저 끼리 주고 받을 수 있게 만든 기술

<Br>

---

필요한 요소

- Signaling Server
- NAT Traversal(STUN TURN) Server
- Media Server

<Br>

## Signaling Server

<br>

WebRTC는 사용자 간의 Peer to Peer 통신을 통해 데이터를 교환한다.
그리고 이를 위해서는 통신을 하는 주체끼리의 약속이 필요하다.
<Br>

Signaling Server는 사용자 간의 P2P 통신을 위해 사용자를 엮어주는 역할을 한다.

<br>

## STUN, TURN

Signaling 서버를 통해 P2P 통신을 하고자 하는데, 방확벽이 있거나 NAT 환경에서는 연결이 불가하다.<br>

이런 때에 시그널링을 하기 위해서는 __방화벽을 통과시켜주거나 private ip를 public ip로 바꿔주는 STUN서버 또는 TURN서버__ 를 시용해야 한다.
<br>중간에서 중개해줄 무언가가 필요하다.

<br>

### STUN Server
<Br>

__S__ ession __T__ raversal __U__ tilities for __N__ AT <br>

client가 자신의 public IP를 확인하기 위해 STUN 서버로 요청을 보내고 서버로 부터 자신의 Public IP를 받는다. <br>
~~신분을 확인받고 입장권을 받는 느낌~~
<br>
그리고 받은 Public IP를 이용하여 시그널링을 한다.

*단, 두 Cleint가 같은 네트워크에 존재하고 있을 때는 이것으로 해결이 되지않는다<br>


### TURN Server

<br>
Client들이 통신할 때 public 망에 존재하는 TURN 서버를 경유하여 통신하게 한다.<br>
Client는 자신의 private IP를 포함한 TURN 메시지를 턴서보로 보내고, TURN 서버는 메시지에 포함된 주소와 UDP 포트넘버와의 차이를 통해 public ip에 응답한다.<br>
<br>
그리고 이때 NAT 매핑 테이블에 기록되어 있는 정보에 따라 NAT가 클라이언트의 private IP로 메시지를 전송함.