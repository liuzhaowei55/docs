---
title: Thread pool
date: 2022-02-24
---

# Java 线程池

## 常用线程池实现类

```java
package java.util.concurrent

public class ThreadPoolExecutor extends AbstractExecutorService {
    /**
     * 核心线程数
     */
    private volatile int corePoolSize;
    /**
     * 最大线程数
     */
    private volatile int maximumPoolSize;
    /**
     * 超过核心线程数的线程存活等待时间，单位 ns
     */
    private volatile long keepAliveTime;
    /**
     * 阻塞队列
     */
    private final BlockingQueue<Runnable> workQueue;
    /**
     * Thread 工厂类
     */
    private volatile ThreadFactory threadFactory;
    /**
     * 当任务数超过线程池队列，且运行最大线程数超过配置后的拒绝策略
     */
    private volatile RejectedExecutionHandler handler;
}
```

## 参考文献

- [Java 线程池参数的合理设置](https://www.modb.pro/db/65544)
- [Java 线程池实现原理及其在美团业务中的实践](https://tech.meituan.com/2020/04/02/java-pooling-pratice-in-meituan.html)
