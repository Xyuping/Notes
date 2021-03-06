# 操作系统(MOOC,南京大学 骆斌)

## 一.计算机操作系统概述

### 1.1计算机系统概览

### 1.2计算机硬件系统

### 1.3计算机软件系统

### 1.4计算机操作技术的发展

### 1.5计算机操作系统

### 1.6:资源管理的角度

### 1.7:程序控制的角度

#### 目标

- 掌握多道程序设计的概念
- 理解多道程序同时计算
- 掌握多道程序设计的优点
- 理解多道程序设计的实现

#### 多道程序设计概念

多道程序:指让多个程序同时进入计算机的主存储器进行计算

多道程序可以解决机械速度和电子速度不匹配的问题,提高CPU利用率

#### 多到程序同时计算

- CPU速度与I/O速度不匹配的矛盾非常突出
- 只有让多道程序同时进入内存争抢CPU运行,才可以使得CPU和外设充分并行,从而提高计算机系统给的使用效率
- ![img_0552](/Users/xyp/Desktop/MySQL/img/img_0552.png)

#### 多道程序设计优点:

- CPU与外设充分并行
- 外设之间充分并行
- 发挥CPU的使用效率
- 提高单位时间的算题量

#### 多道程序体统的实现

- 为进入内存执行的程序建立管理实体:进程
- OS应该能管理与控制进程程序的执行
- OS协调管理各类资源在进程间的使用
	- 处理器的管理和调度
	- 主存储器的管理和调度
	- 其他资源的管理和调度

#### 多道程序实现要点

![img_0553](/Users/xyp/Desktop/MySQL/img/img_0553.png)

### 1.8操作系统控制计算机的角度

#### 目标

- 掌握计算机操作控制方式
- 理解脱机作业控制方式
- 理解联机作业控制方式
- 掌握命令解释程序及其处理过程

#### 计算机系统操作方式

- OS规定了合理操作计算机的工作流程
- OS的操作接口:系统程序
	- OS提供给用户的功能级接口,为用户提供的解决操作计算机和计算共性问题的所有服务的集合
- OS的两类作业级接口
	1. 脱机作业控制方式:作业控制语言
	2. 联机作业控制方式:操作控制命名

#### 脱机作业控制方式(今天比较少见)

- OS:提供作业说明语言
- 用户:编写作业说明书,确定作业加工控制步骤,并与程序数据一并提交
- 操作员:通过控制台输入作业
- OS:通过作业控制程序自动控制作业的执行
- 例如:批处理OS的作业控制方式,UNIX的shell程序,DOS的bat文件

#### 联机作业控制方式(现在的主要方式)

- 计算机:提供终端(键盘/显示器)
- 用户:登录系统
- OS:提供命令解释程序
	- 命令解释程序:接收和执行一条用户提出的对作业的加工处理命令的一个程序包.
		- 当一个新的批作业被启动,或新的交互型用户登录进系统时,系统就自动执行命令解释程序,负责读入控制卡或命令行,做出相应解释,并予以执行.
		- 处理过程
			1. OS启动命令解释程序,输出命令提示符,等待 键盘中断/鼠标点击/多通道识别/编程命令中断符...
			2. 每当用户输入一条命令(暂存在命令缓冲区)并按回车换行时,申请中断 [即读出在缓冲区中的用户要求计算机要执行的命令]
			3. CUP响应,然后将控制权交给命令解释程序,接着读入命令缓冲区内容,分析命令,接受参数,执行处理代码
				- 前台命令:严格按序执行.一个作业步一个作业步顺序执行.(前台命令执行结束后,再次输出命令提示符,等待下一条命令)
				- 后台命令:后台命令处理启动后,即可接受下条命令(不管该命令是否执行结束)
	- 会话语言:可编程的命令解释程序.(例如 UNIX的shell)
	- 图形化的命令控制方式
	- 多通道交互的命令控制方式
- 用户:联机输入命令,直接控制作业步的执行
- 例如:分时OS的交互控制方式

### 1.9人机交互角度

#### 目标

