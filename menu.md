
# (1) Abstraction Is Good But Don’t 
### Most CS and CE courses emphasize abstraction

Abstract data types

Asymptotic analysis

### These abstractions have limits

Especially in the presence of bugs

Need to understand details of underlying implementations

### Useful outcomes from taking 213

Become more effective programmers

Able to find and eliminate bugs efficiently

Able to understand and tune for program performance

Prepare for later “systems” classes in CS & ECE

Compilers, Operating Systems, Networks, Computer Architecture, Embedded Systems, Storage Systems, etc.

# 1.1 computer 
### Does not generate random values

Arithmetic operations have important mathematical properties

### Cannot assume all “usual” mathematical properties

Due to finiteness of representations

Integer operations satisfy “ring” properties

Commutativity, associativity, distributivity

Floating point operations satisfy “ordering” properties

Monotonicity, values of signs

### Observation

Need to understand which abstractions apply in which contexts

Important issues for compiler writers and serious application programmers


# (2) You’ve Got to Know Assembly
### 有可能，你永远不会在汇编中编写程序

编译器比你更好，更耐心

### 但是：了解程序集是机器级执行模型的关键

存在错误的程序行为

高级语言模型崩溃了

调整程序性能

理解编译器完成/未完成的优化

了解程序无效率的来源

实施系统软件

编译器将机器代码作为目标

操作系统必须管理进程状态

创建/对抗恶意软件

x86汇编是首选语言！

# (3)C和C ++不提供任何内存保护
超出范围的数组引用

指针值无效

滥用malloc /免费

## 可能导致讨厌的错误

bug是否有任何影响取决于系统和编译器

远距离行动

损坏的对象在逻辑上与正在访问的对象无关

可以在生成之后很久就观察到bug的影响

我怎么处理这个？

程序使用Java，Ruby，Python，ML，......

了解可能发生的交互

使用或开发工具来检测引用错误（例如Valgrind）

# (4)：性能比渐近的复杂性更重要
常数因素也很重要！

甚至精确的操作数也不能预测性能

根据编写代码的方式轻松查看10：1的性能范围

必须在多个级别进行优化：算法，数据表示，过程和循环

必须了解系统以优化性能

程序如何编译和执行

如何衡量计划绩效和识别瓶颈

如何在不破坏代码模块性和通用性的情况下提高性能


#(5) Computers do more than execute programs

### 他们需要获取数据

I / O系统对程序可靠性和性能至关重要


### 他们通过网络相互沟通

存在网络时会出现许多系统级问题

自治进程的并发操作

应对不可靠的媒体

跨平台兼容性

复杂的性能问题


# （5.1）
### 复杂的性能问题

大多数系统课程都是以Builder-Gentric

计算机架构

在Verilog中设计流水线处理器  
- Verilog是一种用于描述、设计电子系统（特别是数字电路）的硬件描述语言，主要用于在集成电路设计，特别是超大规模集成电路的计算机辅助设计

操作系统

实现操作系统的示例部分

编译器

编写简单语言的编译器

联网

实现和模拟网络协议


# topic and lab

### Programs and Data
比特操作，算术，汇编语言程序

C控制和数据结构的表示

包括架构和编译器的各个方面

L1（datalab）：操作位

L2（bomblab）：解散二进制炸弹


### The Memory Hierarchy
话题
内存技术，内存层次结构，缓存，磁盘，位置
包括架构和操作系统方面

分配
L4（cachelab）：构建缓存模拟器并优化局部性。
了解如何利用程序中的位置。


### Exceptional  Control Flow
话题
硬件异常，进程，进程控制，Unix信号，非本地跳转
包括编译器，操作系统和体系结构的各个方面

分配
L5（tshlab）：编写自己的Unix shell。
并发的第一个介绍


###  Virtual Memory
话题
虚拟内存，地址转换，动态存储分配
包括架构和操作系统方面

L6（malloclab）：编写自己的malloc包
真正感受系统级编程

### Networking, and Concurrency(高并发)
 网络和并发
话题
高级和低级I / O，网络编程
互联网服务，Web服务器
并发，并发服务器设计，线程
I / O与select复用
包括网络，操作系统和架构等方面

L7（proxylab）：编写自己的Web代理
学习网络编程以及有关并发和同步的更多信息。

### source
实验室由CMU Autolab系统提供
项目页面：http：//autolab.cs.cmu.edu
由CMU教师和学生开发
主要思想：自动编排和记分板
自动编辑：为您提供即时反馈。
记分板：实时，排序和匿名摘要。
每学期有3,000多名学生使用
使用Autolab，您可以使用Web浏览器：
下载实验室资料
通过Autolab服务器处理您的自动编码代码
查看班级记分牌
查看代码手柄的完整历史记录，自动生成的结果，教师的评估和成绩簿。
查看样式点代码的TA注释。