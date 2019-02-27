# 知识网络

> 简单内容直接呈现，复杂内容链接文章
## IT技术基础
### 计算机原理
#### 二进制
#### 编码
### 计算机网络
### 数据结构与算法
#### 简单的数据结构
栈、队列、链表、数组、哈希表、

栈和队列的相同和不同之处

栈通常采用的两种存储结构
#### 树
二叉树、字典树、平衡树、排序树、B树、B+树、R树、多路树、红黑树
#### 堆
大根堆、小根堆
#### 图
有向图、无向图、拓扑
#### 排序算法
稳定的排序：冒泡排序、插入排序、鸡尾酒排序、桶排序、计数排序、归并排序、原地归并排序、二叉排序树排序、鸽巢排序、基数排序、侏儒排序、图书馆排序、块排序

不稳定的排序：选择排序、希尔排序、Clover排序算法、梳排序、堆排序、平滑排序、快速排序、内省排序、耐心排序

各种排序算法和时间复杂度
#### 深度优先和广度优先搜索
二叉树的深度优先遍历与广度优先遍历

图的深度优先搜索和广度优先搜索
#### 全排列算法
字典序法、递增进位制数法、递减进位制数法、邻位对换法
#### 分治算法
#### 动态规划算法
#### 贪心算法
获取局部最优解
#### 回溯法
#### 分支限界法
#### KMP算法(字符串匹配算法)
#### hash算法
### 编译原理
### 操作系统
### 数据库原理
## Java基础
### 理念
#### 面向对象
- **面向对象**：将一类事物抽象成类，将事物的属性抽象成属性，事物的行为抽象成方法，然后将其封装起来的编程思想。重点关注的是对象。
- **面向过程**：重点关注的是执行步骤，利用函数将每个步骤实现逐个调用的方式。

面向对象的三大基本特征和五大基本原则
- **三大特征**
    - 封装
    - 继承
    - 多态
- **五大原则**
    - 单一职责原则
    - 开放封闭原则
    - 里氏替换原则
    - 依赖倒置原则
    - 接口隔离原则
#### 值传递
值传递、引用传递

为什么说Java中只有值传递
#### 三大特性：封装、继承、多态
什么是多态

- [方法重写与重载]

- [Java的继承与实现]

构造函数与默认构造函数

- 类变量、成员变量和局部变量
    - 类变量：在类内部定义，由static修饰的变量，可由类名点用（无需创建对象使用），共享使用，在类加载阶段完成赋值操作（可直接赋值，静态块赋值，静态方法赋值）
    - 成员变量：在类内部定义，需要使用对象调用，每个对象有一个自己的变量，不共享，在创建对象时赋值（可直接赋值，构造器赋值，块赋值，成员方法赋值等）
    - 局部变量：方法内定义，只在方法内有效，天生线程安全。

- [成员变量和方法作用域]

- [接口和抽象类]

- [四大内部类]
    - 成员内部类：定义在另一个类内部的非静态内部类，级别和成员变量和方法一致，依附于外部类而存在
    - 静态内部类：定义在另一个类内部的静态内部类（static修饰），超脱了外部类而存在
    - 局部内部类：定义在一个方法或者一个作用于（{}）中的内部类，与方法的局部变量一致，只在作用域内有效
    - 匿名内部类：直接通过new 接口的方式定义个内部类，不存在类名，函数式接口的匿名内部类可以使用Lambda表达式来替换。

### 基本数据类型
- 8种基本数据类型：
    - byte：1字节，-128~127（-2<sup>7</sup>~2<sup>7</sup>-1）
    - short：2字节，-32768~32717（-2<sup>15</sup>~2<sup>15</sup>-1）
    - int：4字节，-2147483648~2147483647（-2<sup>31</sup>~2<sup>31</sup>-1）
    - long：8字节，-9223372036854775808~9223372036854775807（-2<sup>63</sup>~2<sup>63</sup>-1）
    - float：4字节，单精度浮点数，二进制科学计数法表示，1.401298e-45~3.402823e+38
    - double：8字节，双精度浮点数，二进制科学计数法表示，4.9000000e-324~1.797693e+308
    - char：2字节，0~65535
    - boolean：1字节，0~1
