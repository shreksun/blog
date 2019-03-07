---
title: IO
date: 2019-03-07 15:34:38
tags: javaIO
categories:
- Java
---

#### 输入字节流InputStream:

* **ByteArrayInputStream、StringBufferInputStream、FileInputStream** 是三种基本的介质流，它们分别从Byte 数组、StringBuffer、和本地文件中读取数据。
* **PipedInputStream** 是从与其它线程共用的管道中读取数据。PipedInputStream的一个实例要和PipedOutputStream的一个实例共同使用，共同完成管道的读取写入操作。主要用于线程操作。
* **DataInputStream**： 将基础数据类型读取出来
* **ObjectInputStream** 和所有 **FilterInputStream** 的子类都是装饰流（装饰器模式的主角）。

<!--more-->

#### 输出字节流OutputStream：

* **ByteArrayOutputStream**、**FileOutputStream**： 是两种基本的介质流，它们分别向- Byte 数组、和本地文件中写入数据。
* **PipedOutputStream** 是向与其它线程共用的管道中写入数据。
* **DataOutputStream** 将基础数据类型写入到文件中
* **ObjectOutputStream** 和所有 **FilterOutputStream** 的子类都是装饰流。

#### 字符输入流Reader：

- **FileReader、CharReader、StringReader** 是三种基本的介质流，它们分在本地文件、Char 数组、String中读取数据。
- **PipedReader**：是从与其它线程共用的管道中读取数据
- **BufferedReader** ：加缓冲功能，避免频繁读写硬盘
- **InputStreamReader**： 是一个连接字节流和字符流的桥梁，它将字节流转变为字符流。

#### 字符输出流Writer：

- **StringWriter**:向String 中写入数据。
- **CharArrayWriter**：实现一个可用作字符输入流的字符缓冲区
- **PipedWriter**:是向与其它线程共用的管道中写入数据
- **BufferedWriter** ： 增加缓冲功能，避免频繁读写硬盘。
- **PrintWriter** 和**PrintStream** 将对象的格式表示打印到文本输出流。 极其类似，功能和使用也非常相似
- **OutputStreamWriter**： 是OutputStream 到Writer 转换的桥梁，它的子类FileWriter 其实就是一个实现此功能的具体类（具体可以研究一SourceCode）。功能和使用和OutputStream 极其类似，后面会有它们的对应图。

源引[Java IO，硬骨头也能变软](https://mp.weixin.qq.com/s?__biz=MzU4NDQ4MzU5OA==&mid=2247483981&idx=1&sn=6e5c682d76972c8d2cf271a85dcf09e2&chksm=fd98542ccaefdd3a70428e9549bc33e8165836855edaa748928d16c1ebde9648579d3acaac10#rd)