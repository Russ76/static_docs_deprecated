---
title: 'hFramework library development'
platform: 'CORE2'
autotoc: true
layout: layout.hbs
page: 'Tutorials'
order: 3
---

# hFramework library development #

If you like to develop [hFramework](https://github.com/husarion/hFramework) together with our community, or to adapt it to your purposes, this is a tutorial for you.

## hFramework sourcecode compilation ##

1. Download current version of hFramework on your computer.
(Github link: https://github.com/husarion/hFramework)
2. Unpack downloaded file.
3. Open Visual Studio Code. Close open project if you have one already loaded.
4. Instal Husarion plugin for Visual Studio Code.
5. Press Ctrl+Shift+p. Then type “flash project to CORE2” and press Enter to accept. Terminal window on the bottom should open.

or

Find terminal tab on bottom and click on it. Then type 
> set PATH=%PATH%;C:%HOMEPATH%\.vscode\HusarionTools\bin;
6. Use cd command to change directory to folder you previously unzip.
example: >cd C:\Users\husarion\Downloads\hFramework-master\hFramework-master
7. Type
> mkdir build\stm32_core2_1.0.0\

> cd build\stm32_core2_1.0.0\

> cmake ../.. -DBOARD_TYPE=core2 -DPORT=stm32 -DHFRAMEWORK_PATH=. -GNinja
8. Type
>ninja
9. Compiler should run and create static library for hFramework.
If you find on terminal line like below compilation succeed.
![image](/assets/img/howToStart/lib_p9.png)

## Using the library compiled by yourself ##

1. Create new folder for your project.
2. In VSCode File -> Open Folder
![image](/assets/img/howToStart/com_p2.png)
In open window find directory of your new project.
Project tree should be empty.
3. Press Ctrl+Shift+p
Small console will open on top.
4. Type “Create Husarion project” and press Enter to accept.
5. In project tree you should find similar files like this on photo below.
![image](/assets/img/howToStart/com_p5.png)
6. Open CMakeLists.txt and remove line "enable_module(hCloudClient)".
7. Open main.cpp ana nied remove lines "#include "hCloudClient.h" and "platform.begin(&RPi);".
(This lains contain functions use to connect platform to cloud, you can add them after first compilation).
8. Press Ctrl+Shift+p and type “Husarion project variable” and press Enter.
9. Type “HFRAMEWORK_PATH” and press Enter.
10. Type path to hFramework directory.
example: C:/Users/husarion/Downloads/hFramework-master/hFramework-master
11. Press Ctrl+Shift+b to compile your project. If everything goes alright, no message should pop up and in project tree you should find myproject.bin, myproject.elf and myproject.hex file.