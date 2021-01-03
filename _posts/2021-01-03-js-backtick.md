---
layout: post
title: "JS Backtick"
subtitle: "js"
categories: devlog
tags: js
---
## Backtick ``
backtick 이라고 부르는 이 기호(``)는 JS에서 문자열을 표현할 때 "", '' 같이 사용할 수 있는 기호로,    
문자열 안에 변수 등의 표현식을 넣을 수 있어서, 표현에 있어 따옴표들보다 편하다는 강점이 있다.   
작은 따옴표와 비슷하게 생겼지만 다르므로 주의해야한다.

```js
const num1 = 10;
const num2 = 20; 
const num3 = num1 + num2;

console.log("plus: " + num1 + " + " + num2 " = " + num3); // plus: 10 + 20 = 30
console.log(`plus: ${num1} + ${num2} = ${num3}`);         // plus: 10 + 20 = 30
```

따옴표를 사용할 때처럼 따옴표를 열고 닫기, 띄어쓰기에 민감하게 신경쓰지 않아도 된다.   
위와 같이 사용하고 싶은 변수는 **${VariableName}** 이렇게 표현하여 그냥 백틱의 문자열에 함께 사용하면 된다.

