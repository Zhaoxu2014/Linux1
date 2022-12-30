---
title: 赵旭的Linux大作业
---

## 部分学习笔记
**Linux的一些基础命令**
1、cd：切换目录命令（cd /home）
2、ls ：列出目录的文件信息（ls -l）
3、cat ：查看文件全部内容（cat test.txt）
4、tail ：查看文件指定行数内容（tail -n 10 test.txt）
5、touch：创建文件（touch test.txt）
6、mkdir：创建文件夹（mkdir testdir）
7、cp：复制文件或文件夹（cp test.txt > newtext.txt）
8、mv ：移动文件或文件夹（mv test.txt > /dir）
9、rm：删除文件或文件夹（rm test.txt或rm -rf testdir）
10、find：查找文件（find / -name test.text）
11、vi：编辑文件（vi test.txt）
12、rename：文件重命名（rename test.txt  newtext.txt）
13、chmod：文件权限修改（chmod 777 text.txt）
14、history：最近历史执行过的命令（history）
15、wget：下载网络资源文件（wget http://xzwk.cn/test.txt）
16、top：查看资源实时用量情况（top）
17、logout：注销（logout）
18、reboot：重启（reboot）
19、shutdown： 定时关机（shutdown -s -t 3600 //3600秒后关机）
20、poweroff： 立即关机（poweroff）

**Linux下编写C语言**
概念：Linux下C语言编程常用的编辑器是vim，编译器一般用gcc，编译链接程序用make，跟踪调试一般使用gdb，项目管理用makefile。
1、vim编辑hello.c
输入代码下载vim（sudo apt install vim）
下载完成后进入编辑界面，开始c程序编辑（vim hello.c）
![csdn](https://img-blog.csdnimg.cn/e52312d1699548f99d8774a8f66d8f5a.png)
然后用esc退出编辑，输入wq，保存并退出

2、gcc编译器的使用
概念：GCC 编译工具链（toolchain）是指以 GCC 编译器为核心的一整套工具，用于把源代码转化成可执行应用程序。
它主要包含以下三部分内容：
• gcc-core：即 GCC 编译器，用于完成预处理和编译过程，例如把 C 代码转换成汇编代码。
• Binutils ：除 GCC 编译器外的一系列小工具包括了链接器 ld，汇编器 as、目标文件格式查看器 readelf 等。
• glibc：包含了主要的 C 语言标准函数库， C 语言中常常使用的打印函数 printf、 malloc 函数就在 glibc 库中。linux系统默认安装了GCC 编译工具链，windows系统可以通过安装，使用GCC工具。
用以下四个指令查看编译结果：
$ gcc -E hello.c -o hello.i
$ gcc -S hello.i -o hello.s
$ gcc -c hello.s -o hello.s
$ gcc hello.o -o hello
![csdn](https://img-blog.csdnimg.cn/35bbe15cfd7146b3b861a8e7adbc594a.png)
可以发现执行完后会在指定区域里面生成文件，生成了hello hello.c hello.i hello.o hello.s 5个文件
![csdn](https://img-blog.csdnimg.cn/ee0d5382f6c144d18f76919e58693141.png)
用这个代码查看结果（./hello）


## Linux操作系统大作业
**实验内容和要求**
1.在Linux下，安装git，使用git管理大作业相关的代码、配置文件等，要求有能反映大作业过程的git提交记录。
2.在Linu2.在Linux下，运行系统监控，查看常见的系统资源占用例如CPU、内存、网络、硬盘IO等等。
a)加分项：使用持久性监控面板动态显示系统状态。
3.Hexo是一个静态网站生成器，官网为：https://hexo.io/zh-cn/，查阅相关资料，在Linux下，完成以下内容：
a)配置好Hexo相关环境
b)使用Markdown语法编写网站内容，至少要包含的内容：Linux课程中的学习笔记、大作业完成步骤记录，且要求有相关图片、代码或命令
c)使用Hexo，将上述内容生成静态网站，部署到Web服务器（如Nginx或Apache），访问Web服务器，测试可以正常访问。
以下加分项2选1：
d)加分项1：使用容器技术（如Docker或Podman）部署上述静态网站，测试可以正常访问。
e)加分项2：部署上述静态网站，使其可以公网访问，可以是自己的云服务器，或者一些免费的托管平台，如gitee pages、github pages。
4.加分项：录制视频，对大作业进行演示和讲解，如git log讲解、监控程序演示和讲解、静态网站演示、配置文件讲解等，视频配有每个步骤的语音讲解，讲解越详细加分越多。
**实验步骤**
1、安装git
![csdn](https://img-blog.csdnimg.cn/img_convert/30cb4eb2010f5c681a161e54b92544ad.png)
![csdn](https://img-blog.csdnimg.cn/img_convert/ca596758faa7a636beae28c00f1125d5.png)
2、配置git
![csdn](https://img-blog.csdnimg.cn/img_convert/a2f31791676125ef8f476bfef53b7523.png)
![csdn](https://img-blog.csdnimg.cn/img_convert/2394508a892404f3d9b0d955e6d2981c.png)
3、使用git
![csdn](https://img-blog.csdnimg.cn/img_convert/4185497e420e6219086673ce4cdab2a8.png)
![csdn](https://img-blog.csdnimg.cn/img_convert/54ac96bd9976ece7a6c1f5150fe2893d.png)
4、top命令监控系统状态
![csdn](https://img-blog.csdnimg.cn/img_convert/4e964b14d656cf9c93b4085567048097.png)
5、综合监控
![csdn](https://img-blog.csdnimg.cn/img_convert/83a8695156c596f794237ec917fe398f.png)
6、内存监控
![csdn](https://img-blog.csdnimg.cn/img_convert/a0ad588d5b85e5ed2d6152b5042f30e3.png)
7、网络监控
![csdn](https://img-blog.csdnimg.cn/img_convert/10a20fc4bd4df699da7432d5ef6afb4b.png)
8、硬盘IO监控
![csdn](https://img-blog.csdnimg.cn/img_convert/13d3d8b69dfea681676e3776a83f3a3b.png)
9、磁盘空间监控
![csdn](https://img-blog.csdnimg.cn/img_convert/c13db2da875bf6a09fb50a142849186c.png)
10、配置hexo环境
![csdn](https://img-blog.csdnimg.cn/img_convert/0ab4c7c54a7ef910f10dbe0c97ab3959.png)
![csdn](https://img-blog.csdnimg.cn/img_convert/56e92f7393bd2eb1ce40405f2ada8321.png)
![csdn](https://img-blog.csdnimg.cn/img_convert/d829ae0e704b96aea1d19f5214f904fe.png)
![csdn](https://img-blog.csdnimg.cn/img_convert/28a932ad7894b74cb6ef6ce99b237574.png)
11、生成静态网页和运行本地服务器
![csdn](https://img-blog.csdnimg.cn/img_convert/acf78f765b37b3ca5f02fa402719be5b.png)


