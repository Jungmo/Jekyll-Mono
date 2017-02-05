---
layout: post
title: Use argument in Python
data: 2016-07-15
categories: python
---

```
import argparse

parser = argparse.ArgumentParser()

parser.add_argument('--path', type = str, default='.', help='blahblah')
parser.add_argument('--path2', type = str, default='.', help='blahblah')
parser.add_argument('--id', type = str, default='jack', help='blahblah')
parser.add_argument('--password', type = int, default='123', help='blahblah')

args = parser.parse_args()

print args.id
```

argparse를 import해주고 parser를 만든다.

```
parser.add_argument('--path', type = str, default='.', help='blahblah')
```
add_argument로 argument의 이름, 타입, 기본값, 도움 메세지를 적어준다.

도움 메세지의 경우 --help argument를 사용하면 표시되는 메세지이다.