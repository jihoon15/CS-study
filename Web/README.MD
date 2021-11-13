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

웹 브라우저(Web Browser)는 인터넷을 활용하기 위해 사용하는 프로그램이다.<br>
HTML, CSS, 자바스크립트, 이미지, 폰트파일 등 **Rendering(렌더링)** 에 필요한 리소스를 서버에 요청하고 응답을 받아 화면을 구성한 뒤, 사용자에게 보여준다.

<br>

웹 서버(Web Server)는 HTTP를 통해 웹 브라우저에서 요청하는 HTML,CSS,JS 문서나 오브젝트(이미지 파일 등)을 전송해주는 서비스 프로그램이다.

<br>

---

### Rendering

<br>

대부분의 브라우저는 렌더링을 수행하는 렌더링 엔진(Rendering Engine)을 가지고 있다.<br>
렌더링이랑 HTML,CSS,JavaScript 등 개발자가 작성한 문서를 **브라우저에서 그래픽 형태로 출력하는 과정**을 말한다.

<br>

---

### 렌더링 과정

<br>

1. DOM(Document Object Model) 과 CSSOM(CSS Object Model) 생성

<img src="img/WEB_DOM.JPG"></img><br/>
**_<DOM, CSSOM 구조도> 출처 : http://bit.ly/3137pmh_**

<br>

서버로부터 받은 HTML, CSS를 다운로드 받아 연산과 관리가 유리하도록 Object Model을 생성한다.

<br>

2. Render Tree 생성<br>

<br>

<img src="img/WEB_RenderTree.JPG"></img><br/>
**_<렌더 트리 구조도> 출처 : http://bit.ly/2Okn0fG_**

<br>
   DOM Tree 와 CSSOM Tree를 이용해서 Render Tree를 생성한다.<br>
   DOM Tree와 다르게 __스타일 정보__가 설정되어 있다.<br>

. . . **실제 화면에 표현되는 노드**들로만 구성되어있다.

<br>

3. 자바스크립트 파싱<br>

<br>

<br>

4. Layout<br>

<br>

생성된 Render Tree 노드들이 가지고 있는 스타일과 속성에 따라서 **브라우저 화면의 어느위치에 어느크기로 출력될지 계산하는 단계**이다.

<br>

5. Paint<br>

<br>

요소들을 실제 화면을 그리는 단계.<br>
. . .Layout에서 요소들의 위치와 크기, 스타일 **계산이 완료된 Render Tree 를 이용해 실제 픽셀 값을 채워넣는다.** <br>
이 때 텍스트, 색, 이미지, 그림자 효과등이 모두 처리되어 그려진다.

---

<br>

### HTML, CSS , JavaScript

<br>

---

### DOM
