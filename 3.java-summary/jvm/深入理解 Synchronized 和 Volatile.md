# 深入理解 synchronized 

## 语法

- `synchronized`：修饰某个方法或某个代码块儿，某线程运行此代码块儿时，会先获对象锁，只有获取了此对象锁才能运行 `synchronized` 修饰的方法或代码块儿；
	- 修饰类方法：表示需要获取此 `对象锁`，等同 `synchronized(this){}`;
	- 修饰静态方法：表示需要获取此 `类对象锁`，等同 `synchronized(XX.class){}`;
	- 优点：简单易用，实现多线程操作共享内存时的数据同步和保护；
	- 缺点：降低并发度，加解锁效率依赖于 JVM 的优化；

## 基础原理





## 深入过程

- java 编译器将 java 文件编译为 class 文件时，遇到 `synchronized` 块儿时需要转换为 `monitorenter` 和 `monitorexit` 两条指令；
- `monitorenter` 表示线程执行到此处时需要获取前一条 `astore_x` 存储的对象对象锁；
- 如果 `monitorenter` 获取不到锁，则线程执行到此处会 `"阻塞"` 住，直到获取到锁为止，此时 Thread 的状态为 `WATING` ；
- `monitorexit` 表示线程执行到此处时释放当前持有的对象锁，具体释放的锁是前一条 `astore_x` 存储的对象；

### monitor、monitorenter、monitorexit 执行原理

`monitorenter` 在 JVM 层面是一个方法实现，此方法中

 
