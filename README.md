# 手写一个简单的操作系统

## Day 1

### 环境搭建

* VirtualBox安装Ubuntu 20.04.3
* VSCode远程连接Ubuntu
* 安装编译链接工具

### 遇到的问题：

修改/boot/grub/grub.cfg文件后，重启Ubuntu后无法选择自己写的操作系统。

解决方案：

step1:

  在修改文件前，先进入/etc/default/grub文件，修改三个地方。
  
  ```
  GRUB TIMEOUT STYLE = menu
  GRUB TIMEOUT = 30
  GRUB CMDLINE LINUX DEFAULT = "text"
  
  sudo update-grub
  ```
  
step2:

  修改grub.cfg文件。
  
### 运行展示
启动界面

![image](https://github.com/xiao-yang25/myos/assets/92993462/71fea927-1af3-47f9-9e00-599c5d4d2b9d)

运行My Operating System

![image](https://github.com/xiao-yang25/myos/assets/92993462/1850f765-b268-4784-91b1-4dffe293d25b)

### 参考资料

【油管】Write your own Operating System

【B站】自己动手写一个操作系统(上面的加字幕版）

【B站】使用c++编写操作系统（基础知识上解释更详细，油管中文翻版，作为补充）


