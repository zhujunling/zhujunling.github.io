---
title: ARM_Linux
date: 2019-11-05 10:32:43
categories:
- Development
tags:
- Embedded System
- IoT
---

+ 交叉编译工具链主要由binutils、gcc和glibc（uClibc-ng、musl和 newlib）三部分组成。
---
+ 命名规则：arch [-vendor] [-os] [-(gnu)eabi]——（Embedded Application Binary Interface）   
   1. gcc-arm-linux-gnueabihf ——linux armhf（arm hard float，arm64默认hf）——使用glibc或musl库
   2. gcc-arm-linux-gnueabi——linux armel（arm eabi little endian）——使用glibc或musl库
   3. gcc-arm-none-eabi——裸机开发环境——基于newlib库：
   4. https://developer.arm.com/open-source/gnu-toolchain/gnu-rm/downloads
   5. https://launchpad.net/~team-gcc-arm-embedded/+archive/ubuntu/ppa
---
+ The C library实现了传统的POSIX API通过system calls访问内核并提供higher-level services。  
   + ANSI（American National Standards Institute）== ISO C
   + C标准库（标准C89/C99/C11） ——POSIX C库（C标准库超集）——GLIBC
   + 
![alt](/images/LinuxC.png)
+ 制作arm交叉编译工具链：arm-linux-gnueabihf-gcc -v
   1. 分步架构——分步编译和安装工具链所需要的库和源码，各种依赖及补丁导致问题多困难。
   2. 脚本工具架构——使用crosstool-ng脚本、Buildroot、 Yocto等构建工具。
   3. 开源项目——apt-get（不可重定位）、Linora、Codesourcery（Mentor）（Buildroot获取）——解压后添加环境变量