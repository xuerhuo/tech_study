# Java基础

***知识细节***</br>

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
         - 底层数据结构是***数组***
      - LinkedList
         - 底层数据结构是***链表***  
   - Set 
   	   - HashSet
   	      - 底层数据结构是***哈希表*** 
   	   - TreeSet
   	      - 底层数据结构是***红黑树***
   	   - LinkedHashSet 
   	      - 底层数据结构是***双向链表*** 
   - Tree
   - Map
   	   - HashMap
   	      - 底层数据结构是***数组+链表***
   	      - JDK 1.8中对HashMap的实现做了优化,当链表中的节点数据超过八个之后,该链表会转为红黑树来提高查询效率,从原来的 O(n)到 O(logn)
   	   - LinkedHashMap
   	      -   
- 锁




#JavaWeb
- 集群环境下如何实现Session共享
   - ***粘性Session:*** 是指将用户锁定到某一个服务器上；缺乏容错性，如果当前访问的服务器发生故障，用户被转移到第二个服务器上时，他的 session 信息都将失效。
   - ***Session复制:*** 任何一个服务器上的 session 发生改变（增删改），该节点会把这个 session 的所有内容序列化，然后广播给所有其它节点。如果 session 量大的话可能会造成网络堵塞，拖慢服务器性能。
   - ***Session共享:*** 使用分布式缓存方案如 redis 集群。可容错，session 实时响应。 



# 多线程部分
- **视频讲解资料**
   - [马士兵老师java多线程高并发编程
](https://www.bilibili.com/video/av33688545) *注意播放顺序*


***知识细节***</br>

- 实现多线程方法
   - ***继承Thread类:*** 
   - ***实现Runnable接口:*** 重写Run()方法，创建Runnable实例，并以此实例作为Thread类的 target（目标）参数创建Thread对象,调用 Thread 对象的start()启动线程。
   - ***ExecutorService接口:*** 



# JVM知识汇总
- 视频
- 其他补充
  - [JVM知识点总览-高级Java工程师面试必备](http://www.importnew.com/23792.html) 

***知识细节***</br>

- JVM内存模型

![avatar](https://github.com/sanwancoder/it_study_lib/blob/master/images/jvm%E5%86%85%E5%AD%98%E7%BB%93%E6%9E%84.jpg?raw=true)

   - 堆区:Java虚拟机所管理的内存中最大的一块。Java堆是被所有线程共享的一块内存区域，在虚拟机启动时创建。此内存区域的唯一目的就是存放对象实例，几乎所有的对象实例都在这里分配内存。
   - 方法区:方法区（Method Area）与Java堆一样，是各个线程共享的内存区域，它用于存储已被虚拟机加载的类信息、常量、静态变量、即时编译器编译后的代码等数据。
   - 虚拟机栈:线程私有的，它的生命周期与线程相同。虚拟机栈描述的是Java方法执行的内存模型：每个方法被执行的时候都会同时创建一个栈帧（Stack Frame）用于存储局部变量表、操作栈、动态链接、方法出口等信息。
   - 本地方法栈:为虚拟机使用到的Native方法服务。
   - 程序计算器


# 数据结构部分
- 栈
- 列表
- 哈希表
- 树





# 设计模式

- 设计模式六大原则
   - 组合复用原则：多用组合，少用继承。
   - 依赖倒置原则：要依赖于抽象，不要依赖具体；高层模块不应该底层模块。
   - 开闭原则：对扩展开放，对修改关闭。
   - 里氏替换原则：所有引用基类的地方必须能透明地使用其子类对象；子类能扩展父类的功能时不能破坏父类原有的功能；子类可以实现父类的抽象方法，但不能覆盖父类的非抽象方法；当子类重载父类方法时，
方法的形参要比父类的方法的参数更宽松；当子类实现父类的抽象方法时，方法的返回值要比父类更严格。
   - 迪米特法则：一个对象应该与其他对象保持最少的了解。只与直接朋友交谈。
   - 单一职责原则：一个类只负责一项职责。

- 模式分类
   - 创建型模式(简单工厂模式不是GoF总结出来的23种设计模式之一)[来源](https://github.com/jiayisheji/blog/issues/2)
       - ***简单工厂模式（Simple Factory）***
		- 工厂方法模式（Factory Method）
		- 抽象工厂模式（Abstract Factory）
		- 创建者模式（Builder）
		- 原型模式（Prototype）
		- 单例模式（Singleton）
   - 结构型模式：
	   - 外观模式/门面模式（Facade门面模式）
		- 适配器模式（Adapter）
		- 代理模式（Proxy）
		- 装饰模式（Decorator）
		- 桥梁模式/桥接模式（Bridge）
		- 组合模式（Composite）
		- 享元模式（Flyweight）
   - 行为型模式：
       - 模板方法模式（Template Method）
       - 观察者模式（Observer）
       - 状态模式（State）
       - 策略模式（Strategy）
       - 职责链模式（Chain of Responsibility）
		- 命令模式（Command）
		- 访问者模式（Visitor）
		- 调停者模式（Mediator）
		- 备忘录模式（Memento）
		- 迭代器模式（Iterator）
		- 解释器模式（Interpreter）

- 单例模式



# 书籍推荐
  - 《Java多线程编程核心技术》
  - 《Java并发编程实践》
  - 《深入理解Java虚拟机  JVM高级特性与最佳实践》 周志明 著


      

