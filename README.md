# Unix Network Programming UNIX网络编程源码&读书笔记

## 简介
春招计划第三弹。
[原代码](https://github.com/DingHe/unpv13e)中不能正常运行的错误已修改，直接按照环境搭建步骤进行即可。

## 环境
- linux 18.04
  - 下载本项目到本地并进入文件夹
  
  - 更改configure权限使其可执行
  
  - 编译lib文件：
    - cd lib
    - make
    - cd ../libfree
    - make
    - cd ../libgai
    - make
  - 设置全局环境
    - cd .. // 回到主目录
    - sudo vim lib/unp.h // 修改unp.h , 将#include “../config.h”修改为 #include “config.h”
    - sudo cp config.h /usr/local/include
    - sudo cp lib/unp.h /usr/local/include
    - sudo cp libunp.a /usr/local/lib
  - 测试intro中的代码
    - 首先安装xinet.d
      - sudo apt install xinet.d
    - 编辑daytime
      - vi /etc/xinetd.d/daytime // 将两个disable的 yes 改为 no
    - 重启xinetd
      - service xinetd restart
    - 测试
      - ./daytimetcpcli 127.0.0.1 //得到正确结果

## 运行