- 理解操作系统的人机交互部分
- 了解操作系统人机交互技术的发展
- 理解操作系统的WIMP界面
- 了解多媒体计算机的人机交互
- 了解虚拟现实系统的人机交互

#### 操作系统的人机交互部分

- OS改善人机界面,为用户提供良好的使用环境
- 人机交互设备宝库传统的终端设备和新型的模式识别设备
- OS的人机交互部分用于控制有关设备运行和理解执行设备传来的命令
- 人机交互功能是决定计算机系统友善性的重要因素,是当今OS研发热点

#### 发展

- ##### 初期

	- 交互式控制方式
		- 行命令控制方式
		- 全屏幕控制方式
		- 斯坦福研究所提出:强调以人为中心的人机交互而不是以技术(效率)为中心.代表性成果:鼠标,菜单与窗口控制

- ##### WIMP界面

	- 特征:窗口(W),图标(Icons),菜单(Menu),指示装置(Pointing Devices)
	- 得益:Apple最初采用并大力推动
	- 目前,ios是wimp界面的最高境界
	- 不足:不允许同时使用多个交互通道,从而产生人机交互的不平衡

- ##### 多媒体计算机

	- 缘起:MPC
	- 把音频视频,图形图像和人际交互控制结合起来,进行综合处理的计算机系统
	- 构成:多媒体硬件平台,多媒体OS,图形用户接口,多媒体数据开发工具
	- 提供与时间有关的时变媒体界面,既控制信息呈现,也控制何时呈现/如何呈现

- ##### 虚拟现实系统(临镜系统)

	- VR:通过计算机,模拟三维虚拟世界,根据 观察点,观察点改变的导航和对周围对象的操作 来模拟(身临其境)的感觉
	- 支持多通道交互
	- 支持用户主动参与的高度自然的三维HCI(Human-Computer Interaction 人机交互),以及语音识别,头部跟踪,视觉跟踪,姿势识别等新型HCI
	- 容许用户产生模糊和不精确的处理



### 1.10程序员接口的角度

#### 目标

- 操作系统的程序接口
- 操作系统调用的实现机制
- 系统调用的实现要点
- 系统调用的实现流程

#### 操作系统的程序接口

- 操作系统主要的程序接口:系统调用
- 系统调用:操作系统实现的完成某种特定功能的过程,为所有运行程序提供访问操作系统的接口

#### 系统调用的实现机制

- 陷入处理机制:计算机系统中控制和实现系统调用的机制(用户程序如何陷入计算机操作系统,请求操作系统为其服务)
- 陷入指令(访管指令/异常中断指令):计算机系统为实现系统调用二引起处理器中断的指令
- 计算机系统中有大量的系统调用,每个系统调用事先规定编号,并在约定个寄存器中规定了传递给操作系统的内部处理程序的参数(这些编号传递给操作系统,以供操作系统的内部吹程序来调用相应的系统调用服务)

#### 系统调用的实现要点

- 编写系统调用处理程序(主框架)
- 设计一张系统调用入口地址表,每个入口地址指向一个系统调用的处理程序,并包含系统调用自带参数的个数(主框架来查入口地址表)
- 陷入处理机制要开辟现场保护区,以保存发生系统调用时的处理器现场

#### 系统调用实现流程

- 由计算机系统的硬件(陷入)和操作系统(查入口地址,处理)共同完成

