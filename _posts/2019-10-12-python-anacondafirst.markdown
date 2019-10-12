---
layout: post
title: "아나콘다 업데이트"
subtitle: "Python"
categories: devlog
tags: python
---

파이썬 라이브러리를 편하게 사용하기 위해서 `Anaconda`를 설치하는데 인터넷에서 설치 시 보통은 최신버전이 아닌 상태로 받아지고, 사용하다가도 업데이트가 종종 발생한다. 그럴 때 업데이트를 위해 사용하는 명령은 다음과 같다.

```
conda update -n root conda
conda update --all
```

`conda update -n root conda`로 아나콘다 자체를 업데이트하고   
`conda update --all`로 아나콘다의 모든 라이브러리를 업데이트 한다.