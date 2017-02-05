---
layout: post
title: Raspberry Pi OS설치
data: 2016-04-26
categories: Raspberry Pi   
---

1. 라즈베리파이 홈에서 OS image 다운로드.
2. diskutil list로 현재 마운트되어있는 디스크 확인.
3. 연결한 SD카드를 umount함. (sudo umount /dev/disk2s1)
4. sudo dd bs=1m if=2016-03-18-raspbian-jessie-lite.img of=/dev/disk2
5. 기다리면 다 구워짐 끝!