![img_0677](https://ws4.sinaimg.cn/large/006tKfTcly1g1887nxr2lj31bf0szq8m.jpg)

### 1.11系统结构的角度

#### 目标

- 理解操作系统软件的规模
- 理解操作系统的构件与设计原则
- 了解操作系统内核
- 理解操作系统实现的层次式结构模型

#### 操作系统软件的规模

- 在计算机软件发展史上,OS是第一个大规模的软件系统
- 直接催生了软件工程(另一个催生来源是数据库)
- OS结构设计是关键

#### 操作系统软件的结构设计

- OS构件
	- 内核,进程,线程,管程等
- 设计概念
	- 模块化,层次式,(资源)虚拟化
- 内核设计是OS设计中最为复杂和关键的部分
	- (操作系统必须提供内核,只有在这个内核的支持下,计算机上运行的各种应用和软件才能被抽象成进程,线程,管程这些实体)
	- 单内核:内核中各部件杂然混居的形态,广泛使用.如Unix,Linux,Windows(自称采用混合内核的C/S[客户/服务器]结构)
	- 微内核:强调结构性部件与功能性部件的分离,大部分OS研究都集中在此.(把内核中的功能性部件做小,把内核中的功能性部件变成进程,在内核外运行).这种结构主要在学术界中研究
	- 混合内核:单内核和微内核的折中,较多组件在核心态中运行.(把单内核变小,一部分移到外面的进程去做,Windows试图去做)
	- 外内核:尽可能减少内核的软件抽象化和传统微内核的消息传递机制,使得开发者专注于硬件的抽象化;部分嵌入式系统使用
- 操作系统实现的层次结构
	- ![img_0678](https://ws2.sinaimg.cn/large/006tKfTcly1g1887l7n55j31da0u078w.jpg)
		- (理想化的模式,今天用的不多)
	- ![fullsizerender(https://ws2.sinaimg.cn/large/006tKfTcly1g1887lql1ej31de0tm0z8.jpg)](/Users/xyp/Desktop/学习/02_笔记/操作系统笔记/img/fullsizerender(2).jpg)





## 二.处理器管理

### 2.1处理器与寄存器

#### 目标

- 理解处理器及其部件
- 理解用户程序可见寄存器
- 理解控制与状态寄存器
- 掌握程序状态字概念

#### 处理器部件



- 寄存器
	- 用户程序可见寄存器
		- 可以是程序员减少访问主存次数,提高指令执行效率
		-  所有程序可使用,包括应用程序和系统程序
			- 数据寄存器(通用寄存器)
			- 地址寄存器:
				- 索引寄存器:SI,DI
				- 栈指针寄存器:SP,BP
				- 段地址急促承诺期:CS,DS,SS,ES
	- 操作系统使用的:控制与状态寄存器
		- 用于控制处理器的操作,主要被具有特权的操作系统程序使用,以控制程序的执行
		- 程序计数器PC
		- 指令寄存器IR
		- 条件码CC:CPU为指令操作结果设置的位,标志正/负/零/溢出等结果
			- 标志位:中断位,中断允许位,中断屏蔽位,处理器模式位,内存保护位...
- 程序状态字PSW
	- PSW既是操作系统的概念,指记录当前程序运行的动态信息(是操作系统在控制程序执行行为,控制资源访问行为中非常重要的概念,指状态寄存器中存储的一些内容)
		- 通常包含:程序计数器,指令寄存器,条件码;中断字,中断允许/禁止,中断屏蔽,处理器模式,内存保护,调试控制
	- PSW也是计算机系统给的寄存器
		- 通常设置一组控制与状态寄存器



### 2.2指令与处理器模式

#### 目标

- 机器指令及其执行过程
- 指令流水线
- 特权指令与非特权指令
- 处理器模式及其切换

#### 机器指令

- 计算机系统执行的基本命令,中央处理器执行的基本单位
- 指令执行过程
- 指令执行周期:取址,解码,执行

#### 特权指令与非特权指令

- 用户程序并非能够使用全部机器指令,那些与计算机核心资源相关的特殊指令会被保护,如 启动I/O指令,置PC指令(置程序状态字)等
- 核心资源相关的指令只能被操作系统程序使用
- 特权指令:只能被操作系统内核使用的指令
- 非特权指令:能被所有程序使用的指令

#### 处理器模式

- 处理器模式位

	- 计算机通过设置处理器模式位实现特权指令管理(特权的处理器模式位和非特权的处理器模式位)
	- 计算机一般设置四种运行模式,0  1  2 3 ,分别对应:
		- 0:操作系统内核
			- 可以执行全部指令
		- 1:系统调用
			- 可以规定执行的指令子集
		- 2:共享库程序
			- 可以规定执行的指令子集
		- 3:用户程序等保护级别
			- 只能执行非特权指令
	- 一般来说,现代操作系统值使用0和3模式,对应于内核模式和用户模式

	#### 模式的切换

	- 用户模式->内核模式
		- 中断,异常或系统异常等时间导致用户程序向OS内核切换,触发用户模式->内核模式
			- 程序运行时发生并响应中断
			- 程序运行时发生异常
			- 程序请求操作系统服务
	- 内核模式->用户模式
		- OS内核处理完成后,调用中断返回指令(如Internet)触发:内核模式->用户模式



### 2.3中断

#### 目标

- 掌握中断的基本概念
- 理解中断,异常与系统异常

#### 中断的基本概念

- 中断是指:程序执行过程中,遇到继续处理的事件时,暂时终止CPU上现行程序的运行,转去执行响应的事件处理程序,再返回源程序被中断处或调度其他程序执行的过程

- 操作系统是"中断驱动"的(只有通过中断,用户系统在运行的时候才能切换到操作系统程序,操作系统再挑选另一个用户程序运行,来实现用户程序的切换).

	- > 中断是激活操作系统的唯一方式

		操作系统要求计算机硬件系统为其设置相应的中断激活的硬件机制,再配合操作系统的内核程序,共同完成中断驱动的方式,并且中断驱动方式是操作系统程序实现的最根本的基础

#### 中断,异常与系统异常

- 中断
  - 有广义和狭义之分,上述中断指的是广义的中断
  - 中断最初是形成于CPU与外围设备协同工作上,所以最初的中断是来源于处理器之外的外围设备
  - 狭义的中断指的是 ==来源于处理器之外的外围设备,即与当前运行指令无关的中断事件== ,如I/O中断,时钟中断,外部信号中断(键盘,鼠标)等
- 异常

  指当前<u>运行指令</u>引起的中断事件,如地址异常,算数异常(如溢出),处理器硬件故障(比如停电)

  异常和狭义的中断构成广义的中断
- 系统异常
  - 系统异常指因<u>执行陷入指令</u>(用户程序被中断,陷入系统内核) 而<u>触发系统调用</u> 引起的中断事件,如请求设备,请求I/O,创建进程等
  - 与硬件无关
  - 是异常中的一种



### 2.4中断源

#### 目标

- 掌握中断源
- 掌握中断源的处理原则

#### 中断事件的分类

1. 中断源-处理器硬件故障中断事件
	- 由处理器,内存储器,总线等硬件故障引起
	- 除极少数外,大部分是非常严重的中断事件
	- 处理原则:保护现场,停止设备,停止CPU,向操作员报告,等待人工干预
2. 中断源-程序性中断事件
	- 处理器执行机器指令引起
		- 除数为零,操作数溢出等算数异常.通常简单处理,报告用户,也可以由用户编写中断续元程序处理
		- 非法指令,用户态使用特权指令,地址越界,非法存取等指令异常:终止程序
		- 终止程序指令:终止程序
		- 虚拟地址异常(指令不在内存在外存):调整内存后重新执行指令
3. 中断源-自愿性中断事件(系统异常)
	- 处理器执行陷入指令,请求OS服务引起的. 在操作系统中,他一般又被称作系统调用
		- 请求分配外设,请求I/O等
		- 处理流程:陷入OS,保护现场,根据功能号查入口地址,跳转具体处理程序
4. 中断源-I/O中断事件(狭义中断事件)
	- 来源于外围设备报告I/O状态的中断事件
		- I/O完成:调整进程状态,释放等待进程
		- I/O出错:等待人工干预
		- I/O异常:等待人工干预
5. 中断源-外部中断事件
	- 由外围设备发出的信号引起的中断事件
		- 时钟中断,间隔时钟中断(时间片):记时与时间片处理
		- 报备报道与结束中断:调整设备表(操作系统资源管理表)(例如连接在计算机的打印机,开机)
		- 键盘/鼠标信号中断:根据信号做出相应反应
		- 关机/重启中断:写回文件,停止设备与CPU

### 2.5中断系统(1)

软硬件协同

#### 目标

- 了解中断系统
- 了解终端管理与指令执行周期
- 掌握中断响应与中断装置

#### 中断系统

中断系统是计算机系统中响应和处理中断的系统,包括硬件子系统和软件子系统

- 中断响应由硬件子系统完成
- 中断处理由软件子系统完成

![](https://ws1.sinaimg.cn/large/006tKfTcly1g1887ia15aj318l0u0tfv.jpg)

#### 中断装置

- 计算机系统中发现并响应中断/异常的==硬件==装置称为中断装置
- 由于中断源的多样性,硬件实现的中断装置有多种,分别处理不同类型的中断
	- 处理器外的中断:由中断控制器发现和响应
	- 处理器内的异常:由之路的控制逻辑和实现线路发现和响应,响应机制称为陷阱
	- 请求OS服务的系统异常:处理器执行陷入指令时直接触发,相应机制称为系统陷阱

##### 中断控制器

是CPU中的一个控制部件,包括中断控制逻辑线路和中断寄存器

- 外部设备向其发出中断请求IRQ,在中断寄存器中设置已发生的中断(异步过程)
- 指令处理结束前,会检查中断寄存器,若有不被屏蔽的中断产生,则改变处理器内操作的顺序,引出操作系统的中断处理程序(同步过程)

##### 陷阱与系统陷阱(同步过程)

- 指令的逻辑实现线路的一部分
	- 执行指令出现异常后,(线路向操作系统报告),会根据异常情况转向<u>操作系统的异常处理程序</u>
	- 出现虚拟地址异常后,(指令没有执行完),需要重新执行指令,往往<u>越过陷阱</u>独立设置<u>页面异常处理程序</u>
	- 执行陷入指令后,越过陷阱处理,触发<u>系统陷阱</u>,激活<u>系统调用处理程序</u>

#### 中断响应过程

1. 发现中断源,提出中断请求
	1. 发现中断寄存器中记录的中断
	2. 决定这些中断是否被屏蔽
	3. 当有多个要响应的中断源时,根据规定的优先级选择一个
2. 中断当前程序的执行
	- 保存当前程序的PSW/PC到核心栈
3. 转向操作系统的中断处理程序/异常处理程序



### 2.6中断系统(2)

#### 目标

- 掌握中断处理与中断处理程序
- 掌握中断响应与中断处理的整体流程

#### 中断的处理(软件)

- 中断处理程序
	- 操作系统处理中断事件的控制程序,主要任务是处理中断事件和恢复正常操作

> 1. 保护未被硬件保护的处理器状态(硬件保存了PSW/PC)
> 2. 通过分析被中断进程的PSW中断码字段,<u>识别中断源</u>
> 3. 分别处理发生的中断事件
> 4. 恢复正常操作
> 	1. 某些中断:在处理完毕后,直接返回刚刚被中断的过程
> 	2. 其他中断:要中断当前进程的运行,调整进程队列,启动进程调度,选择下一个执行的而进程并回复其执行(即回复别人,自己恢复到另一个用户进程)
> 	3. 都是从内核切换到用户进程

 ![icon](https://ws2.sinaimg.cn/large/006tKfTcly1g1887km9hoj314k0u0gq3.jpg)



### 2.7多中断的响应与处理

#### 目标

- 掌握中断屏蔽
- 掌握中断优先级
- 掌握中断的嵌套处理
- 掌握多中断的响应与处理

#### 中断屏蔽

- 当计算机检测到中断时,中断装置通过中断屏蔽位决定是否响应已发生的中断
- 可以有选择的响应中断

#### 中断优先级

- 当计算机同时检测到多个中断时,中断装置响应中断的顺序不同
- 有优先度的响应中断
- 一种可能的处理次序:
	- 处理机硬件故障中断事件,自愿性中断事件,程序中断事件,时钟等外部中断事件,输入输出中断事件,重启和关机中断事件
- 不同操作系统有不同的中断优先级

#### 中断的嵌套处理

- 当计算机响应中断后,中断处理过程中可以在响应其他中断
- 操作系统是性能攸关的程序,且中断响应和处理有硬件要求,考虑系统效率和实现代价问题,中断嵌套处理应该限制在一定层数,如3层
- 中断的嵌套处理改变中断处理次序,先响应的有可能后处理

### 多中断的响应与处理

- 中断屏蔽可以使中断装置不响应某些中断
- 中断优先级决定了中断装置响应中断的次序
- 中断可以嵌套处理,先响应的可以后处理,改变了中断处理的次序



### 2.8进程及其状态

#### 目标

- 掌握进程的基本概念
- 掌握进程的三状态模型
- 理解进程挂起的概念

#### 进程的提出

操作系统必须全方位地管理计算机系统中运行的程序.为此,操作系统为正在运行的程序建立一个管理实体--进程

#### 进程的概念

- 进程是一个具有一定独立功能的程序关于某个数据集合的一次运行活动

- 进程是操作系统进行资源分配和调度的一个独立单位

- 一个进程包括五个实体部分:

	1. P:(OS管理运行程序的)数据结构
	2. C:(运行程序的)内存代码
	3. D:(运行程序的)内存数据
	4. R:(运行程序的)通用寄存器信息
	5. PSW:(OS控制程序执行的)程序状态字信息

- 进程举例

	1. 不同程序代码在不同数据集上运行,构成无关进程
	2. 不同程序代码在相同数据集上运行,构成共享数据的交往进程
	3. 相同程序代码在不同数据集上运行,构成共享代码的无关进程
		- 把共享的代码称为 <u>可再入程序</u>,如编辑器,编译器
		- 可再入程序是纯代码的

	> 注意前述的程序与数据集均是内存级别的
	>
	> 在不同时段中,针对(同一个外存数据文件)运行(同一个外存程序文件),意味着完全不同的(P,C,D,R,PSW)
	>
	> 所以两次运行构成两个不同的进程

#### 概念级的进程状态

1. 运行态:只进程占有处理器运行
2. 就绪态:指进程具备运行条件等待处理器运行
3. 等待态:值进程由于等待资源/输入输出/信号等不具备运行条件

三种状态的相互转换(指的是同一个进程)

![icon](https://ws4.sinaimg.cn/large/006tKfTcly1g1887hy4rej31kw0twagr.jpg)



### 进程挂起

- 由于OS无法预期进程的数目与资源需求,计算机系统在运行过程中可能出现资源不足的情况
- 运行资源不足表现为系统的 <u>*性能低*</u>和 <u>*死锁*</u> 两种情况
- 解决办法:剥夺某些进程的内存及其他资源,把他们调入OS管理的对换区,让其不参加进程调度,待适当时候再调入内存,恢复资源,让其再参与运行(进程调度).
- 这就是 *进程挂起*
- 挂起态与等待态有着本质区别,等待态占有已申请到的资源处于等待,而挂起状态进程没有任何资源

![icon](https://ws2.sinaimg.cn/large/006tKfTcly1g1887mr0gdj31hs0tw11s.jpg)



### 2.9进程的数据描述

#### 目标

- 掌握进程控制块的概念
- 了解进程控制块的内容
- 理解进程的内存映像
- 理解进程上下文的概念

#### 进程控制块(Process Control Block)

![cion](https://ws2.sinaimg.cn/large/006tKfTcly1g1887irfqjj31ak0u0qb3.jpg)

- 标识信息
	- 用于存放唯一标识该进程的信息
		- 系统分配的标识号
		- 系统分配的进程组标识号
		- 用户定义的进程名
		- 用户定义的进程组名
- 现场信息
	-  用于存放该进程运行时的处理器现场信息
		- 用户可见寄存器内容:数据寄存器,地址寄存器等
		- 控制与状态寄存器内容:PC,IR,PSW等
		- 栈指针内容:核心栈与用户栈指针
- 控制信息
	- 用于存放与管理,调度进程相关的信息
		- 调度相关信息:状态,等待事件/原因,优先级
		- 进程组成信息:代码/数据地址,外存映像地址
		- 队列指引元:进程队列指针,父子兄弟进程指针
		- 通信相关信息:消息队列,信号量,锁
		- 进程特权信息:如内存访问权限,处理器特权
		- 处理器使用信息:占用的处理器,时间片,处理器使用时间/已执行总时间,记账信息
		- 资源清单信息:如正占有的资源,已使用的资源

#### 进程映像(process image)

某一时刻进程的内容及其执行状态集合,包括:

- 进程控制块:用于保存进程的标识信息,状态信息和控制信息
- 进程程序块:进程执行的程序空间
- 进程数据块:进程处理的数据空间,包括数据,处理函数的用户栈和可修改的程序
- 核心栈:进程在内核模式下运行时使用的堆栈,中断或系统过程使用

进程映像是内存级的物理实体,又被称为进程的内存映像

### ![icon](https://ws2.sinaimg.cn/large/006tKfTcly1g1887jdgkcj31a60u046a.jpg)

#### 进程上下文(process context)

- 进程的执行需要环境的支持,包括CPU现场和Cache中的执行信息
- OS中的进程的物理实体和支持进程运行的环境合成进程上下文,包括:
	1. 用户级上下文
		- 用户程序块/用户数据区/用户栈/用户共享内存
	2. 寄存器上下文
		- PSW/栈指针/通用寄存器
	3. 系统级上下文
		- PCB/内存区表/核心栈
- 进程上下文刻画了进程的执行情况



### 2.10进程的管理

#### 目标

- 了解进程管理程序的概念级组成
- 掌握进程队列模型和队列管理模块
- 理解进程的控制与管理程序的实现

#### 概念级的OS进程管理软件

- 概念级的OS进程管理软件包括:
	- 系统调用/中断/异常处理程序(中断管理中介绍的)
	- 队列管理模块(OS管理进程控制块的程序,是一个核心程序包)
	- 进程控制程序(OS用于控制进程状态转换所用到的程序包)
	- 进程调度程序(独立进程居多)
	- 进程通信程序(多个程序包)
	- 一些外围程序,比如:终端登录与作业控制程序,性能监控程序,审计程序

#### 进程实现的队列模型

![icon](https://ws2.sinaimg.cn/large/006tKfTcly1g1887njhw8j31gf0u07ab.jpg)

#### 队列管理模块

- 队列管理模块是操作系统实现进程管理的核心模块
- 操作系统建立多个进程队列,包括就绪队列和等待队列
- 按需组织为先进先出队列或优先队列
- 队列中的进程可以通过PCB(进程控制模块)中的队列指引元,采用单/双指引元或索引连接
- 队列管理模块围绕各个进程队列执行出队和入队操作
- 进程关于资源调度围绕进程队列展开

#### 操作系统中的进程控制与管理

常用的进程控制过程包括:进程的创建,进程的撤销,进程的阻塞,进程的唤醒,进程的挂起,进程的激活. 都涉及到进程状态的转换

- 进程创建:进程表加一项,申请PCB并初始化,生成标识,建立映像,分配资源,移入就绪队列
- 进程撤销:从队列中移除,归还资源,撤销标识,回收PCB,移除进程表项(与创建逆过程)
- 进程阻塞:保存现场信息,修改PCB,移入等待队列,调度其他进程执行
- 进程唤醒:等待队列中移出,修改PCB,移入就绪队列(唤醒进程的优先级如果高于此时正在运行的进程,触发抢占)
- 进程挂起:修改状态,出入相关队列,收回内存等资源送至对换区
- 进程激活:分配内存,修改状态并出入相关队列
- 其他:如修改进程特权

#### 原语与进程控制原语

进程控制是进程管理的重要内容

进程控制过程中涉及对OS核心数据结构(如进程表/PCB池/队列/资源表)的修改,这些都是重要的共享资源,不恰当的调整会产生与时间有关的错误

为防止与时间有关的错误,应使用原语实现进程控制的核心操作(注意不是进程控制的整个流程)

- *原语* 是由若干条指令构成的完成某种特定功能的程序,执行上具有不可分割性(操作系统要保证其在执行过程中不可以被中断,不可以被分割).原语是短小精悍的程序段.
	- 进原语前把中断关掉,出原语后把终端开放
- 进程控制使用的原语称为进程控制原语
- 另一类常用的原语是*进程通信原语*

### 2.11进程切换与模式切换

