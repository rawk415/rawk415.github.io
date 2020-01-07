---
layout: post
title: "JUnit5 기본 어노테이션"
subtitle: "JUnit5 Annotations"
categories: devlog
tags: java
--- 

# 2.1. Annotations
JUnit Jupiter는 Test 환경을 설정하는 다양한 Annotation들을 지원한다.

### @Test
- JUnit5로 Test하는 메소드를 만든다. 
- JUnit4의 @Test로 매핑된다. 

### @Disabled
- Diaabled Annotation이 있는 테스트는 실행하지 않고 넘어간다.
- 깨진 테스트에 사용할 수 있으나, 깨진 테스트는 넘기는 것이 아니라 고치는 것이 바람직하다.
- @Ignore로 매핑된다.

---

## 2.2. LifeCycle Method

### @BeforeAll, @AfterAll
- Test class 안에 있는 모든 테스트가 실행되기 전, 모든 테스트가 실행된 후 딱 한 번만 실행된다.
- 반드시 `static` 이어야한다.
- 접근 제어자는 private은 불가, default는 가능
- 리턴타입이 있으면 안된다. `void`
- `static void`로 사용한다고 기억하자.
- @BeforeAll은 @BeforeClass로 매핑된다.
- @AfterAll은 @AfterClass로 매핑된다.

### @BeforeEach, @AfterEach
- 각각의 테스트들을 실행하기 전, 후에 실행된다.
- static일 필요 x
- @BeforeEach은 @Before로 매핑된다.
- @AfterEach은 @After로 매핑된다.

---

## 2.3. Display Names

### @DisplayNameGeneration
- Test 이름을 표기하는 방법을 설정한다.
- class, method에 사용할 수 있다.
- 기본 구현체로 ReplaceUnderscores 제공
- `@DisplayNameGeneration(DisplayNameGenerator.ReplaceUnderscores.class)` : Test Name에 method 이름에서 `_`를 지운 이름을 사용한다. 

### @DisplayName
- Test method 이름만으로 Test의 내용을 모두 표현하기는 어렵다.
- Test method의 이름을 직접 지정해준다.(한글, 이모지 등 사용가능)
- @DisplayNameGeneration 보다 우선순위가 높다.
- `@DisplayName("스터디 만들기 😍")`

---

### 예제 코드
```java
package me.rawk.inflearnthejavatest;
import org.junit.jupiter.api.*;
import static org.junit.jupiter.api.Assertions.*;

class StudyTest {

    @Test
    @DisplayName("스터디 만들기 😍")
    // Test Name: 스터디 만들기 😍
    void create_new_study() {
        Study study = new Study();
        assertNotNull(study);
        System.out.println("Create");
    }

    @Test
    @DisplayNameGeneration(DisplayNameGenerator.ReplaceUnderscores.class)
    // Test Name: create new study again
    void create_new_study_again() {
        System.out.println("Create2");
    }

    @Test
    @Disabled
    void create3() {
        System.out.println("Create3");
    }

    @BeforeAll
    static void beforeAll() {
        System.out.println("Before All");
    }

    @AfterAll
    static void afterAll() {
        System.out.println("After All");
    }

    @BeforeEach
    void berforeEach() {
        System.out.println("Before Each");
    }

    @AfterEach
    void afterEach() {
        System.out.println("After Each");
    }

}

```

### 실행 결과
```
Before All

Before Each
Create
After Each


Before Each
Create2
After Each




void me.rawk.inflearnthejavatest.StudyTest.create3() is @Disabled

After All
```


<br><br><br><br>

이 포스트는 [JUnit5 공식문서][JUnit]와 [더 자바, "코드를 테스트 하는 다양한 방법" - 백기선님][Baik] 을 참고하여 작성하였습니다.

[JUnit]: https://junit.org/junit5/docs/current/user-guide/
[Baik]: https://www.inflearn.com/course/the-java-application-test#











