---
layout: post
title: Raspberry Pi Wifi 연결하기
data: 2016-04-26
categories: Raspberry Pi   
---

sudo nano /etc/wpa_supplicant/wpa_supplicant.conf

```
network={
	ssid="SSID"
	psk="PASSWORD"
}
```
추가해주기.