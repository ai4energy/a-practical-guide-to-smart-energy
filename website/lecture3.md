@def title = "第3讲 云服务基础"

# 云服务基础

\tableofcontents

## Linux简介

Linux是服务器端广泛使用的操作系统。
### linux的起源

Unix最初受到Multics计划的启发。Multics是由麻省理工学院、通用电气和贝尔实验室合作进行的操作系统项目。该计划要创建一套多用户、多任务、多层次（multi-user、multi-processor、multi-level）的MULTICS操作系统。但由于目标过于庞大，糅合了太多的特性，但是性能都很低。1969年贝尔实验室决定退出这个计划。

UNIX操作系统，是一个强大的多用户、多任务操作系统，支持多种处理器架构，按照操作系统的分类，属于分时操作系统，最早由肯·汤普逊、丹尼斯·里奇等在贝尔实验室开发。Unix中，Multics的许多功能都被采纳，重新实现。对应于Multics，该系统最早戏称为“UNiplexed Information and Computing System”，缩写为“UNICS”。后来布莱恩·柯林汉提议改名为UNIX。

1983年，理查德·斯托曼提出GNU计划，希望发展出一套完整的开放源代码操作系统来取代Unix。

RMS是自由软件活动家。他发起自由软件运动，倡导软件用户能够对软件自由进行使用、学习、共享和修改，确保了这些软件被称作自由软件。斯托曼发起了GNU项目，并成立了自由软件基金会。他开发了GCC、GDB、GNU Emacs，同时编写了GNU通用公共许可协议。

1989年，GNU项目中的其他部分，如编辑器、编译器、Shell等都已经完成，独缺操作系统核心。1990年，自由软件基金会开始正式发展内核Hurd。

1991年芬兰大学生林纳斯·托瓦兹在GNU通用公共许可证下发布了最初是为自己创作的Linux操作系统内核，暂时替代了GNU计划的Hurd内核。至此，GNU计划基本完成，此操作系统被命名为GNU/Linux。这类操作系统常常被称为Linux。斯托曼坚持认为 Linux 应该被称作 GNU/Linux，因为 GNU 项目更早出现，且在 Linux 操作系统的早期，GNU 社区的源代码在其中起了关键的作用，例如 GCC 编译器。

### Linux的基本知识

### Linux的发行版

## 虚拟机

云服务器通常也是某种意义上的虚拟机。

虚拟机（Virtual Machine）指通过软件模拟的具有完整硬件系统功能的、运行在一个完全隔离环境中的完整计算机系统。在实体计算机中能够完成的工作在虚拟机中都能够实现。在计算机中创建虚拟机时，需要将实体机的部分硬盘和内存容量作为虚拟机的硬盘和内存容量。每个虚拟机都有独立的CMOS、硬盘和操作系统，可以像使用实体机一样对虚拟机进行操作。

流行的虚拟机软件有VMware、VirtualBox和Virtual PC，它们都能在Windows系统上虚拟出多个计算机。
## 使用虚拟机安装Linux

我们使用VirtualBox来安装Ubuntu。

首先到[VirtualBox的官方站点](https://www.virtualbox.org/)下载[VirtualBox安装程序](https://download.virtualbox.org/virtualbox/6.1.16/VirtualBox-6.1.16-140961-Win.exe)和[扩展包](https://download.virtualbox.org/virtualbox/6.1.16/Oracle_VM_VirtualBox_Extension_Pack-6.1.16.vbox-extpack)。我们以Windows 10作为宿主机，顾下载Windows版本。

安装VirtualBox，然后安装扩展包。

打开VirtualBox，创建虚拟机。

到Ubuntu的官方站点下载iso安装文件。

虚拟机中加载光驱。启动虚拟机，开始安装。

虚拟机重启，安装增强功能。

设置宿主机和客户机文件共享。

## 云服务器及其使用

事实上云服务器也是虚拟机。我们购买一个阿里云ECS就是获得了一个虚拟机。以下我们展示一下如何在一个ECS云服务器上安装操作系统。

使用ssh登录ECS服务器。登录工具可以使用mobaxterm，文件传输工具可以使用filezilla。我们可以把云服务器设置成密匙登录加强安全。
## Linux下安装一个服务

在ubuntu下使用root用户，直接apt update，apt install nginx安装一个nginx服务器。这样我们就可以通过ECS的ip地址访问这个网页了。但是需要注意的是阿里云的安全组规则也许关闭了对应的端口，需要去打开。
## Docker及其使用

### Docker简介

### 运行一个Docker

### Docker的编排docker-compose

### Docker的Dockfile

### 从docker到k8s

## WSL2

事实上，以上这些都是为了理解云服务器就是个虚拟机，在虚拟机上可以使用docker开启各式各样的服务。而为了方便练习，显然在本地最好了。microsoft的确是开源巨人，github是他家的，windows也可以直接运行linux系统了。这就是WSL。WSL现在已经是版本2了，比较好用。