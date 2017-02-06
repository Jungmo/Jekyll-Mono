---
layout: post
title: Git helpful command
data: 2016-07-13
categories: Git   
---
git 쓸 때 유용했던 커맨드들 정리

## Git Ignore 제대로 안 먹힐 때

```Bash
$ git rm -r --cached .
$ git add .
$ git commit -m "fixed untracked files"
```

이미 저장소에 push 되어있는 내용을 삭제해준다..

출처 : [theeye's blog](http://theeye.pe.kr/archives/2091)

## Github push 되돌릴때

git push -f origin HEAD^:master
