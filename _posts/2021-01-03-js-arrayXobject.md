---
layout: post
title: "JS Array(배열) & Object(객체)"
subtitle: "js"
categories: devlog
tags: js
---
## Array (배열)
Array는 배열이라는 뜻과 동일하게 여러 변수들을 나열해놓을 수 있다.   
JS에서는 자료형에 상관없이(String, int, Variable 등) 나열 가능하다.   
[ ]로 감싸고 Comma(,)로 구분한다.   
특정 위치의 원소를 꺼내고 싶을 땐 **배열명[원소번호]** 라고 작성하면 되고,   
**원소 번호(인덱스)는 0부터 시작이다.**

```js
const language= "JAVA"
const myFavorite = ["peach", 7, language];
// myFavorite[0] = peach
// myFavorite[1] = 7
// myFavorite[2] = JAVA

console.log(myFavorite);    // [ 'peach', 7, language ]
console.log(myFavorite[2]); // JAVA
```

## Object (객체)
Array를 사용할 경우 어떤 값이 몇 번째 인덱스인지를 외워야하는 단점이 있는데,   
Object는 Key와 Value를 가지기 때문에 이를 보완할 수 있다.   
{ }로 감싸고, Comma(,)로 구분한다.   
Key값은 String이더라도 따옴표("")로 감싸지 않아도 된다.   
또한 원하는 Key값을 불러 쉽게 해당 값을 호출할 수 있다.

```js
const rawkInfo = {
  name: "rawk",
  age: 24,
  favoriteMovie: [
    {
      name: "Darknight",
      director: "Christopher Nolan"
    },
    {
      name: "Parasite",
      director: "Bong Joon Ho"
    }
  ], // (,)를 빼먹어선 안된다.
  hasGirlfriend: true
}

console.log(rawkInfo.age); // 24
console.log(rawkInfo.favoriteMovie[1].name); // Parasite

```

