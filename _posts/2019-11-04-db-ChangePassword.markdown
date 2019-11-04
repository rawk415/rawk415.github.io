---
layout: post
title: "MySQL 5.7이상 비밀번호 변경방법"
subtitle: "How to change MySQL Password"
categories: devlog
tags: db
---

1. mysql에 로그인한다.
> mysql -uroot -p
계정이 기억나지 않으면 이 구문을 실행하고 password에 아무것도 치지않으면 들어가진다.


2. mysql db에 접근
> use mysql;

3. 비밀번호 변경
> ALTER user 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'newPW';

4. 변경 내역 저장
> flush privileges;




