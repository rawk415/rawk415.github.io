---
layout: post
title: "JUnit5 Test 작성"
subtitle: "JUnit5 Writing Tests"
categories: devlog
tags: java
---

# 2. 테스트 작성
아래의 예제 코드는 JUnit Jupiter로 테스트를 작성하는 최소한의 요구사항을 보여준다.

```Java
// A first test case
import static org.junit.jupiter.api.Assertions.assertEquals;
import example.util.Calculator;
import org.junit.jupiter.api.Test;

class MyFirstJUnitJupiterTests {

    private final Calculator calculator = new Calculator();

    @Test
    void addition() {
        assertEquals(2, calculator.add(1, 1));
    } // 2와 calculator.add(1, 1)의 결과가 같은지를 비교해 같으면 테스트 성공, 다르면 테스트 실패.

}
```
JUnit5부터는 class와 method에 public을 붙이지 않아도 동작한다. (private이더라도 reflection으로 접근이 가능하기 때문)


<br><br><br><br>

이 포스트는 [JUnit5 공식문서][JUnit]와 [더 자바, "코드를 테스트 하는 다양한 방법" - 백기선님][Baik] 을 참고하여 작성하였습니다.

[JUnit]: https://junit.org/junit5/docs/current/user-guide/
[Baik]: https://www.inflearn.com/course/the-java-application-test#