# 一小时总结 -- Redis 及缓存

- 原理知识
	- 内存模型：Redis 的数据存储方式
		- Redis 支持的数据结构及内存占用；
		- Redis 的 key 过期策略及内存满处理策略；
		- Redis 的刷盘实现方案；
	- 线程模型及网络模型：Redis 的单线程 IO 多路复用机制；
		- Reactor 模型及 Redis 的实现；
		- Redis 如何支持事务； 
	- 高可用：Redis 的集群部署方式
		- Redis 的主从复制
		- Redis 的哨兵思想；
		- Redis Cluster 方案；
		- 其他变种：Codis 方案；
	- 高性能缓存方案：
		- 选取你的单机：内存、线程、网络模型；
		- 选取你的高可用方案：水平扩展、防止雪崩；
		- 一致性 Hash 算法
		- 布隆过滤器；
- 应用场景
	- Redis 实现分布式锁，setnx 及 RedLock；
	- Redis 实现海量小 key 存储内存节约方案；
	- Redis 的缓存雪崩及防止策略；
	- Redis 缓存穿透的防范机制；
	- Redis 的缓存预热和冷热数据；


	