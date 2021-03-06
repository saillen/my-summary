# 计算机基础

## 一、计算机组成和硬件

1. 计算机组成原理的意义
2. 冯诺依曼结构 VS 哈佛结构
3. CPU 运行原理
   1. CPU 内部结构及运行原理
   2. CPU 时钟及 OS 的时间计算方式
   3. 超线程 和 程序线程的不同
   4. CPU 原子操作和锁存
   5. 案例：一个简单的程序的 CPU 执行过程

4. 内存特性及原理
   1. 内存工作原理：易失性内存 VS 非易失性内存
   2. DDR4 及内存主频的意义和作用
   3. MMU 技术及  OS 的内存管理
   4. 物理地址、逻辑地址、虚拟地址
   5. voliate 与 CPU、内存的关系
5. 磁盘特性及原理
   1. 磁盘存储原理
   2. SSD VS HDD 
   3. OS 的一次 I/O 处理在计算机硬件层面的过程

6. 总线与其他外设：网卡、键盘
   1. 总线的作用及总线带宽
   2. 主板南北桥的意义
   3. 网卡工作原理
   4. 中断处理机制及设备驱动
   5. 案例：一次网络包的处理过程
7. 硬件限制对计算机编程的影响
   1. 为什么选择二进制
   2. 为什么一个字节是 8 位
   3. 二进制的四则运算
   4. IEEE 754 及浮点数的存储与表示
   5. 为什么一般循环从 0 开始
8. 32 位 和 64 位对计算机编程的影响
   1. 什么是 32 位和 64 位；
   2. 64 位 CPU 中 int 还是 32 位吗？
   3. ADM、Intel、X86、X64 如何根据查看 CPU 参数及制造商
9. 显卡及图形、字符的显示
   1. 显卡的作用
   2. 什么是独显什么是集显
   3. 图形显示原理
   4. 字体原理
   5. 一个汉字 “Hello” 的显示过程
   6. 字符集、字符编码、显示乱码的分析
10. 未来计算机硬件的发展及计算机硬件市场格局
    1. CPU 设计及制造商
    2. 显卡设计及制造商
    3. 主板设计及制造商
    4. 内存设计及制造商
    5. 量子计算机及量子制霸时代

## 二、计算机操作系统 -- Linux 系统

1. 计算机操作系统的种类
   1. 计算机操作系统作用
   2. 计算机操作系统的种类
   3. Linux 系统的种类及如何查看操作系统版本
2. Linux 下面的各种概念
   1. 一切皆文件
   2. 什么是 tty
   3. 如何安装程序
3. Linux 的系统文件
   1. 各目录下的文件及文件作用
   2. 软连接
   3. 系统相关命令
4. Linux 的进程管理
   1. 什么是进程描述符
   2. 进程和线程的不同
   3. Linux 的进程调度算法
   4. 什么是 CPU 虚拟
5. Linux 的内存管理机制
   1. MMU 的作用
   2. 虚拟内存技术
   3. SWAP 分区
6. Linux 的中断处理机制、设备驱动和定时器
   1. 上半部和下半部
   2. 驱动原理：网卡驱动过程
   3. DMA 技术对驱动的优化
   4. OS 是如何计时的：墙上时钟和系统时间
   5. 网络计时协议
7. Linux 下的常用命令汇总
   1. 系统管理相关：查看系统状态及版本
   2. 文件及权限相关
   3. 日志查询及分类
   4. 远程登录、上传、下载 类
   5. 性能分析类
   6. 标准 API



## 三、计算机网络

1. OSI 七层和 TCP 五层模型
   1. 分层的意义
   2. OSI 七层和 TCP 五层的对比
   3. Linux 下的各层协议
2. 下三层回顾
   1. 链路层：802.X 协议
   2. 网卡的工作原理
   3. 传输层和网络层：ARP协议和IP协议
   4. IP 地址及 IP 掩码
   5. IPv4 VS IPv6
   6. 网络层的数据帧及 MTU
3. 上二层回顾
   1. TCP、UDP协议
   2. TCP 三次握手及四次挥手过程
   3. ICMP VS ICMPv6 协议
   4. SSL 层的作用及实现原理
4. 网络相关命令汇总
   1. 相关命令汇总
   2. 网络分析工具：TcpDump、Wareshare
   3. 代理抓包过程
5. 应用层协议
   1. Http、Https
   2. WebSocket
   3. Socket 编程