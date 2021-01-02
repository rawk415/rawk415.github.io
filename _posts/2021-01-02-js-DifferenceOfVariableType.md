---
layout: post
title: "var, let, const 차이"
subtitle: "js"
categories: devlog
tags: js
---
## var
var은 js에서 변수의 자료형의 기본으로 쓰였지만, 문제점 때문에 최근에는 거의 사용하지 않는다.   
var은 재할당이 가능해 상수로 쓸 수 없고, 심지어는 재선언에도 문제가 없게된다.

```js
var a = 10;
var a = 20; // 재선언 가능
a = 30; // 재할당 가능
console.log(a);
```

이를 위한 해결책으로 let과 const의 개념을 새로 도입했다.

## let
let은 재할당은 가능하고, 재선언은 불가능하다. 일반적인 변수를 생각하면 된다.   
선언 후 나중에 초기화 해주어도 된다.

```js
let a = 10;
let a = 20; // Uncaught SyntaxError:Identifier 'a' has already been declared. 재선언 불가능
a = 30; // 재할당 가능
console.log(a);
```

## const
const는 재할당, 재선언 모두 불가능한 상수를 만드는 자료형이다.   
또한 상수이기 때문에 반드시 선언과 동시에 초기화 해주어야한다.

```js
const a = 10;
const a = 20; // Uncaught SyntaxError:Identifier 'a' has already been declared. 재선언 불가능
a = 30; // Uncaught TypeError:Assignment to constant variable. 재할당 불가능
console.log(a);
```
