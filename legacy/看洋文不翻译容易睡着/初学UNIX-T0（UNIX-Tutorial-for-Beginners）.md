#####UNIX介绍
UNIX是一个通用的操作系统。说到操作系统，就是是使得计算机硬件运行起来的一整套软件系统。UNIX的应用主要是在工作站和学校里的多用户服务器。
UNIX主要是由三个部分组成：内核（kernel），壳（shell），还有程序（program）。

内核：UNIX操作系统的核心就是内核，他会将内存和时间片分配给程序，处理文件系统还有系统调用的通信。

内核和壳程序（shell）总是协同工作的，假设用户输入了命令rm myfile（效果就是删除磁盘上的myfile文件）。shell程序首先会搜索文件系统，找找有没有程序rm，之后会对内核发起请求，通过系统调用执行程序rm来处理文件myfile。当进程rm myfile运行结束，shell就会返回到UNIX提示符，表示等待用户的下一个命令输入。

壳（shell）：shell的角色是用户和内核之间的接口界面。用户登录的时候，计算机检查用户名和口令之后就会调用另一个程序shell。shell就是一个命令行解释器（command line interpreter，CLI）。用户输入的命令都会由shell来解释执行。这些命令本身也就是程序，命令运行结束之后，shell就会回到提示符（一般是%，还有$）。

高级用户可以定制自己要使用的shell，在一个机器上也可以使用不同种类的shell。一般学校里的学生默认使用的是tcsh shell。
tcsh有一些帮助用户来输入命令的功能。
文件名补全-输入部分文件名，然后按[Tab]键，他就会自动补全剩下的文件名。如果有超过一个以上的文件名符合你的部分的话，系统就出一个提示音，来提示输入更多的信息，然后在按{Tab]键。
历史命令-shell会保留以前输入过的命令，只要按下箭头上就可以回滚到上一条命令了。
文件和进程：凡是UNIX中的，不是文件就是进程。
一个进程是指由唯一的PID（进程ID）来定义的一个执行程序。
文件就是数据的集合，一般是由用户或者编译器等等来创建的。
文件举例：
- 一个文档（报告，论文等等）
- 高级语言所编写的程序文本
- 二进制文件，可以直接解释为机器指令的可执行程序
- 一个目录，包含他内容的一些信息，其中可能有其他目录（子目录）和一些文件

目录结构：所有的文件都由目录结构组织在一起。文件系统就是被组织成一个侧此结构，就像一颗倒过来的树。树的顶部一般是被称为根（root）。
