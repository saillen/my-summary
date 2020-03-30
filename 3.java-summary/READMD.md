# Java 编程

## 一、Java语言基础

1. Java 语法回顾
   1. 各类关键字及原理作用
   2. Java 中基本数据类型及内存占用
2.[Java 中的数据结构](./launage/2-0-Java中的数据结构.md)
   1. [Util 包下的 Collection 等](./launage/2-1-类结构.md)
   2. [Map、List、Set 的实现及源码](./launage/2-2-Collection源码.md)
   3. [Concurrent 包源码](./launage/2-3-Concurrent包源码.md)
3. Java 中异常处理
   1. 异常分类及产生
   2. 异常处理过程
   3. 建议的编码规约
4. Java 多线程及实现
   1. 多线程的意义及如何启动线程
   2. 线程状态的流转及相关 API
   3. 线程池的管理
5. Java 网络编程及 IO 操作
   1. 网络编程 API 及 IO API
   2. 字符流、字节流及装饰器模式
   3. Java 中文件 I/O 过程
   4. BIO、AIO、NIO 及内核的支持
   5. Java 在 Linux 系统中一次 Socket 过程
6. Java Web 编程 -- Java 对 Http 协议的支持
   1. Servelt API 及生命周期
   2. Web 容器及原理
   3. Filter 及责任链模式
7. Java 反射及动态代理
   1. Java 反射及动态代理思想
   2. 反射 API
   3. 动态代理 API
   4. WeekReference 及 unsafe 类
8. Java 加解密技术
   1. 信息摘要技术及算法
   2. 对称机密技术技术及算法
   3. 非对称加密技术及算法
   4. 证书及 PKCS
   5. Java 中证书相关的命令
9. JDBC 及数据库操作
   1. JDBC 的原理及 API
   2. ODBC 及 ORM 思想
   3. JDBC Template 思想及模板方法
10. Java 序列化、XML、JSON 等数据交换格式
    1. Java 本身的序列化
    2. Java 对 XML 的支持
    3. Java 对 JSON 的支持
11. JDK 8 及以后版本的新语法新特性
    1. 流处理思想及流 API
    2. Lambad 表达式

## 二、Java 单机框架

1. Spring 核心框架
   1. Spring 包依赖关系及各包作用
   2. Spring 的 IoC 及 DI 思想
   3. Spring Context 的组件结构
   4. BeanFactory 的初始化过程
   5. Spring AOP 原理：aspectj VS cglib 及 Java 动态代理
   6. Spring 核心包用到的设计模式
2. Spring MVC 框架
   1. 前段控制器思想
   2. MVC 组件结构
   3. Spring MVC 初始化过程
   4. Spring MVC 框架请求处理过程
   5. MVC 框架的各种注解和扩展点
   6. 用到的设计模式
   7. 一些实践建议
3. Spring Dao 包
   1. JDBC Template 思想
   2. 类结构及异常转换方式
   3. Spring 事务级别及事务传播机制
4. MyBaits 框架
   1. iBaits、MyBaits 及 ORM 框架
   2. 组件结构及源码
   3. 如何与 Spring 结合
   4. ORM 过程
   5. 各注解及扩展点
5. 定时任务实现及框架
   1. 如何实现单机定时任务及各框架优缺点
   2. Timer 和 TimerTask 
   3. ExecutorService 方式实现定时任务
   4. Quaz 单机定时任务框架原理
   5. 集群（分布式）环境下定时任务框架：ElasticJob
   6. ElasticJob 的组件结构及原理
6. Web 容器
   1. Tomcat 的组件结构
   2. Tomcat 的请求处理过程
   3. Tomcat 各项配置及端口意义

## 三、Java 网络通信

1. RPC 通信及思想
   1. RPC 思想及 RMI 实现
   2. 网络通信待解决的问题
   3. 同步 VS 异步通信
   4. 分布式框架：Dubbo VS Spring Cloud
2. Java 中对 Http 协议的支持及框架
   1. 内置 Http 通信框架
   2. HttpClient 开源框架组件结构
   3. HttpTemplate 思想及建议
3. Netty 网络通信框架
   1. Netty 思想及产生背景
   2. Netty 的组件结构
   3. Netty Worker 的多路复用技术；
4. Dubbo 框架及原理
   1. Dubbo 框架思想及原理
   2. Dubbo 组件结构及源码分析
   3. Dubbo 中各注解及扩展点
   4. Dubbo 中支持的各项协议及实现
5. Zookeeper 分布式协调框架
   1. Zookeeper 的作用及意义
   2. Paxos 及 Zookeeper 的选主算法
   3. Zookeeper 的组件结构及源码
6. ElastcJob 分布式定时任务框架详解
   1. ElasticJob 在分布式环境下的作用及思想
   2. ElasticJob 的失效任务转移及选主过程
7. RocketMQ 源码
   1. MQ 的作用及意义
   2. RocketMQ 的组件结结构及源码

## 四、Java 虚拟机技术

1. JVM 的发展和 JVM 规范
   1. Java 虚拟机规范及发展历史
   2. JVM 规范中：JVM 的逻辑结构
   3. JVM 规范中：JVM 的内存管理方式
2. GC 算法
   1. GC 的作用及 GC 停顿
   2. 标记清楚、标记整理
   3. 新生代、老年代及元数据区
   4. 编程对 GC 的影响和建议
3. JVM 的类加载过程
   1. 双亲委派模型
   2. JVM 类加载过程：校验、初始化过程
4. JVM 锁的实现
   1. 监视器思想 和 synchronize 关键字
   2. 锁的膨胀及 JDK 1.8 的优化
   3. 减小锁的粒度的好处和方案
   4. 终极方案：协程思想
5. JVM 问题分析及优化
   1. JVM 问题分析工具
   2. OOM 分析：火焰图
   3. JVM 调优建议