# 数据库及缓存

## 一、缓存原理

1. 单机缓存原理
   1. 缓存的意义及单机缓存的实现
   2. 线程安全的缓存 ThreadLocal
2. 集群下的缓存
   1. 一致性 Hash 算法
   2. Tomcat 的 Session 共享方案
   3. 分布式缓存要面临的问题
3. Redis 
   1. Redis 的作用及原理
   2. Redis 下的各项命令
   3. Redis 的集群部署方案
   4. 半支持 VS 全支持
   5. Redis 做分布式锁的正确实现
   6. Reids 的 Key 过期策略 
4. 其他缓存组件

## 二、关系型数据库

1. 数据库原理
   1. 三层模式两层映射
   2. 一、二、三范式及其优缺点
   3. 基本 SQL 语法：DDL、DML
2. MySql 数据库
   1. MySql 的发展史及各版本特性
   2. MySql 的软件结构
   3. MySql 存储引擎：各引擎特点及适用场景
3. MySql -- InnoDB 引擎
   1. 引擎特点及原理
   2. InnoDB 的索引组织表 -- 索引结构
   3. InnoDB 的文件存储方案
   4. InnoDB 的 BinLog 实现方案
   5. InnoDB 的加锁方案及 MVVC 技术
4. MySql - 事务隔离级别
   1. 四个事务隔离级别及问题
   2. InnoDB 中四个事务隔离级别是如何实现的及加锁类型
   3. 乐观锁 VS 悲观锁
   4. 特殊的读语句：for update 、 lock for share model
5. SQL 优化
   1. SQL 优化原则及意义
   2. SQL 优化方案
   3. explain 的用法及案例分享
6. 分库分表及分布式事务
   1. 水平分表 VS 垂直分表
   2. 何时做分表
   3. 什么是分布式事务
   4. 2PC、3PC 及 TCC
   5. 支持分布式事务的中间件及开源组件

## 三、NoSQL 数据库

1. 什么时候 NoSQL 数据库
2. MongoDB 数据库
   1. MongoDB 的思想和结构
   2. MongoDB 的适用场景
   3. MongoDB 的集群部署方案
3. ElasticSearch 全文检索
   1. ElasticSearch 的思想和结构
   2. ElasticSearch 的用法汇总
   3. 倒排索引 VS 全文索引
   4. ElasticSearch 的集群部署方案