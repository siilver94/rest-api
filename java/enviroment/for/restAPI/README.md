# JAVA 시스템 개발 환경

- **JDK 11.0.4** ver
- **Maven**
- **Jersey**
- **Apache Tomcat 8.0**

---

## Maven

<code><img height = "350"
src = https://github.com/user-attachments/assets/886785be-4eba-40a6-9cfd-4e70e24cdb7c></code>


- 프로젝트를 진행하게 되면 단순히 자신이 작성한 코드만으로 개발하는것이 아니라 많은 라이브러리들을 활용해서 개발을 하게 됩니다. 이 때 사용되는 라이브러리들의 수가 수십개가 훌쩍 넘어버리는 일이 발생해 이 많은 라이브러리들을 관리하는 것이 힘들어지는 경우가 종종 발생하곤 합니다. Maven은 이러한 문제를 해결해 줄 수 있는 도구 입니다. Maven은 내가 사용할 라이브러리 뿐만 아니라 해당 라이브러리가 작동하는데에 필요한 다른 라이브러리들까지 관리하여 네트워크를 통해서 자동으로 다운받아 줍니다.

- Maven은 프로젝트의 전체적인 라이프 사이클을 관리하는 도구 이며, 많은 편리함과 이점이 있어 널리 사용되고 있습니다. 기존에는 Ant가 많이 사용되었지만 Maven이 Ant를 넘어서 더 많은 개발자들이 사용하게 되었고 비교적 최근에는 Gradle이 새롭게 나와 사용되고 있습니다(대표적으로는 Android Studio).


출처: https://boxfoxs.tistory.com/324

---

## Jersey

<code><img height = "350"
src = https://github.com/user-attachments/assets/a3540f11-12ce-4360-99f2-c578a1c7e81e></code>


- Jersey는 Sun의 JSR 311에서 구현된 JAX-RS: RESTful 웹 서비스용 Java API입니다. 

- Jersey는 JSR-311에서 정의된 내용을 가지고 있기 때문에 개발자는 Java 및 Java JVM으로 RESTful 웹 서비스를 쉽게 작성할 수 있습니다. 

- Jersey는 JSR에서 지정하지 않은 추가 기능도 지원합니다. 

---

## Apache Tomcat

![image](https://github.com/user-attachments/assets/bf8fcc0a-d750-4eb5-9310-bc62036af200)


- 아파치 톰캣(Apache Tomcat)은 아파치 소프트웨어 재단에서 개발한 서블릿 컨테이너(또는 웹 컨테이너)만 있는 웹 애플리케이션 서버이다.

- 톰캣은 웹 서버와 연동하여 실행할 수 있는 자바 환경을 제공하여 자바서버 페이지(JSP)와 자바 서블릿이 실행할 수 있는 환경을 제공하고 있다. 톰캣은 관리툴을 통해 설정을 변경할 수 있지만, XML 파일을 편집하여 설정할 수도 있다. 그리고, 톰캣은 HTTP 서버도 자체 내장하기도 한다.

- 아파치 톰캣은 Apache Licence, Version 2를 채용한 오픈소스 소프트웨어로서, 자바서버 페이지이나 자바 서블릿를 실행하기 위한 서블릿 컨테이너를 제공하며, 상용 웹 애플리케이션 서버에서도 서블릿 컨테이너로 사용하는 경우가 많다. 

출처 : https://ko.wikipedia.org/wiki/%EC%95%84%ED%8C%8C%EC%B9%98_%ED%86%B0%EC%BA%A3
