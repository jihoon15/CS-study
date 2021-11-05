## **운영 체제**

참고 문헌: Operating System Concepts(
Abraham Silberschatz , Peter B. Galvin , Greg Gagne)

---

## <h1> 운영 체제란?

컴퓨터의 하드웨어를 관리하는 소프트웨어, 하드웨어와 소프트웨어 사이의 **인터페이스**이다.

<img src="img/OS_intro.JPG"></img><br/><br/>

컴퓨터 시스템 자원들을 효율적으로 관리하여 사용자의 편의를 높여준다.

<img src="img/OS_service.JPG"></img><br/>

---

## 운영체제 서론

컴퓨터의 구조를 단순화하면 이러하다.
<img src="img/OS_BootLoader.JPG"></img><br/>

- Processor: 일반적인 CPU
- ROM: 비휘발성, 전원이 꺼져도 내용이 유지된다. 보조메모리, 디스크
- RAM: 휘발성, 전원이 꺼지면 내용이 지워진다. 흔히 말하는 메인 메모리

컴퓨터의 전원을 키면 CPU에서 ROM에 있는 내용을 읽는다.
ROM에는 **POST**,**부트 로더** 가 저장되어 있다. POST는 전원이 켜지면 가장 처음에 실행되는 프로그램으로 컴퓨터의 상태를 검사한다.
그 다음 부트 로더가 실행된다. 부트 로더는 하드디스크에 저장되어 있는 운영체제를 찾아서 RAM 에 가지고 온다. 이러한 부트 로더의 과정을 부팅이라고 한다
