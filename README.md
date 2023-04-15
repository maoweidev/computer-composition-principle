```diff + hello ```
# 计算机组成原理课后习题答案与解析
## 习题1
### 1.1
	摩尔定律：“当价格不变时，集成电路上可容纳的晶体管数量大约18~24个月翻一番，性能也将提升一倍。”
	汇编器：汇编程序负责将汇编语言翻译成机器语言目标程序，也称为汇编器。
	编译器：编译程序负责将高级语言翻译成汇编语言，也称为编译器。
	解释器：解释程序负责用于将源程序中的语句按执行顺序逐条翻译成机器指令并执行，且不生成目标程序，也称为解释器。
	链接器：链接器是一个程序，将一个或多个由编译器或汇编器生成的目标文件外加库链接为一个可执行文件。
	时钟周期：时钟周期是计算机中最基本的、最小的时间单位。
	机器字长：计算机的字长一般是指CPU一次处理的数据位数，用二进制数的长度来衡量。
	主存容量：主存容量是指主存能存储的最大信息量。
	CPI:Clock Cycles Per Instruction，是执行每条指令所需要的平均时钟周期数。
	IPC:Instructions Per Cycle，是指每个时钟周期CPU能执行的指令条数，是CPI的倒数。
	MIPS:Million Instructions Per Second，即每秒百万条指令。
	MFLOPS:Million Floating-Point Operations Per Second，是指计算机每秒执行浮点数运算的次数。
	CPU时间：CPU执行时间也称CPU时间，是指CPU真正花费在该程序上的时间，又包括执行用户程序本身花费的CPU时间和为执
	行程序而花费在操作系统上的时间，很难精确区分一个程序执行过程中的用户CPU时间和系统CPU时间。
### 1.2
	（1）D，相比十进制，二进制的运算规则更简单，“0”和“1”两个状态更容易用物理状态实现，适合采用布尔代数的方法实现
	运算电路。
	（2）C，根据冯·诺依曼体系结构的基本思想可知，所有的数据和指令序列都是以二进制形式存放在存储器中，计算机根据
	周期来区分指
	令和数据，因此数据是从存储器读取而非在指令中给出，因此C项是错误的。
	（3）C，编译程序负责将高级语言翻译成汇编语言，也称为编译器。
	（4）A，机器语言是计算机唯一可以直接执行的语言。汇编语言属于低级语言，但其源程序必须要翻译成目标程序成为机器
	语言程序后才能被直接执行。硬件描述语言是电子系统硬件行为描述、结构描述、数据流描述的语言。
	（5）D，MFLOPS:Million Floating-Point Operations Per Second，是指计算机每秒执行浮点数运算的次数。
	（6）D，CPU时钟频率（主频)越高,完成指令的一个执行步骤所用的时间就越短，执行指令的速度越快。数据通路的功能是
	实现CPU内部的运算器和寄存器以及寄存器之间的数据交换，优化数据通路结构，可以有效提高计算机系统的吞吐量，从而
	加快程序的执行。计算机程序需要先转化成机器指令序列才能最终得到执行，通过对程序进行编译优化可以得到更优的指
	令序列，从而使得程序的执行时间也越短。
	（7）C，CPI=2*0.5+3*0.2+4*0.1+5*0.2=3，1.2GHz=1200MHz，MIPS=1200/3=400。
	（8）D，90/1.5+10=70秒。
	（9）D，T1=CPI*IC*T=20秒，T2=1.2CPI*0.7IC*T=0.84T1=0.84*20=16.8秒。
	（10）C，T=CPI*IC/f，使用同样的基准程序P，所以两次的IC相同，T1/T2=（CPI1*f2）/（CPI2*f1）=（2*1.2）/（1.5*1）=1.6。
### 1.3
	存储程序和程序控制是冯·诺依曼结构计算机的主要设计思想，按照冯·诺依曼的设计思想，计算机的硬件系统包含运算器、控
	制器、存储器、输入设备和输出设备五大部件。
### 1.4
	可将计算机系统的层次结构分成6个抽象层次：
	第6层是高级语言层，是面向用户的抽象层次。
	第5层是汇编语言层，该层为用户提供基于助记符表示的汇编语言编程。
	第4层是操纵系统层，该层用于对计算机系统的硬件和软件资源进行统一管理和调度，提高计算机系统的使用效率，方便用户使用计算机。
	第3层是指令集架构层，该层可通过机器语言编写程序实现对计算机硬件的控制，是计算机中软件系统和硬件系统的、之间的界面和纽带。
	第2层是微代码层，该层是实际的机器层，该层的用户使用微指令编写微程序，用户所编写的微程序由硬件直接执行，注意只有采用微程
	序设计的计算机系统才有这一层。
	第1层是逻辑门层，该层是计算机系统最底层的硬件系统，由逻辑门、触发器等逻辑电路组成，它是由逻辑设计者采用布尔代数设计的硬
	件内核。
### 1.5
	CPI1=2*0.4+3*0.2+4*0.15+5*0.25=3.25，MIPS1=f1/CPI1=600/3.25=185；
	CPI2=2*0.4+2*0.2+3*0.15+4*0.25=2.65，MIPS2=f2/CPI2=800/2.65=302。
### 1.6
	（1）优化前CPI=1*0.4+2*0.2+2*0.15+2*0.25=1.6，优化后CPI=(1*0.2+2*0.2+2*0.15+2*0.25)/0.8=1.75.
	（2）优化前MIPS=f/CPI=312.5，优化后MIPS=f/CPI=285.7。
	（3）优化后CPI增加，MIPS减少，优化失败，应尝试降低最大指令的比例。
