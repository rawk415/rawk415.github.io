---
layout: post
title: "IntelliJ 컴파일 시 args 세팅하는 방법"
subtitle: "IntelliJ"
categories: tip
tags: tip
---

cmd 창의 경우 java `클래스명` `args` 와 같이 입력해주면 쉽게 args를 입력할 수 있지만 IDE에서는 자동으로 실행하기 때문에 뒤에 추가 인수를 줄 수 없습니다.

따라서 Run하기 전에 args를 추가하는 방법을 사용합니다.

![alt-shift-f10] (https://github.com/rawk415/rawk415.github.io/blob/master/assets/img/Intellij-alt-shift-f10.png)

![alt-shift-f10] (https://github.com/rawk415/rawk415.github.io/blob/master/assets/img/Intellij-alt-shift-f10.png "alt+shift+f10")

`alt` + `shift` + `f10`키를 눌러 프로젝트를 선택한 후 실행이 아닌 오른쪽 방향키를 눌러 확장한 후 `Edit..`을 누룬다.


![Edit Configuration] (https://github.com/rawk415/rawk415.github.io/blob/master/assets/img/Intellij-edit-configuration.png "Edit Configuration")
`Edit configuration settings` 창이 뜨면 `configuration` 탭의 `Program arguments`에 원하는 args 들을 입력하고 아래쪽의 `RUN`을 눌러 실행하면 된다.