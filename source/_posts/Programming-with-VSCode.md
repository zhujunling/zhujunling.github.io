---
title: Programming with VSCode
date: 2019-11-05 23:34:19
categories:
- Development
tags:
- Tools
---

### 1. C/C++——微软C/C++ for Visual Studio Code
+ Mingw-w64——http://mingw-w64.org/doku.php/download/mingw-builds （MinGW只能编译生成32位，已停止更新）
+ 环境变量path——C:\Program Files (x86)\mingw-w64\i686-8.1.0-posix-dwarf-rt_v6-rev0\mingw32\bin
cmd输入gcc或者g++命令验证。

+ 建立并进入Workspace文件夹，通过cmd命令code .，新建一个main.c文件写简单c代码并保存。
+ vscode中View > Command Palette（Ctrl+Shift+P）：
输入C/C++，在列表中选择编辑配置Edit Configurations，将会打开c_cpp_properties.json文件。
+ 输入task，在列表中选择 Tasks: Configure Default Build Task，将会打开tasks.json文件。
${file}      ${fileDirname}/${fileBasenameNoExtension}    
"isDefault": true 表示可以通过Ctrl+Shift+B运行这个任务，否则要通过Command Palette运行 "Tasks: Run Build Task"。
+ vscode中左侧调试按钮（Ctrl+Shift+D）：设置——选择C++（GDB/LLDB），将会打开launch.json文件。
program：${workspaceFolder}/${fileBasenameNoExtension}
stopAtEntry：调试时默认在第一行设置断点，默认为true。
miDebuggerPath：设置为C:\\Program Files (x86)\\mingw-w64\\i686-8.1.0-posix-dwarf-rt_v6-rev0\\mingw32\\bin\\gdb.exe
按Ctrl+Shift+B进行编译，调试菜单——启动调试（快捷键F5），先点左侧调试按钮然后点击小绿色三角。
调试程序system("pause"); 或者可在return 0前面加断点。
+ .vscode隐藏文件夹通常包含了各种配置文件，settings.json，选择vscode资源管理器打开对应文件夹即可应用此文件夹配置。
---
### 2. Python——微软Python extension for Visual Studio Code
+ Command Palette (Ctrl+Shift+P)使用命令Python： Select Interpreter选择使用的python版本 , 或者通过状态栏选择（如可用）。手动设置： File > Preferences > Settings command (Ctrl+，) 。
+ 建立并进入Workspace文件夹，通过cmd命令code .  （# open code with current directory），新建一个py文件写简单代码并保存。
+ 使用vscode的终端输入命令：View | Terminal   （Ctrl+`）
+ 调试：设置断点，点击调试图标，可点击debug的设置图标configure launch.json进行调试器的配置。
点击绿色箭头即可开始调试，如果程序代码有输入，则可在下拉列表中选择外部终端进行输入。
---

### 3. Latex
+ TeX Live环境变量：<目录>texlive\2019\bin\win32，命令行输入 tex -v 验证安装。
+ 建立工作目录，通过cmd命令code .，新建一个tex文件并保存。
+ 配置VSCode的LaTeX Workshop插件，编辑 .vscode 目录中的settings.json。