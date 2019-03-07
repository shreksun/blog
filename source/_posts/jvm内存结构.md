---
title: jvm内存结构
date: 2019-03-07 17:27:23
categories:
- Java
tags:
- JVM
---

JVM内存结构主要有三大块：**堆内存**、**方法区**和**栈**

<!--more-->

控制参数

- -Xms设置堆的最小空间大小。
- -Xmx设置堆的最大空间大小。
- -XX:NewSize设置新生代最小空间大小。
- -XX:MaxNewSize设置新生代最大空间大小。
- -XX:PermSize设置永久代最小空间大小。
- -XX:MaxPermSize设置永久代最大空间大小。
- -Xss设置每个线程的堆栈大小。

#### Java堆

- **特点**：各线程共享，垃圾回收管理的主要区域。可以动态地分配内存大小、比较灵活，生命周期不固定。
- **存放**：new的对象和数组 this

#### 方法区

* **特点**：各线程共享，堆内存又被划分成不同的部分：伊甸区(Eden)，幸存者区域(Survivor Sapce)，老年代（Old Generation Space）。
* **存放**：已被加载的类信息，常量，静态变量，即时编译器编译后代码。

#### 程序计数器

* 当前线程所执行的字节码的行号指示器。
* 如果正在执行的是Natvie方法，这个计数器值则为空（Undefined）。

#### JVM栈（JVM Stacks）

* **它的生命周期与线程相同。虚拟机栈描述的是Java方法执行的内存模型：**每个方法被执行的时候都会同时创建一个栈帧（Stack Frame）用于存储局部变量表、操作栈、动态链接、方法出口等信息。**每一个方法被调用直至执行完成的过程，就对应着一个栈帧在虚拟机栈中从入栈到出栈的过程。**
* **存放**：局部变量，基本数据类型，对象引用。
* 特点：大小固定，编译期间完成分配空间。

参考：

[JVM内存结构](https://mp.weixin.qq.com/s?__biz=MzI4NDY5Mjc1Mg==&mid=2247483949&idx=1&sn=8b69d833bbc805e63d5b2fa7c73655f5&chksm=ebf6da52dc815344add64af6fb78fee439c8c27b539b3c0e87d8f6861c8422144d516ae0a837&scene=21#wechat_redirect)

[堆和栈](https://www.jianshu.com/p/bfa5337ef59e)







