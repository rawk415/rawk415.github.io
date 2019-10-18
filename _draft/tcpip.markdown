---
layout: post
title: "TCP/IP TEST"
subtitle: "tcpip"
categories: tip
tags: tip
---

## 파일 디스크립터 `File Descriptor`
시스템으로부터 할당받은 소켓에 부여된 정수를 의미  
- 0번 : 표준입력(Standard Input)
- 1번 : 표준출력(Standard Output)
- 2번 : 표준에러(Standard Error)

0~2번 파일 디스크입터는 항상 사용중이므로 새로운 소켓을 `open()`하면 3번부터 생성된다.



```linux
# open 함수
# open("파일", 오픈 모드)
open("file.txt", O_CREAT | O_WRONLY | O_TRUNC) 

# close 함수
# close(fd);


```
