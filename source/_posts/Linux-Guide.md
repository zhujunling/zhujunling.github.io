---
title: Linux Guide
date: 2019-11-04 17:32:23
tags:
- linux
---
1. 常用命令
``` bash
$ sudo su
$ du -sh
$ which
$ whereis
$ sudo shutdown -h/-r now
$ sudo service --status-all
$ ps -ef | grep ssh 
$ tar –xvf (tar) /   -xzvf (bz)  / -xjvf (bz2)  /  -xJvf  (xz)
$ curl
```
2. vi
3. internet/ssh/git/vscode  configure
``` bash
# /etc/network/interfaces
auto wlan0
iface wlan0 inet dhcp [ static ] 
[  address 192.168.1.X
   netmask 255.255.255.0
   gateway 192.168.1.1  ]
wpa-essid Wi-Fi名称     [WEP认证方式：wireless-essid Wi-Fi名称]
wpa-psk Wi-Fi密码       [WEP认证方式：  wireless-key Wi-Fi密码]
```
``` bash
sudo service ssh status[start]
# /etc/ssh/sshd_config
```
``` bash
git  config  --list
ssh  -T  git@github.com  
```