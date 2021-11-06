## **운영 체제**

참고 문헌: Operating System Concepts(
Abraham Silberschatz , Peter B. Galvin , Greg Gagne)<br>
참고 강의: KOCW 양희재 교수님 운영체제 강의

---

## <h1> 운영 체제란?

컴퓨터의 하드웨어를 관리하는 소프트웨어, 하드웨어와 소프트웨어 사이의 **인터페이스**이다.

<img src="img/OS_intro.JPG"></img><br/><br/>

컴퓨터 시스템 자원들을 효율적으로 관리하여

- 성능을 높이고
- 사용자의 편의를 높여준다.<br>
  . . 컴퓨터 하드웨어를 관리하는 프로그램

<img src="img/OS_service.JPG"></img><br/>

---

## 운영체제 서론

<br>

**-Booting**
<br>

컴퓨터의 구조를 단순화하면 이러하다.<br>

<img src="img/OS_BootLoader.JPG"></img><br/>

- Processor: 일반적인 CPU
- ROM: 비휘발성, 전원이 꺼져도 내용이 유지된다. 보조메모리, 디스크
- RAM: 휘발성, 전원이 꺼지면 내용이 지워진다. 흔히 말하는 메인 메모리

컴퓨터의 전원을 키면 CPU에서 ROM에 있는 내용을 읽는다.
ROM에는 **POST**,**부트 로더** 가 저장되어 있다. POST는 전원이 켜지면 가장 처음에 실행되는 프로그램으로 컴퓨터의 상태를 검사한다.
그 다음 부트 로더가 실행된다. 부트 로더는 하드디스크에 저장되어 있는 운영체제를 찾아서 RAM 에 가지고 온다. 이러한 부트 로더의 과정을 부팅이라고 한다

---

**-Shell**

Command Interpreter

<br>

운영체제는 크게보면 커널(Kernel), 쉘(Shell) 로 구성된다.
<br>

<img src="img/OS_Shell.JPG"></img><br/>

- 커널 : 실제로 관리하는 프로그램. 뜻 그대로 핵심
- 쉘 : 사용자의 명령을 화면에 보여주는 역할 <br>
  쉘은 사용자가 요청하는 **_명령어를 해석하여 커널에 요청하고 결과를 화면에 보여준다._**
  <br>
  <br>

**-Application on OS**<br>

프로그램은 특정 운영체제에 맞춰서 만든다. 같은 CPU에 같은 명령어일지라도 **System call**의 종류가 다르기 때문이다.
<br>

<img src="img/OS_Application.JPG"></img><br/>

애플리케이션은 위의 그림과 같이 운영체제 위에서 수행한다. 즉, 하드웨어 자원을 직접적으로 사용하지 않고 운영체제가 **제공하는 자원**만을 사용할 수 있다.

---
