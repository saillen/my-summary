# 一小时总结 -- 数据结构及 Java 实现

- 原理性知识
	- 数据结构
		- 线性表、链表、队列
		- 树、二叉树、堆、AVL 树、红黑树、B 树、B+ 树；
		- 二叉树的前中后序遍历；
		- 图及图的遍历；
		- 哈希表及哈希冲突；
	- Java 的实现
		- 集合包和并发包的继承结构；
		- 线性表：List、ArrayList、LinkedList；
		- 队列：Queue、Deque、LinkedList、BlockingQueue、BlockedLinkedList、SychronizedQueue、TransforQueue；
		- 栈：Stack、Vector；
		- 树：
		- 哈希表：Map、SortedMap、HashMap、ConcurrentHashMap、TreeMap、LinkedHashMap；
	- Java 的结构的效率问题
		- JDK 1.8 的优化，提升了什么效率；
		- HashMap 的 resize、rehash 发生的时机；
		- 为什么 HashMap 的 table size 为 2 的幂次方；
		- JDK 1.8 前 HashMap 为什么会发生死循环；
		- Conncurrent 包下的效率为什么高？原理是什么？
			- CAS 原理；
			- JDK 1.6 的新锁和锁种类；
- 应用知识
	- 如何实现 LRU 算法；
	- 如何实现一致性 Hash 算法；
	- JDK 1.8 前为什么会发生死锁；

## 数据结构
		- 线性表、链表、队列
		- 树、二叉树、堆、AVL 树、红黑树、B 树、B+ 树；
		- 二叉树的前中后序遍历；
		- 图及图的遍历；
		- 哈希表及哈希冲突；

		
## Java 的实现

### 集合包和并发包的继承结构

- 集合包：java.util.collection 包下面的类，这个包从 JDK 1.2 开始提供 Java 数据结构实现相关内容。包中线程安全类基本上使用 synchronized 关键字做的方法同步，在 JDK 1.8 前效率都很低。

- collection：集合接口，集合包的元素不超过 Integer.MAX\_VALEU 都是可以动态扩容的。
	- List：
		- BlockingQueue：阻塞队列，采用新锁，当队列满的时候会阻塞写入操作，当队列空的时候会阻塞消费操作，其子接口 Deuque 实现了双端队列。
			- LinkedBlockingQueue：基于链表实现的阻塞队列；
			- ArrayBlockingQueue：数组实现的阻塞队列；
			- DelayQueue：基于链表实现的延迟队列，写入元素要实现 Delay 接口，元素在指定时间后才可读；
			- PriorityQueue：带有优先级的队列，取出的元素保证是优先级最高的元素，使用堆来实现。
		- ArrayList：基于数组实现；
		- LinkedList：基于链表实现；
	- Set：数据不能重复。
		- HashSet：线程不安全的 set，基于 HashMap 实现，只用了 key 部分；
		- SortedSet：元素是排序且数据元素不能重复；
			- TreeSet：线程不安全的 set，元素是有序的基于 TreeMap 实现；
- Map：字典接口，元素可以使用 key - value 方式存储，元素数量不超过 Integer.MAX\_VALUE 都是可以动态扩容的。
	- SortedMap：元素为有序的 Map，key 要实现 compare 接口来做排序比较
		- TreeMap：基于红黑树实现的有序 map；
	- HashMap：线程不安全的 map，冲突解决方案为转换为冲突链，JDK 1.8 优化冲突链超过阈值（默认 8）转换为红黑是；
	- HashTable：线程安全的 map，基本上就是 HashMap 的方法加 synchronized 关键字；
	- ConcurrentHashMap：线程安全且高效的 map，采用 segment 将元素分段，做到分段加锁降低锁粒度，并且采用 lock 接口的锁，可进一步实现读锁、写锁的拆分提高并发度。

## 线性表

Java 支持的线性表接口：

- List：定义了线性表的基础操作方法；
- Queue：定义了队列接口，方法和 List 方法的不同是，规定队空返回 null 而不是抛出异常；
- Deque：定义了双端队列接口，在 Queue 接口的基础上扩展了头插和尾取方法；
- BlockingQueue：阻塞队列，在 Queue 接口的基础上规定队满方法 尾插调用要被阻塞等待，

Java 的线性表实现类

- ArrayList：基于数组实现的线性表，随机读效率高；
- LinkedList：基于链表实现的线性表，随机插入效率高；
- 

## 队列：Queue、Deque、LinkedList、BlockingQueue、BlockedLinkedList、SychronizedQueue、TransforQueue

## 栈：Stack、Vector

## 哈希表：Map、SortedMap、HashMap、ConcurrentHashMap、TreeMap、LinkedHashMap