- 基本数据类型的产生的历史原因：其实是为了兼容C语言的模式，为C语言开发者转Java提供方便
- [整型和浮点型的二进制表示形式与计算原理]
- [什么是浮点型]
- [什么是单精度和双精度]
- **为什么不能用浮点型表示金额**：因为使用浮点数能精确表示的小数很少，大部分都无法精确表示，这和十进制无法精确表达1/3一样。
- [浮点数为什么不精确？为什么银行的金额不能用浮点数计算](https://blog.csdn.net/keke_xin/article/details/84831024)
### 自动拆装箱
- **什么是包装类型**：包装类型是针对八个基本数据类型定义的包装类，用于在面向对象的Java中执行一些只有对象才能执行的操作。
- **什么是自动拆装箱**：拆装箱就是基本类型和包装类型的转换操作，由编译器来完成拆装箱操作。
- [Integer的缓存机制](Java_Technology\Java_Base_Technology\Integer的缓存机制.md)（享元模式：池）
- [Integer的缓存机制](https://blog.csdn.net/yrwan95/article/details/82785129)
- Byte、Short、Long的均是将-128到127缓存起来备用。
- 包装类型的比较需要使用equals，不能直接使用==，除非将其手动转换为基本类型。
### String
- [字符串的不可变性](https://blog.csdn.net/qunzer/article/details/25157309)：String类被final修饰，是为最终类，不可被继承修改,且底层保存字符序列的字符数组也被final修饰，一旦赋值不再改变，这是String不变的原理。这种不变性也保证了其可以作为Map中键的常客。
- [JDK 6和JDK 7中substring的原理及区别](Java_Technology\Java_Base_Technology\JDK 6和JDK 7中substring的原理及区别.md)
- replaceFirst、replaceAll、replace区别
    - replace：使用新字符替换所有旧字符，字符的替换操作
    - replaceFirst：使用给定的字符序列根据给定的正则表达式替换第一次出现的旧字符序列，字符序列的替换操作，涉及正则表达式，只替换首个出现的匹配的旧字符序列
    - replaceAll：使用给定的字符序列根据给定的正则表达式替换所有旧的字符序列，replaceFirst的加强版，替换所有匹配的旧字符序列
- String对“+”的重载：String的+操作符在编译阶段会被编译为StringBuilder的appand操作和toString操作的整合版。（语法糖）
- 字符串拼接的几种方式和区别
    - +：效率最慢，少数字符串或者数值拼接时使用，直观
    - concat方法：通过Arrays.copyOf()实现拼接，适用于字符串少的拼接
    - String.format方法：
    - StringUtils.join()：org.apache.commons.lang3中提供的方式，通过StringBuilder实现拼接
    - String.join()：JDK 1.8中新增的方式，通过StringBuilder实现拼接
    - StringBuilder：速度最快速的方式
- String.valueOf和Integer.toString的区别：前者拥有诸多重载方法，用于将各种类型的对象转换成字符串，后者是单单对整型而言的转字符串方法。
- switch对String的支持（语法糖）：JDK 1.7新增功能，switch比较的是字符串常量的哈希值（int类型），但是hash值可能会有冲突，所以还需要再调用equals方法进行二次比较。[Java1.7增加switch对字符串的支持](https://blog.csdn.net/troyaninpc/article/details/79475474)
- switch支持以下类型：
    - 基本数据类型：byte, short, char, int
    - 包装数据类型：Byte, Short, Character, Integer
    - 枚举类型：Enum
    - 字符串类型：String（Jdk 7+ 开始支持）
- 字符串常量池
    字符串常量池和运行时常量池不同，后者是class文件私有的，每个class文件有一个运行时常量池，而字符串常量池是公共的，全局的。
    JDK 1.6之前，字符串常量池位于方法区，JDK1.7开始挪到了堆内存。
    使用字面量创建字符串，会直接在字符串常量池中查找有无指定的字符串字面值，有则直接返回其引用，没有就在池中创建一个字面量并返回其引用。
    使用new方式创建字符串，会直接在堆内存中创建一个String对象，这个对象保存着一个字符串字面值，这时与字符串常量池无关。
    当我们对字符串执行intern之后，将会触发下面的操作。
- intern
intern方法的作用是在常量池中保留字符串的一份引用或者字面值。
- JDK 1.6
    - 若字符串常量池中有指定的字符串常量值，则直接返回该值的地址，将new方式在堆中创建的字符串替换为这里的地址
    - 若字符串常量池中没有指定的字符串常量值，则在常量池中创建一个同样的字符串，并将其地址返回给栈引用。
- JDK 1.7
    - 同上
    - 若字符串常量池中没有指定的字符串常量值，则在常量池中保留一份堆中字符串的引用地址。 
### 关键字
- [Java关键字](https://www.cnblogs.com/chenglc/p/6922834.html)
- transient原理及用法：使用于序列化机制中，用于屏蔽不想参与序列化的字段，被其修饰的字段不参与序列化与反序列化。一般使用writeObject和readObject方法来自定义其值的序列化与反序列化，通常是直接写入流中或从流中获取赋值。
- [instanceof原理及用法]()
- [volatile原理及用法]()
- [synchronized原理及用法]()
- [final原理及用法]()
- [static原理及用法]()
- const原理及用法：C/C++中的关键字，Java中作为保留字存在，和goto一样
### 集合
- 常用集合类的使用
    - ArrayList：数组实现的列表，查找元素速度快，增删元素较慢，适用于保存偏于查询的数据
    - LinkedList：链表实现的列表，同时也是队列，增删匀速快，查询元素慢，适用于保存偏于增删操作的数据
    - HashMap：基于Hash实现的键值对集合，查找元素快，适用于做缓存，偏于查询，保存元素涉及扩容
    - HashSet：基于hash实现的无序集合，用于保存不重复的数据，可用于去重
    - TreeMap：基于红黑树实现的键值对集合，天然有序，用于保存有序的键值对数据
    - TreeSet：基于红黑树实现的无序集合，天然有序，用于保存有序的去重数据
    - **LinkedHashMap**：基于Hash和链表实现的键值对集合，保存了插入顺序。其实就是对HashMap的所有元素使用一个链表连起来罢了。视为一个有序的HashMap
    - **LinkedHashSet**：同上，视为有序的HashSet
- [ArrayList和LinkedList和Vector的区别](https://www.cnblogs.com/yw-ah/p/5841327.html)
- SynchronizedList和Vector的区别
    - SynchronizedList有很好的扩展和兼容功能。他可以将所有的List的子类转成线程安全的类,Vector底层固定只能是数组
    - 使用SynchronizedList的时候，进行遍历时要手动进行同步处理
    - SynchronizedList可以指定锁定的对象
- HashMap、HashTable、ConcurrentHashMap区别
    - HashMap：线程不安全的键值对集合
    - HashTable：线程安全的键值对集合，使用synchronized加锁实现线程安全，效率较低
    - ConcurrentHashMap：线程安全的键值对集合，使用原子操作+synchronized实现，效率更高，推荐使用
- Set和List区别？
    - Set特点：无序-不可重复-可保存null值但只能有一个
    - List特点：有序-可重复-可保存多个null值
- Set如何保证元素不重复？
    Set一般底层以Map来实现，可以说Set就是一个value为固定值的Map，那么Set保存的值映射到Map，就是Map的key，key当然不能重复，如果key重复那么
- [Java 8中stream相关用法]
- [apache集合处理工具类的使用]
- [不同版本的JDK中HashMap的实现的区别以及原因]
- Collection和Collections区别
    - Collection是集合的基础接口定义了一些公共的方法。
    - Collections是集合工具类，主要用于操作集合：排序、反转、拷贝、查找、定位等功能
- Arrays.asList获得的List使用时需要注意什么
    - Arrays.asList获取到的ArrayList是Arrays的一个内部类，表示一个不可改变的列表，不同于JUC中的ArrayList。
    - 前者返回的ArrayList不能添加元素
    - 而且操作asList的时候，必须是引用类型的值（比如：Integer、Long等），不能是原始类型（比如：int、long之类）
- Enumeration和Iterator区别
    二者都是用来遍历集合的，前者是JDK 1.0就出现的遍历工具，实现者包括Vector、HashTable等，后者是在JDK 1.2中新增的，新的集合框架就是在其基础上扩展开来的。
    前者只有两个方法，只能用于遍历获取元素，后者多一个方法，可以执行元素删除操作，而且后者支持fast-fail：当多个线程对同一个集合的内容进行操作时，就可能会产生fail-fast事件。
- [fail-fast 和 fail-safe的区别](https://blog.csdn.net/u010889616/article/details/79954413)
    fail-fast：快速失败，ju包下的集合类均是快速失败的，当多个线程对同一个集合进行操作，就可能产生fail-fast。
    fail-safe：安全失败，所有针对同一集合结构的更改操作都会在一个复制的集合上进行。
- CopyOnWriteArrayList
    
- ConcurrentSkipListMap
    
### 枚举
- [深入理解Java枚举类型(enum)](https://blog.csdn.net/javazejian/article/details/71333103)
- 枚举的用法
    - 枚举可以实现多个接口
    - 可以定义新的变量
    - 可以定义新的方法
    - 可以定义根据具体枚举值而相异的类
    - 可以定义抽象方法，并由枚举值实现，使用大括号（{}）来进行定义。
- [枚举的实现原理](Java_Technology/Java_Base_Technology/枚举实现原理.md)：枚举是通过语法糖实现的额，枚举类被编译之后，就能看出其大致结构。
- **枚举与单例**：都说枚举是实现单例最简单有效的方式。确实，即使是序列化机制也不会导致多实例产生。
- Enum类：[Enum深入解析](Java_Technology/Java_Base_Technology/Enum深入解析.md)
- **Java枚举如何比较**：使用equals和==都可以进行比较，因为每个枚举都是单例的，是天然单例，其equals就是使用==实现的。[比较java枚举成员使用equal还是==](https://www.cnblogs.com/xiohao/p/7405423.html)
- **switch对枚举的支持**：枚举在jdk1.5出现，switch在jdk 1.6中支持枚举。这是一种编译器的语法糖。
    我们都知道在class文件中switch判断只支持int类型。那么枚举是怎么转换的呢？其实底层使用的是枚举类的ordinal方法，即枚举值的序列值，这和switch支持的String差不多，这也是一种语法糖，底层判断的是字符串的hashCode。
- **枚举的序列化如何实现**：[深度分析 Java 的枚举类型：枚举的线程安全性及序列化问题](http://blog.jobbole.com/94074/)
    枚举的序列化是由JVM所控制，禁用的定制方法，所以其实永远的单例。
- 枚举的线程安全性问题
### 注解
- [深入理解Java注解类型(@Annotation)](https://blog.csdn.net/javazejian/article/details/71860633)
- [元注解](Java_Technology/Java_Base_Technology/元注解.md)：用于标注注解的注解，标注在注解类之上的注解。定义注解的注解。
    - @Target：指明目标注解的作用范围
    - @Retention：指明目标注解的生命周期
    - @Documented：指明该注解将被包含在javadoc中
    - @Inherited：指明子类可以继承父类中的该注解
- [自定义注解](Java_Technology/Java_Base_Technology/自定义注解.md)
- [Java中常用注解使用](Java_Technology/Java_Base_Technology/Java中常用注解使用.md)
    - @Override：方法重写
    - @Deprecated：方法弃用
    - @Suppvisewarnings：忽略警告
- [注解与反射的结合](Java_Technology/Java_Base_Technology/注解与反射结合使用.md)
- [Spring常用注解] 
### 泛型
- **泛型**：Java编译器语法糖的一种，泛型只在编译期有效，编译器会执行类型擦除，来去掉泛型。
- 泛型与继承
- **类型擦除**：编译阶段，编译器在完成类型检查之后就会执行类型擦除，将泛型去除。
- 泛型中K T V E ? Object等的含义
    - K T V E这些其实是一样的，我们还可以使用其他任意的大写字母来替换它们，只是这几个经常使用罢了，它们表示一个具体的类型
    - ?表示不限定类型，
    - ? extends Father表示只能使用Father类型和其子类型。
    - ? super Son表示只能使用Son类型和其父类型
    - Object则表示任意类型均可以使用
- [泛型各种用法](Java_Technology/Java_Base_Technology/泛型各种用法.md)
- 限定通配符和非限定通配符
    - 限定通配符：? extends XXX、? super XXX
    - 非限定通配符：?
- 上下界限定符extends 和 super
    - 上界定符extends：将指定的类型作为上限，只允许使用指定类型及其子类型
    - 下界定符super：将指定类型作为下限，只允许使用指定类型及其父类型
- List<?>和List\<Object\>、List之间的区别
    - List：原始类型，可以使用任意类型，可以添加任意类型元素。
    - List\<?\>：通配符类型，形参，可以接受任何对应List<E>的参数化类型，包括List，来作为实参，形参并不能添加元素。
    - List\<Object\>：类型参数为Object的参数化类型，实参，仅仅能够接受List和其本身类型，可以添加任意类型元素。
### 异常
- [Java 中的异常和处理详解](http://www.importnew.com/26613.html)
- [如何优雅的设计 Java 异常](http://www.importnew.com/28000.html)
- **异常类型**
    - 错误Error
        - AssertionError：抛出断言失败错误
        - OutOfMemoryError：抛出内存溢出错误，当JVM没有多余内存来存放目标对象，并且使用GC垃圾回收之后仍然无多余内存来保存目标对象
        - StackOverflowError：堆栈溢出错误，递归太深导致堆栈溢出
    - 异常Exception
        - 受检异常（编译期异常）
            - ClassNotFoundException
            - CloneNotSupportedException
            - FileAlreadyExistsException
            - FileNotFoundException
            - InterruptedException
            - IOException
            - SQLException
            - TimeoutException
            - UnknownHostException
        - 非受检异常（运行时异常）
            - AlreadyBoundException
            - ClassCastException：类转换异常，将一个实例转化为非其真实类型的子类时发生异常
            - ConcurrentModificationException：并发修改异常，多线程修改
            - IllegalArgumentException：参数非法异常，表示方法传递了一个非法的不适合的参数
            - IllegalStateException：非法状态异常，表示方法被在不合适的时机调用
            - IndexOutOfBoundsException：下标越界异常
            - NullPointerException：空指针异常，针对空对象进行方法调用的时候触发
            - SecurityException：安全异常，由安全管理器抛出
            - UnsupportedOperationException：不支持操作异常，表示不支持指定的操作，从而抛出异常
- [正确处理异常]()
    - 如果不手动处理异常，将会由默认的异常处理器来处理异常。
- [自定义异常]()
    - 自定义受检异常：继承Exception
    - 自定义运行时异常：继承RuntimeException
    - 自定义异常需要提供以下构造器：
        - 无参构造器
        - 带有一个String参数的构造器，需传递给父类构造器
        - 带有一个Throwable参数的构造器，需传递给父类构造器
        - 带有一个String参数、一个Throwable参数的构造器，需传递给父类构造器
- **Error和Exception**
    - Error：Throwable的子类，代表的是错误，没有恢复的可能，一般是系统性错误。
    - Exception：Throwable的子类，代表的异常，存在恢复的可能，可以进行捕捉处理。
- **异常链**：在捕获异常处理的catch块中再次抛出一个异常，形成异常链，一般我们希望在异常链中保留原始异常的信息，这时就需要在抛出新异常时将原始异常作为参数来创建新的异常。
- [try-with-resources](Java_Technology/Java_Base_Technology/try-with-resources.md)
- **finally和return的执行顺序**：先执行try块或者catch块中的return，然后将结果保存起来，去执行finally中的代码，执行完后再将之前保存的返回结果返回即可，但是如果在finally块中定义了return，那么就坏菜了，程序会直接提前返回。所以，我们不能再finally块中加return。
- **异常注意事项**
子类重写父类带有throws申明异常的时候，子类只能抛出小于等于父类方法中的异常数量，而且类型必须是父类方法申明异常类型或者其子类型
### 正则表达式
- java.lang.util.regex.Pattern：规则模型
- java.lang.util.regex.Matcher：匹配器
- [JAVA正则表达式：Pattern类与Matcher类详解(转)](https://www.cnblogs.com/ggjucheng/p/3423731.html)
### IO
- IO流分类：
    - 传输格式：
        - 字符流：
            - Reader
            - Writer
        - 字节流
            - InputStream
            - OutputStream
    - 传输方向：
        - 输入流
            - InputStream
            - Reader
        - 输出流
            - OutputStream
            - Writer
- 四大概念理解：[聊聊同步、异步、阻塞与非阻塞](https://www.jianshu.com/p/aed6067eeac9)
    - 同步：调用方一直等待被调用方返回结果（等待结果，需要时刻关注被调用方是否完成）
    - 异步：调用方不等待被调用方返回结果，只要被调用方完成后主动通知调用方即可，即调用方等待的是被调用方的通知（等待通知[不等待结果-属于被动行为不需要主动触发]，不关注被调用方何时完成）
    - 阻塞：调用方等待被调用方的结果或者通知时，不做其他任何操作（干等，线程被挂起）
    - 非阻塞：调用方等待被调用方的结果或者通知时，兼职其他操作（不干等，先干点别的）
- 四大组合概念理解：
    - 同步阻塞：效率最低，等待结果，时刻关注，同时线程挂起，不执行其他内容
    - 同步非阻塞：效率较低，等待结果，时刻关注（间断性关注），线程可以执行其他任务，但需要在关注被调用者与执行其他任务之间来回切换
    - 异步阻塞：不等待、不关注被动用者，被动等待通知，线程挂起，不执行其他内容
    - 异步非阻塞：效率最高，被动等待通知，线程执行其他任务
- Linux的5种IO模型：[聊聊Linux 五种IO模型](https://www.jianshu.com/p/486b0965c296)
    - 同步阻塞 I/O（BIO）：效率最低，等待结果，时刻关注，同时线程挂起，不执行其他内容
    - 同步非阻塞 I/O（NIO）：效率较低，等待结果，时刻关注（间断性关注），线程可以执行其他任务，但需要在关注被调用者与执行其他任务之间来回切换
    - 多路复用IO：同步阻塞的一种，一个进程监听多个IO操作，只要有一个准备好数据，就执行对应的操作，如果都没有准备好，那么会阻塞执行，一直等待
    - 信号驱动I/O：不常用
    - 异步 I/O（AIO）：效率最高
- [BIO、NIO和AIO的区别、用法、原理](Java_Technology/Java_Base_Technology/BIO、NIO和AIO的区别、用法、原理.md)
    - BIO：同步阻塞IO
    - NIO：同步非阻塞IO
    - AIO：异步非阻塞IO
- Netty
### 序列化
- 什么是序列化与反序列化
    - 序列化：把对象转换为字节序列的过程
    - 反序列化：把字节序列恢复为对象的过程
- 为什么序列化
    - 为了持久化保存对象数据
    - 为了网络传递对象数据
- [序列化底层原理](https://blog.csdn.net/xlgen157387/article/details/79840134)
- 序列化与单例模式：[序列化破坏单例的解决方案](Java_Technology/Java_Base_Technology/序列化破坏单例的解决方案.md)
    - 序列化破坏单例：反序列化的时候ObjectInputStream中readObject方法中会反射调用无参构造器生成一个新的实例，这个实例不同于之前的单例，所以破坏了单例。
    - 解决方案：在单例类重定义readResolver方法，返回单例实例，那么就会忽略上面执行而是直接返回已有的单例。
- [protobuf理解](https://www.ibm.com/developerworks/cn/linux/l-cn-gpb/index.html)：一种Google使用的序列化方式
- 序列化注意事项
    - transient关键字修饰的字段不参与序列化
    - 静态变量不参与序列化
    - 子类继承自实现了Serializable接口的父类：子类父类中的属性均参与序列化
    - 子类实现了Serializable接口，父类不支持序列化：只有子类中的属性会参与序列化，父类中的被忽略，但是会调用父类的无参构造器
    - 自定义序列化：writeObject和readObject
- [为什么说序列化并不安全](https://www.jianshu.com/p/fa912ce0426f)：序列化后的数据容易被篡改，这样反序列化就会得到错误的数据，所以不安全。
- 常见的序列化方式：[几种常用序列化和反序列化方法](https://blog.csdn.net/jaryle/article/details/54893086)
    - Java原生序列化机制
    - XML序列化
    - Json序列化
        - FastJson
        - Jackson
    - ProtoBuff序列化：[Google Protocol Buffer 的使用和原理](https://www.ibm.com/developerworks/cn/linux/l-cn-gpb/index.html)
    - Thrift序列化
    - Avro序列化
### 第三方工具库
- commons.lang
- commons.*... 
- guava-libraries 
- netty
    - HashedWheelTimer：
        - [Netty工具类HashedWheelTimer源码走读(一) ](https://my.oschina.net/haogrgr/blog/489320)
        - [Netty工具类HashedWheelTimer源码走读(二)](https://my.oschina.net/haogrgr/blog/490266)
        - [Netty工具类HashedWheelTimer源码走读(三)](https://my.oschina.net/haogrgr/blog/490348)
    - 
### API&SPI
- API和SPI的关系和区别
    - API：指的是应用对服务调用方提供的接口，用于提供某种服务、功能
    - SPI：指的是应用对服务实现方提供的接口，用于实现某种服务、功能
- [SPI的使用及原理](Java_Technology/Java_Base_Technology/SPI的使用及原理.md)
- API面向的是服务调用方
- SPI面向的是服务实现方
### 编码
- Unicode
- 有了Unicode为啥还需要UTF-8
- GBK、GB2312、GB18030之间的区别
- UTF-8、UTF-16、UTF-32区别
- URL编解码、Big Endian和Little Endian
- 如何解决乱码问题
### 时间处理
- 时区
- 冬令时和夏令时
- 时间戳
- Java中时间API
- 格林威治时间
- CET,UTC,GMT,CST几种常见时间的含义和关系
- SimpleDateFormat的线程安全性问题
- Java 8中的时间处理
- 如何在东八区的计算机上获取美国时间
### 重点接口解读
- Comparator：比较器，用以实现比较方式，函数式接口，一般使用Lambda方式作为参数传递
- Comparable：可比较的，多被集合类实现，表示可以进行比较，内置的比较方式，如果存在Comparator，将会失效
- Runnable：线程任务，一般用于定义一个线程的执行内容，函数式接口，可作为Lambda使用
- Callable：回调接口，函数式接口，类似Runnable，但可以有返回值或者异常
- RandomAccess：标记接口，被标记的类拥有快速随机访问，一般是数组类集合:ArrayList
- Closeable：可被关闭，实现了该接口的资源表示其可被关闭，JDK 1.7后其继承了AutoCloseable接口，那么自动拥有AutoCloseable的功能
- AutoCloseable：自动关闭，只有实现了该接口的资源才能使用try-with-resources方式，其会在try块执行完自动调用close方法关闭资源
- Appendable：表示能够被追加 char 序列和值的对象。如果某个类的实例打算接收来自 Formatter 的格式化输出，那么该类必须实现 Appendable 接口，比如StringBuffer和StringBuilder
- Flushable：可刷新流，实现了该接口的类可以将缓存中的数据刷新到流中。一般在输出流中实现

### 源码阅读
String、Integer、Long、Enum、BigDecimal、ThreadLocal、ClassLoader & URLClassLoader、ArrayList & LinkedList、 HashMap & LinkedHashMap & TreeMap & CouncurrentHashMap、HashSet & LinkedHashSet & TreeSet

## Java高级
### 设计模式
- [设计模式的六大原则](Java_Technology/Java_Advanced_Technology/DesignPatterns/设计模式的六大原则.md)：
    - 单一职责原则（Single Responsibility Principle）：一个类只负责一个功能领域中的相应职责，或者可以定义为：就一个类而言，应该只有一个引起它变化的原因
    - 开闭原则（Open Close Principle）：一个软件实体应当对扩展开放，对修改关闭。即软件实体应尽量在不修改原有代码的情况下进行扩展
    - 里氏代换原则（Liskov Substitution Principle）：所有引用基类（父类）的地方必须能透明地使用其子类的对象
    - 依赖倒转原则（Dependence Inversion Principle）：抽象不应该依赖于细节，细节应当依赖于抽象。换言之，要针对接口编程，而不是针对实现编程
    - 接口隔离原则（Interface Segregation Principle）：使用多个专门的接口，而不使用单一的总接口，即客户端不应该依赖那些它不需要的接口
    - 迪米特法则（最少知道原则）（Demeter Principle）：一个软件实体应当尽可能少地与其他实体发生相互作用
    - 合成复用原则（Composite Reuse Principle）：尽量能使用组合就不要使用继承
- [了解23种设计模式](Java_Technology/Java_Advanced_Technology/DesignPatterns/23种设计模式.md)
    - 创建型模式：单例模式、抽象工厂模式、建造者模式、工厂模式、原型模式。
    - 结构型模式：适配器模式、桥接模式、装饰模式、组合模式、外观模式、享元模式、代理模式。
    - 行为型模式：模版方法模式、命令模式、迭代器模式、观察者模式、中介者模式、备忘录模式、解释器模式（Interpreter模式）、状态模式、策略模式、职责链模式(责任链模式)、访问者模式。
- 会使用常用设计模式
- [单例的七种写法]()：懒汉——线程不安全、懒汉——线程安全、饿汉、饿汉——变种、静态内部类、枚举、双重校验锁

工厂模式、适配器模式、策略模式、模板方法模式、观察者模式、外观模式、代理模式等必会
#### 不用synchronized和lock，实现线程安全的单例模式
#### 实现AOP
#### 实现IOC
#### NIO和reactor设计模式
### 反射技术
### 动态代理
### 并发编程
#### 并发与并行
- 并发
- 并行
- 并发与并行的区别
#### 线程
线程的实现、线程的状态、优先级、线程调度、创建线程的多种方式、守护线程

线程与进程的区别
#### 线程池
自己设计线程池、submit() 和 execute()、线程池原理

为什么不允许使用Executors创建线程池
#### 线程安全
死锁、死锁如何排查、线程安全和内存模型的关系
#### 锁
CAS、乐观锁与悲观锁、数据库相关锁机制、分布式锁、偏向锁、轻量级锁、重量级锁、monitor、

锁优化、锁消除、锁粗化、自旋锁、可重入锁、阻塞锁、死锁
#### 死锁
死锁的原因

死锁的解决办法
#### synchronized
synchronized是如何实现的？

synchronized和lock之间关系、不使用synchronized如何实现一个线程安全的单例

synchronized和原子性、可见性和有序性之间的关系
#### volatile
happens-before、内存屏障、编译器指令重排和CPU指令重排

volatile的实现原理

volatile和原子性、可见性和有序性之间的关系

有了synchronized为什么还需要volatile
#### sleep 和 wait

#### wait 和 notify

#### notify 和 notifyAll

#### ThreadLocal

#### 写一个死锁的程序

#### 写代码来解决生产者消费者问题
#### 并发包
#### 阅读源代码，并学会使用
Thread、Runnable、Callable、ReentrantLock、ReentrantReadWriteLock、Atomic*、Semaphore、CountDownLatch、、ConcurrentHashMap、Executors

### 网络编程
#### tcp、udp、http、https等常用协议
三次握手与四次关闭、流量控制和拥塞控制、OSI七层模型、tcp粘包与拆包
#### http/1.0 http/1.1 http/2之间的区别
http中 get和post区别

常见的web请求返回的状态码

404、302、301、500分别代表什么
#### http/3
#### Java RMI，Socket，HttpClient
#### cookie 与 session
#### cookie被禁用，如何实现session
#### 用Java写一个简单的静态文件的HTTP服务器

#### 了解nginx和apache服务器的特性并搭建一个对应的服务器

#### 用Java实现FTP、SMTP协议

#### 进程间通讯的方式

#### 什么是CDN？如果实现？

#### DNS？
什么是DNS 、记录类型:A记录、CNAME记录、AAAA记录等

域名解析、根域名服务器

DNS污染、DNS劫持、公共DNS：114 DNS、Google DNS、OpenDNS
#### 反向代理
正向代理、反向代理

反向代理服务器
### NIO技术
### JVM技术
#### JVM内存结构
- 运行时数据区：
    - 堆：
    - 栈：
    - 方法区（元空间）：
    - 直接内存：
    - 运行时常量池：

堆和栈区别

Java中的对象一定在堆上分配吗？(不一定，开启对象逃逸分析，之后未发生逃逸的局部对象有可能会在栈上分配)
#### 垃圾回收
GC算法：标记清除、引用计数、复制、标记压缩、分代回收、增量式回收

GC参数、对象存活的判定、垃圾收集器（CMS、G1、ZGC、Epsilon）
#### JVM参数及调优
-Xmx、-Xmn、-Xms、Xss、-XX:SurvivorRatio、

-XX:PermSize、-XX:MaxPermSize、-XX:MaxTenuringThreshold
#### Java对象模型
oop-klass、对象头
#### HotSpot
即时编译器、编译优化
#### 虚拟机性能监控与故障处理工具
jps, jstack, jmap、jstat, jconsole, jinfo, jhat, javap, btrace、TProfiler

Arthas
#### 平台无关性
Java如何实现的平台无关

JVM还支持哪些语言（Kotlin、Groovy、JRuby、Jython、Scala）
#### 字节码、class文件格式
#### 类加载机制
classLoader、类加载过程、双亲委派（破坏双亲委派）、模块化（jboss modules、osgi、jigsaw）

#### 执行引擎
#### 编译与反编译
什么是编译（前端编译、后端编译）、什么是反编译

JIT、JIT优化（逃逸分析、栈上分配、标量替换、锁优化）

编译工具：javac

反编译工具：javap 、jad 、CRF
#### Java内存模型
计算机内存模型、缓存一致性、MESI协议

可见性、原子性、顺序性、happens-before、

内存屏障、synchronized、volatile、final、锁
#### CPU缓存，L1，L2，L3和伪共享
#### 尾递归
#### 位运算
用位运算实现加、减、乘、除、取余

### 性能优化
使用单例、使用Future模式、使用线程池、选择就绪、减少上下文切换、减少锁粒度、数据压缩、结果缓存
### 新技术
#### Java 8

lambda表达式、Stream API、时间API

#### Java 9

Jigsaw、Jshell、Reactive Streams

#### Java 10

局部变量类型推断、G1的并行Full GC、ThreadLocal握手机制

#### Java 11

ZGC、Epsilon、增强var、

#### Spring 5
响应式编程

#### Spring Boot 2.0

### 语法糖
Java中语法糖原理、解语法糖

语法糖：switch 支持 String 与枚举、泛型、自动装箱与拆箱、方法变长参数、枚举、内部类、条件编译、 断言、数值字面量、for-each、try-with-resource、Lambda表达式
### 高级源码
为什么Thread里有一个ThreadLocalMap类型的变量
ThreadLocalMap为什么作为ThreadLocal的内部类
ThreadLocalMap的扩缩容机制以及碰撞检测
ThreadLocalMap的Entry为什么使用弱引用类型
有些类中的capacity,threshold,position,mark,limit这些成员变量有什么用，如何影响类内部的运算？如何设置？
### 线上问题分析
#### dump获取
线程Dump、内存Dump、gc情况
#### dump分析
分析死锁、分析内存泄露
#### dump分析及获取工具
jstack、jstat、jmap、jhat、Arthas
#### 自己编写各种outofmemory，stackoverflow程序
HeapOutOfMemory、 Young OutOfMemory、MethodArea OutOfMemory、ConstantPool OutOfMemory、DirectMemory OutOfMemory、Stack OutOfMemory Stack OverFlow
#### Arthas
Arthas是什么：是一种命令式的Java应用诊断工具。
jvm相关、class/classloader相关、monitor/watch/trace相关、options、管道、后台异步任务

文档：https://alibaba.github.io/arthas/advanced-use.html
#### 常见问题解决思路
内存溢出、线程死锁、类加载冲突
#### 使用工具尝试解决以下问题，并写下总结
当一个Java程序响应很慢时如何查找问题、

当一个Java程序频繁FullGC时如何解决问题、

如何查看垃圾回收日志、

当一个Java应用发生OutOfMemory时该如何解决、

如何判断是否出现死锁、

如何判断是否存在内存泄露

使用Arthas快速排查Spring Boot应用404/401问题

使用Arthas排查线上应用日志打满问题

利用Arthas排查Spring Boot应用NoSuchMethodError
### JMS
- [JMS(Java消息服务)入门教程](https://www.cnblogs.com/chenpi/p/5559349.html)
- **什么是Java消息服务**：两个应用程序之间进行异步通信的API，它为标准消息协议和消息服务提供了一组通用接口，包括创建、发送、读取消息等，用于支持JAVA应用程序开发。
- JMS消息传送模型
    - 点对点消息传送模型：消息一对一传送，一个发送者对应一个接受者
    - 发布/订阅消息传递模型：消息一对多传送，一个发送者对应多个接受者
### JMX
java.lang.management.*、 javax.management.*
## Java框架
### Servlet
生命周期

线程安全问题

filter和listener

web.xml中常用配置及作用

### Spring
Bean的初始化

AOP原理

实现Spring的IOC

spring四种依赖注入方式

### SpringBoot
Spring Boot 2.0、起步依赖、自动配置、

Spring Boot的starter原理，自己实现一个starter

### SpringMVC
什么是MVC

Spring mvc与Struts mvc的区别

### SpringCloud
服务发现与注册：Eureka、Zookeeper、Consul

负载均衡：Feign、Spring Cloud Loadbalance

服务配置：Spring Cloud Config

服务限流与熔断：Hystrix

服务链路追踪：Dapper

服务网关、安全、消息

### SpringSecurity
### SpringCache
### MyBatis
### Hiberate
什么是OR Mapping

Hibernate的缓存机制

Hibernate的懒加载

Hibernate/Ibatis/MyBatis之间的区别

### 测试
junit、mock、mockito、内存数据库（h2）
### 服务器
#### JBoss

#### tomcat

#### jetty

#### Weblogic
### 工具
### 版本控制工具git & svn
### 项目管理工具maven & gradle
### IDE Intellij IDEA & Eclipse
常用插件：Maven Helper 、FindBugs-IDEA、阿里巴巴代码规约检测、GsonFormat

Lombok plugin、.ignore、Mybatis plugin

## 数据库

## Nosql

## 大数据
### Zookeeper

基本概念、常见用法

### Solr，Lucene，ElasticSearch

在linux上部署solr，solrcloud，ElasticSearch，新增、删除、查询索引

### Storm，流式计算，了解Spark，S4

在linux上部署storm，用zookeeper做协调，运行storm hello world，local和remote模式运行调试storm topology。

### Hadoop，离线计算

### HDFS、MapReduce

### 分布式日志收集 flume，kafka，logstash
ELK
### 数据挖掘，mahout

## 网络安全

## 架构
### 分布式
数据一致性、服务治理、服务降级
#### 分布式事务
2PC、3PC、CAP、BASE、 可靠消息最终一致性、最大努力通知、TCC
#### Dubbo
服务注册、服务发现，服务治理

http://dubbo.apache.org/zh-cn/

#### 分布式数据库
怎样打造一个分布式数据库、什么时候需要分布式数据库、mycat、otter、HBase
#### 分布式文件系统
mfs、fastdfs
#### 分布式缓存
缓存一致性、缓存命中率、缓存冗余
#### 限流降级
Hystrix、Sentinal
#### 算法
共识算法、Raft协议、Paxos 算法与 Raft 算法、拜占庭问题与算法

2PC、3PC
### 微服务
SOA、康威定律
#### ServiceMesh
sidecar
#### Docker & Kubernets
#### Spring Boot
#### Spring Cloud
### 高并发
#### 分库分表
#### CDN技术
#### 消息队列
ActiveMQ

### 监控
#### 监控什么
CPU、内存、磁盘I/O、网络I/O等
#### 监控手段
进程监控、语义监控、机器资源监控、数据波动
#### 监控数据采集
日志、埋点
#### Dapper
### 负载均衡
tomcat负载均衡、Nginx负载均衡

四层负载均衡、七层负载均衡
### DNS
DNS原理、DNS的设计
### CDN
数据一致性
## 扩展