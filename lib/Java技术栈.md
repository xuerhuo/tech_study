# Java基础

***知识细节*** 


- Java三大特性
   - 封装
   - 继承
   - 多态 
- 注解
- 反射
- 代理
  - 动态代理
  - 静态代理
- 构造器初始化顺序
- 接口
- 抽象类
- 接口与抽象类比较
![avatar](https://github.com/sanwancoder/it_study_lib/blob/master/images/%E6%8E%A5%E5%8F%A3%E4%B8%8E%E6%8A%BD%E8%B1%A1%E7%B1%BB%E6%AF%94%E8%BE%83.jpg?raw=true)
- 集合
   - List
      - ArrayList
         - 底层数据结构是 ***数组***
      - LinkedList
         - 底层数据结构是 ***链表***  
   - Set 
   	   - HashSet
   	      - 底层数据结构是 ***哈希表***
   	   - TreeSet
   	      - 底层数据结构是 ***红黑树***
   	   - LinkedHashSet 
   	      - 底层数据结构是 ***双向链表*** 
   - Map
   	   - HashMap
   	      - 底层数据结构是 ***数组+链表***
   	      - 不是线程安全的
   	      - JDK 1.8中对HashMap的实现做了优化,当链表中的节点数据超过八个之后,该链表会转为红黑树来提高查询效率,从原来的 O(n)到 O(logn)
   	   - HashTable
   	   - Properties
   	   - LinkedHashMap
   	      -   
- 锁
- ==与equals比较
   - TODO 
- 
```java
public class Test {
	public static void main(String[] args) {
		String a = new String("ab"); // a 为一个引用
		String b = new String("ab"); // b 为另一个引用,对象的内容一样
		String aa = "ab"; // 放在常量池中
		String bb = "ab"; // 从常量池中查找
		if (aa == bb) // true
			System.out.println("aa==bb");
		if (a == b) // false，非同一对象
			System.out.println("a==b");
		if (a.equals(b)) // true
			System.out.println("aEQb");
		if (42 == 42.0) { // true
			System.out.println("true");
		}
	}
}
``` 


- 浅拷贝与深拷贝

- String StringBuffer StringBuilder比较
    - String 是final的，线程安全
    - StringBuffer 线程安全
    - StringBuilder 线程不安全

- Java 异常
![avatar](https://github.com/sanwancoder/it_study_lib/blob/master/images/Java%E5%BC%82%E5%B8%B8%E7%B1%BB%E5%B1%82%E6%AC%A1%E5%9B%BE.png?raw=true)
- 序列化
   - 对于不想进行序列化的变量，使用transient关键字修饰 


#JavaWeb
- 集群环境下如何实现Session共享
   - ***粘性Session:*** 是指将用户锁定到某一个服务器上；缺乏容错性，如果当前访问的服务器发生故障，用户被转移到第二个服务器上时，他的 session 信息都将失效。
   - ***Session复制:*** 任何一个服务器上的 session 发生改变（增删改），该节点会把这个 session 的所有内容序列化，然后广播给所有其它节点。如果 session 量大的话可能会造成网络堵塞，拖慢服务器性能。
   - ***Session共享:*** 使用分布式缓存方案如 redis 集群。可容错，session 实时响应。 



- Servlet


- RESTFul
   - 网址参考
   	   - [阮一峰 RESTful API 最佳实践](http://www.ruanyifeng.com/blog/2018/10/restful-api-best-practices.html)   



***Java基础面试***

- 参考网址
   - [JAVA面试精选【Java基础第一部分】博客园](https://www.cnblogs.com/hnlshzx/p/3491587.html)
   - [JAVA面试精选【Java基础第二部分】博客园](https://www.cnblogs.com/hnlshzx/p/3492197.html)
   - [JAVA面试精选【Java基础第三部分】博客园](https://www.cnblogs.com/hnlshzx/p/3493449.html)


# 多线程部分

- **视频讲解资料**
   - [马士兵老师java多线程高并发编程
](https://www.bilibili.com/video/av33688545) *注意播放顺序*


***知识细节***



- 实现多线程方法
   - ***继承Thread类:*** 
   - ***实现Runnable接口:*** 重写Run()方法，创建Runnable实例，并以此实例作为Thread类的 target（目标）参数创建Thread对象,调用 Thread 对象的start()启动线程。
   - ***ExecutorService接口:*** 

***多线程面试题***
- 参考网址
   - [Java线程面试题 Top 50 - ImportNew](http://www.importnew.com/12773.html)
   - [多线程面试题 - 掘金](https://juejin.im/post/5b010a016fb9a07a99191ff7)


# JVM知识汇总
- 视频
- 其他补充
  - [JVM知识点总览-高级Java工程师面试必备](http://www.importnew.com/23792.html) 

***知识细节***

- JVM内存模型

![avatar](https://github.com/sanwancoder/it_study_lib/blob/master/images/jvm%E5%86%85%E5%AD%98%E7%BB%93%E6%9E%84.jpg?raw=true)

   - 堆区:Java虚拟机所管理的内存中最大的一块。Java堆是被所有线程共享的一块内存区域，在虚拟机启动时创建。此内存区域的唯一目的就是存放对象实例，几乎所有的对象实例都在这里分配内存。
   - 方法区:方法区（Method Area）与Java堆一样，是各个线程共享的内存区域，它用于存储已被虚拟机加载的类信息、常量、静态变量、即时编译器编译后的代码等数据。
   - 虚拟机栈:线程私有的，它的生命周期与线程相同。虚拟机栈描述的是Java方法执行的内存模型：每个方法被执行的时候都会同时创建一个栈帧（Stack Frame）用于存储局部变量表、操作栈、动态链接、方法出口等信息。
   - 本地方法栈:为虚拟机使用到的Native方法服务。
   - 程序计算器
- JDK和JRE
   - JDK是Java Development Kit	,它是功能齐全的Java SDK。它拥有JRE所拥有的一切，还有编译器（javac）和工具（如javadoc和jdb）。它能够创建和编译程序。
   - JRE是Java运行时环境。它是运行已编译Java程序所需的所有内容的集合，包括 Java虚拟机（JVM），Java 类库，java命令和其他的一些基础构件。但是，它不能用于创建新程序。


# 数据结构部分

- 栈
- 列表
- 哈希表
- 树








# 书籍推荐
  - 《Java多线程编程核心技术》
  - 《Java并发编程实践》
  - 《深入理解Java虚拟机  JVM高级特性与最佳实践》 周志明 著


      

