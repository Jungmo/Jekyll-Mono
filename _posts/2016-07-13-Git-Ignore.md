---
layout: post
title: Git ignore
data: 2016-07-13
categories: Git   
---

Git Ignore 제대로 안 먹힐 때 아래의 커맨드를 사용해본다.

```Bash
$ git rm -r --cached .
$ git add .
$ git commit -m "fixed untracked files"
```

이미 저장소에 push 되어있는 내용을 삭제해준다..

출처 : [theeye's blog](http://theeye.pe.kr/archives/2091)
