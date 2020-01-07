---
layout: post
title: "JUnit5 소개"
subtitle: "JUnit5 Overview"
categories: devlog
tags: java
---

# 1.1. JUnit5 소개
JUnit5는 이전 버전과는 다르게 3개의 모듈로 구성된다.    
### `JUnit5 = JUnit Platform + JUnit Jupiter + JUnit Vintage`
<br>

### JUnit Platform
JUnit Platform은 JVM에서 `테스트를 실행하는 프레임워크`를 제공한다.   
또한 platform에서 돌아가는 테스트 프레임워크를 개발하는 TestEngine API를 정의한다.   
platform을 Command 창에서 실행할 수 있도록 `Console Launcher`와, JUnit4 기반 환경에서 TestEngine을 실행하기 위한 `JUnit4 기반 Runner`를 제공한다.   
다양한 IDE(IntelliJ, Eclipse, NetBeans, VSCode)와 빌드툴(Gradle, Maven, Ant)에서 사용할 수 있다.

### JUnit Jupiter
JUnit Jupiter는 JUnit5의 `Test 작성`과 `extension`을 지원하는 TestEngine을 제공한다.

### JUnit Vintage
JUnit Vintage는 JUnit3와 JUnit4을 지원하는 TestEngine을 제공한다.

# 1.2. 지원하는 Java Versions
JUnit5는 Java8 이상의 JDK를 필요로 한다.   
Java8 이하의 JDK에서도 테스트를 해볼 순 있다.   

# 1.3. 질문하기
JUnit5와 관련된 질문은 [Stack Overflow][SO]와 [Gitter][G]를 통해 할 수 있다.

# 1.4. 시작하기
### 스프링 부트 프로젝트 만들기
스프링 부트 2.2+ 버전의 프로젝트를 생성하면 기본으로 JUnit5의 의존성이 추가된다.

### 스프링 부트 이외의 방법
```xml
<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter-engine</artifactId>
    <version>5.5.2</version>
    <scope>test</scope>
</dependency>
```

<br><br><br><br>

이 포스트는 [JUnit5 공식문서][JUnit]와 [더 자바, "코드를 테스트 하는 다양한 방법" - 백기선님][Baik] 을 참고하여 작성하였습니다.


[SO]: https://stackoverflow.com/questions/tagged/junit5
[G]: https://gitter.im/junit-team/junit5
[JUnit]: https://junit.org/junit5/docs/current/user-guide/
[Baik]: https://www.inflearn.com/course/the-java-application-test#























