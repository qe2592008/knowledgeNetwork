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
- 面向对象和面向过程的区别：
    - **面向对象**：将一类事物抽象成类，将事物的属性抽象成属性，事物的行为抽象成方法，然后将其封装起来的编程思想。重点关注的是对象。
    - **面向过程**：重点关注的是执行步骤，利用函数将每个步骤实现逐个调用的方式。
- 面向对象的三大基本特征和五大基本原则
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
重点：传递关注的是传递的内容本身，而不是其所代表的含义或者指向的内容。
- 值传递：
- 引用传递：
- [为什么说Java中只有值传递](https://www.cnblogs.com/wchxj/p/8729503.html)：如果某个方法的参数是一个对象，那么传递的时候就会直接传递这个对象在栈空间的句柄，那么这种是不是引用传递呢，不是，因为引用是不会再内存中保存的，而这里确实保存着，可以看成是地址传递，因为这个这个句柄保存着的就是目标对象的地址。
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
    - 接口
        - interface定义
        - 不能定义字段
        - 没有构造器
        - 方法默认public abstract
        - 可以定义静态方法、默认方法、重写Object的方法
        - 实现类必须实现其所有抽象方法
        - 接口的继承是多继承
    - 抽象类
        - abstract class定义
        - 拥有构造器，但是不能主动创建实例，主要被子类调用
        - 可以定义抽象方法，让子类去实现，也可以定义普通的方法
        - 可以定义main方法，并且可以运行
        - 其它基本和普通的类没有区别
        - 抽象类的继承是单继承，多实现
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
    - **LinkedHashMap**：基于Hash和链表（循环双向链表）实现的键值对集合，保存了插入顺序。其实就是对HashMap的所有元素使用一个链表连起来罢了。视为一个有序的HashMap。有两种排序方式：
        - 插入顺序，默认为插入顺序，accessOrder=false：按照元素存入map中的顺序排序
        - 访问顺序，accessOrder=true：按照访问Map元素的顺序排序
        - 注意：以上两个排序其实都是在双向链表中实现了，这个链表和HashMap其实是并列存在的。在两个里面均保存了元素的引用。
    - **LinkedHashSet**：同上，视为有序的HashSet，它只支持按照元素的插入顺序排序。
        - 其实LinkedHashSet底层是基于LinkedHashMap实现的，
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
        - K：键值对中的键key
        - V：键值对中的值value
        - T：
        - E：
        - R:
        - ?：不限定类型
        - Object：任意类型
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
> 同步异步说的是等不等待的问题，阻塞不阻塞说的是线程是被挂起还是干点别的的事情；即使我不等待，我也可以闲着不干别的事情（异步阻塞），也可以等待，但不妨碍我期间干点别的，只要我定时返回来看看结束类就是了（同步非阻塞）
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
- Unicode编码（统一编码）：对世界上所有的字符进行了编码与标识，包括两部分，基本字符集和增补字符集
    - 基本字符集：U+0000-U+FFFF
    - 增补字符集：U+10000-U+10FFFF
- 有了Unicode为啥还需要UTF-8：因为Unicode仅仅是对所有的字符进行了编号，却并没有定义如何进行字符的二进制表示，为此专门设计了UTF-*系列二进制映射法则。
- GBK、GB2312、GB18030之间的区别
    - GB2312：最早的汉字编码，采用两个字节共16位来编码，两个字节的最高位均固定为1，剩余14位进行汉字编码，共收录7000余最常用的汉字
    - GBK：GB2312扩展而来，还是两个字节，只是放开了第二个字节首位的1限制，只有第一字节首位固定为1，新增14000余汉字，包括了繁体字，共有21000余字
    - GB18030：GBK扩展而来，采用变长编码，两个字节的就是GBK部分，新增部分全部采用四个字节编码，新增了55000余字符，总量达到了71000多字符
    - BIG5：繁体字编码，用于台湾、香港地区，2个字节编码
- UTF-8、UTF-16、UTF-32区别：都是针对Unicode编码的二进制编码映射
    - UTF-32：4个字节编码，与Unicode编号长度一致，不需要转换即可直接使用。有两种表示方式，前高后低为大端（BE）,反之为小端（LE）,较浪费空间，所以有了UTF-16和UTF-8
    - UTF-16：变长方式表示字符，基本字符采用2个字节表示，增补字符采用4个字节表示，需要经过一个转换算法来将Unicode的四字节编号转换为UTF-16的四字节（二字节）表示形式
    - UTF-8：变长方式表示字符，UTF-8兼容ASCII。
        - Unicode编号范围0X00-0X7F（0-127）：采用一个字节表示，0xxxxxxx（高位固定位0，可表示128个字符），对应ASCII
        - Unicode编号范围0X80-0X7FF（128-2047）：2个字节表示，110xxxxx 10xxxxxx（首字节高位固定110，末字节高位固定10，剩余位可表示最多2048个字符）
        - Unicode编号范围0X800-0XFFFF（2048-65535）：3个字节表示，1110xxxx 10xxxxxx 10xxxxxx（首字节高位固定1110，其余字节首位固定10，剩余16位可表示65536个字符），对应汉字编码
        - Unicode编号范围0X10000-0X10FFFF（65536-1114111）：4个字节表示，11110xxx 10xxxxxx 10xxxxxx 10xxxxxx（首字节高位固定11110，其余字节首位固定10，剩余21位可表示2097152个字符），对应增补字符
- **URL编解码**
- Big Endian和Little Endian
- 如何解决乱码问题:反向去解码，一般出现乱码的原因就是解码方式出错导致的，而且可能经过多重错误编码和解码，要获取源码，需要反向编码和解码，只需要知道你使用的错误的编码类型，如果类型未知，则较难实现数据复原。
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
- [String源码解读]()
- [Integer源码解读]()
- [Long源码解读]()
- [Enum源码解读]()
- [BigDecimal源码解读]()
- [ArrayList源码解读]()
- [LinkedList源码解读]()
- [HashMap源码解读]()
- [LinkedHashMap源码解读]()
- [TreeMap源码解读]()
- [HashSet源码解读]()
- [LinkedHashSet源码解读]()
- [TreeSet源码解读]()
- ThreadLocal源码解读
- ClassLoader源码解读
- URLClassLoader源码解读

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
    - 创建型模式：
        - 工厂模式：使用工厂接口统筹所有工厂类，新增功能后，同时新增新的工厂类，避免修改原有工厂类，针对的是一个目标类
        - 抽象工厂模式：针对的是一系列目标类，这一系列属于同一个工厂，其余与工程模式相似
        - 单例模式：通过编程实现只有一个实例，多种实现方式：懒汉-饿汉-静态内部类-枚举-双重校验
        - 建造者模式：
        - 原型模式：
    - 结构型模式：
        - 适配器模式：涉及双方，主要用于将无关的双方连接起来，被调用的方法是固定的，发起调用的方法是抽象的
            - 类适配器：定义的适配器实现发起调用的接口，继承被调用的类，如此一来，在这个适配器中同时拥有了双方，然后重写发起调用的方法，在其中调用父类的目标方法即可
            - 对象适配器：定义的适配器实现发起调用的接口，持有被调用的类的实例，如此一来，在这个适配器中同时拥有了双方，然后重写发起调用的方法，在其中通过持有的实例调用目标方法即可
            - 接口适配器：屏蔽多余实现
        - 装饰模式：针对目标进行增强，通过实现相同的接口来在装饰类中持有目标的实例，重写接口方法调用实例的目标方法，在此之前之后即可进行增强，主要是那个持有的实例是由调用方创建并传入的
        - 代理模式：针对目标进行全权代理，通过实现相同的接口来在代理类中持有目标的实例，重写接口方法调用实例的目标方法，在此之前和之后还可以进行一些增强，主要是那个持有的实例时由代理类自己创建的
        - 外观模式：主要用于对外屏蔽复杂的模块调用，将模块调用整合到一个外观类中，统一对外提供服务
        - 桥接模式：涉及双方，用于解耦双方，使双方均能实现自由扩展。创建桥接口被调方实现桥接口，主调方定义抽象类，持有桥实例，这样一来，被调方通过实现桥接口来进行扩展，主调方通过继承抽象类来进行扩展，互不影响。
        - 组合模式：针对特定的树形接口而设的模式
        - 享元模式：池技术基础
    - 行为型模式：
        - 策略模式：策略模式用于实现完成一个功能的多种方式（成为策略），定义一个顶层策略接口，定义抽象的功能方法，由实现类来实现功能的不同实现。其实就是一个简单的一接口多实现类的模式。有时候可能会加上一个辅助工具。
        - 模版方法模式：借助抽象类的抽象方法来实现模板功能，将一段代码中需要子类实现的模块抽象出来成一个抽象方法，交给子类来实现，这个方法最好protected修饰
        - 观察者模式：订阅功能，包括观察者的注册，事件发生的通知两个重点。主要就是实现观察者方和被观察者方。观察者方需要有一个被通知方，被观察者需要持有一个观察者列表，添加、删除观察者的方法，通知观察者的方法
        - 迭代器模式：
        - 职责链模式(责任链模式)：
        - 命令模式：包括三方，命令的发出方和接收方，在加上命令方。为了实现三者的解耦，现在讲命令抽象成抽象类，发送方和接收方都是固定的类，那么可在发送方持有命令接口，命令中持有接收方，这样一来就可以实现解耦，命令可以自有扩展，有新命令直接新建一个命令子类即可
        - 备忘录模式：主要就是操作目标实例的时候将实例的原始状态值保存起来，操作完成之后还可以通过备忘系统恢复。这需要一个备忘系统，也可以叫临时存储系统，备忘录系统中需要持有一个临时存储实例，来保存原始状态。
        - 状态模式：
        - 访问者模式：
        - 中介者模式：
        - 解释器模式（Interpreter模式）：
- 会使用常用设计模式
- [单例的七种写法](Java_Technology/Java_Advanced_Technology/DesignPatterns/单例的七种写法.md)：相似点：构造器私有化，大部分都需要有静态私有的类成员（单例），公共的获取类成员的静态方法
    - 懒汉——线程不安全：线程不安全，就不要出来显了
    - 懒汉——线程安全：不安全写法的方法上加锁，线程安全了，算是一个单例实现方式了
    - 饿汉：相对懒汉式而言，丢弃了懒加载，依靠类加载器保证线程安全。
    - 饿汉——变种：所谓变种其实只是换了个写法，单例的创建位置稍变，基本与上一种一样
    - 静态内部类：这种不错，内部类只有在调用的使用才会加载，实现了懒加载，又依靠类加载器实现了线程安全性
    - 枚举：绝妙的注意
    - 双重校验锁：这个是复杂的方式，需要JDK1.5以后才能保证线程安全性。
- 适配器模式和桥接模式：二者均涉及双方
    - 适配器模式：主要用于将无关联的双方关联起来，通过新增一个类来关联，由于Java只支持但继承，而被调用方又是具体的类，那么只能继承被调方（继承），然后实现主调方；或者实现主调方，持有被调方实例（组合）
    - 桥接模式：主要用于将强关联的双方解耦，
> 工厂模式、适配器模式、策略模式、模板方法模式、观察者模式、外观模式、代理模式等必会

> 关联方式有两种，组合和继承（实现）,继承可以持有对象，实现不能

> 总结：使用抽象类可以提升抽象化层次，当然接口是可以的，但是很多情况下，已经不能定义接口了，比如目标要继承一个抽象类，这时候要抽象层次的只能是抽象类，
> 在没有任何限制的情况下，优先使用接口来进行抽象解耦，如果有限制，比如需要持有目标实例，那么就退而求其次使用抽象类来进行抽象解耦
- 不用synchronized和lock，实现线程安全的单例模式：静态内部类方式、枚举方式、饿汉式
- **实现AOP**：需要使用到代理模式和反射
- **实现IOC**：用到了多种设计模式：？？
- NIO和reactor设计模式
    处理一个或多个客户端并发请求服务的事件设计模式，当请求抵达后，服务处理程序使用I/O多路复用策略，然后同步地派发这些请求至相关的请求处理程序。
### 反射技术
- Java反射技术：反射是Java语言的一个特性，它允许程序在运行时（注意不是编译的时候）来进行自我检查并且对内部的成员进行操作。
- 获取Class的三种方式：
    - `Class class = "".getClass();`
    - `Class class = String.class;`
    - `Class class = Class.forName("java.lang.String");`
- **@CallerSensitive**：这个注解是为了堵住漏洞用的。曾经有黑客通过构造双重反射来提升权限，原理是当时反射只检查固定深度的调用者的类，看它有没有特权，例如固定看两层的调用者（getCallerClass(2)）。如果我的类本来没足够权限群访问某些信息，那我就可以通过双重反射去达到目的：反射相关的类是有很高权限的，而在 我->反射1->反射2 这样的调用链上，反射2检查权限时看到的是反射1的类，这就被欺骗了，导致安全漏洞。使用CallerSensitive后，getCallerClass不再用固定深度去寻找actual caller（“我”），而是把所有跟反射相关的接口方法都标注上CallerSensitive，搜索时凡看到该注解都直接跳过，这样就有效解决了前面举例的问题。
- 反射与工厂模式：
    - [IOC的实现原理—反射与工厂模式](https://blog.csdn.net/fuzhongmin05/article/details/61614873/)
- **反射的作用**：可以在运行时动态操作类和对象，可以创建对象，执行方法，解析注解等。
- 反射机制的优缺点：
    - 优点：可以实现动态创建对象和编译，体现出很大的灵活性
    - 缺点：对性能有影响使用反射基本上是一种解释操作，我们可以告诉JVM，我们希望做什么并且让它满足我们的要求。这类操作总是慢于直接执行相同的操作。
- 为何使用反射：
    - 静态编译：在编译时确定类型，绑定对象，即通过。
    - 动态编译：运行时确定类型，绑定对象。动态编译最大限度发挥了Java的灵活性，体现了多态的应用，有效降低类之间的耦合性。
- Class类：Class类可以算是反射的基础了，也是反射的开始，一切的原始就是先要获取到目标的Class对象，然后依此来展开一些列反射操作。
- `java.lang.reflect.*`包：这个包中都是反射使用的类
### 动态代理
- 静态代理：手动创建代理类，需要与目标类实现同一接口，当目标类较多时，需要逐一手动创建，费事
- 动态代理：通过反射来在运行时动态创建代理类
- [动态代理和反射的关系](http://blog.sina.com.cn/s/blog_548c8a8301013j6u.html)：动态代理利用反射实现的
- 动态代理的几种实现方式
    - JDK原生动态代理：基于接口实现，通过创建代理类实现
    - CGLIB动态代理：基于类实现，通过继承创建代理子类实现
- AOP：Spring中的AOP实现原理就是动态代理，同时支持JDK动态代理和CGLIB动态代理
### 并发编程
#### 并发与并行
- 并发：指的是多个任务线程一起执行，但需要抢占CPU时间片，同一时刻只能有一个任务线程在执行，可发生在单核和多核环境
- 并行：指的是多个任务线程一起执行，齐头并进，一般是指在多核CPU环境下，多个线程在不同的CPU下执行的情况
- 并发与并行的区别：同上
#### 线程
- 线程的实现
- 线程的状态
- 线程优先级
- 线程调度
- 创建线程的多种方式
- 守护线程
- 线程与进程的区别
    - 进程：
    - 线程：
#### 线程池
自己设计线程池
submit() 和 execute()
线程池原理
为什么不允许使用Executors创建线程池：因为使用Execcutors返回的线程池都是JDK原生提供的线程池，有四种:FixedThreadPool、SingleThreadPool、CachedThreadPool、ScheduledThreadPool。前两种所使用的阻塞队列是LinkedBlockingQueue，其队列长度为Integer.MAX_VALUE，易造成线程堆积，导致OOM，后两种定义的核心线程数量为Integer.MAX_VALUE，易创建大量线程造成OOM。
#### 线程安全
- 线程安全和内存模型的关系
#### 锁
- CAS
- 乐观锁与悲观锁
- 数据库相关锁机制
- 分布式锁
    - Redis分布式锁
    - Zokeeper分布式锁
- 偏向锁
- 轻量级锁
- 重量级锁
- monitor
- 锁优化
- 锁消除
- 锁粗化
- 自旋锁
- 可重入锁
- 阻塞锁
- 死锁
#### 死锁
死锁的原因
死锁如何排查
死锁的解决办法
#### synchronized
- synchronized是实现原理：synchronized关键字通过编译之后，会在同步块的前后分别形成monitorenter和monitorexit这两个字节码指令，
- synchronized和lock之间区别
- 不使用synchronized如何实现一个线程安全的单例：使用饿汉式、枚举、静态内部类方式实现
- synchronized和原子性、可见性和有序性之间的关系：synchronized可以同时保证操作的原子性，可见性和有序性
    - 原子性
    - 可见性
    - 有序性
#### volatile
- happens-before
- 内存屏障
- 编译器指令重排和CPU指令重排
- volatile的实现原理
 -volatile和原子性、可见性和有序性之间的关系
- 有了synchronized为什么还需要volatile：volatile是一种轻量级的锁，针对确定原子操作的变量可以实现线程安全，不需要加上繁重的synchronized

#### sleep 和 wait

#### wait 和 notify

#### notify 和 notifyAll
#### join操作，三个任务，如何多线程顺序执行
#### Fork/Join框架，分而治之
#### ThreadLocal

#### 写一个死锁的程序

#### 写代码来解决生产者消费者问题
#### 并发包
#### 阅读源代码，并学会使用
- [Thread源码解读]()
- [Runnable源码解读]()
- [Callable源码解读]()
- [ReentrantLock源码解读]()
- [ReentrantReadWriteLock源码解读]()
- [Atomic*源码解读]()
- [Semaphore源码解读]()
- [CountDownLatch源码解读]()
- [ConcurrentHashMap源码解读]()
- [Executors源码解读]()

### 网络编程
#### tcp、udp、http、https等常用协议
- TCP协议：可靠的传输控制协议
- UDP协议：不可靠的数据报传输协议
- HTTP协议：
- HTTPS协议：
- 三次握手与四次关闭
- 流量控制和拥塞控制
- OSI七层模型
    - 应用层
    - 表示层
    - 会话层
    - 传输层
    - 网络层
    - 数据链路层
    - 物理层
- TCP/IP四层模型/五层模型
    - 应用层
    - 传输层
    - 网络层
    - 数据链路层
    - 物理层
- tcp粘包与拆包
#### http/1.0 http/1.1 http/2之间的区别
http中 get和post区别

常见的web请求返回的状态码

404、302、301、500分别代表什么
#### http/3
#### Java RMI，Socket，HttpClient
- Java RMI
- Socket
- HttpClient
#### cookie 与 session
- cookie
- session
- cookie被禁用，如何实现session
#### 用Java写一个简单的静态文件的HTTP服务器

#### 了解nginx和apache服务器的特性并搭建一个对应的服务器

#### 用Java实现FTP、SMTP协议

#### 进程间通讯的方式

#### 什么是CDN？如果实现？

#### DNS？
- 什么是DNS：DNS是域名解析系统，主要用于将域名解析为IP地址
- 记录类型:A记录、CNAME记录、AAAA记录等
- 域名解析
- 根域名服务器
- DNS污染：网域服务器缓存污染或者域名服务器缓存投毒，
- DNS劫持
- 公共DNS：114 DNS、Google DNS、OpenDNS
#### 反向代理
- 正向代理
- 反向代理
- 反向代理服务器
#### 浏览器与服务器通讯过程
### NIO技术
### JVM技术
#### JVM内存结构
- 运行时数据区：
    - 程序计数器：
    - 栈：
        - Java虚拟机栈
        - 本地方法栈
    - 堆：
        - 新生代
            - Eden区
            - From Survivor区
            - To Survivor区
        - 老年代
    - 方法区（元空间）：
    - 运行时常量池：区别于Class文件常量池，后者位于Class文件中，当Class文件被虚拟机加载之后，其中的常量池部分就会进入到运行时常量池保存
    - 直接内存：
- 堆和栈区别
- Java中的对象一定在堆上分配吗？(不一定，开启对象逃逸分析，之后未发生逃逸的局部对象有可能会在栈上分配)
- 常量池：
    - Class文件常量池：存在于class文件中
    - 运行时常量池：存在于方法区中，1.7以后挪到了元空间
    - 字符串常量池：存在于方法区中，1.7以后挪到了堆中
#### 垃圾回收
- GC算法：
    - 标记清除：先标记，再清除。效率低、有空间碎片
    - 复制：先复制，再清除。空间利用率极低（50%）
    - 标记整理：先标记，再整理。
    - 分代回收：将堆划分为新生代、老年代，各区域选择适合的回收算法。
        - 新生代-复制
        - 老年代-标记清除或者标记整理
    - 增量式回收：
- GC参数
- 对象存活的判定
    - 判定方法：
        - 引用计数
        - 可达性分析
    - 引用类型
        - 强引用：可达性分析是否回收
        - 软引用：内存不足标记为可回收
        - 弱引用：一定会被垃圾回收，只能活在两次垃圾回收期间
        - 虚引用：无影响
- 垃圾收集器（CMS、G1、ZGC、Epsilon）
    - serial：新生代收集器，单线程，运行于client模式的默认新生代收集器
    - parnew：新生代收集器，serial的多线程版，server模式中配合CMS使用（重点）
    - parallel scavenge：新生代收集器，复制算法，多线程并行收集器，吞吐量控制，自适应调节策略，jdk1.6之前与serial old配合使用，之后与parallel old配合使用
    - serial old：serial的老年代版本收集器，标记整理算法，单线程，运行于client模式的默认老年代收集器，server模式与parallel scavenge配合使用，或者作为CMS的后备收集器
    - parallel old：parallel scavenge的老年代版本收集器，标记整理算法，多线程，与parallel scavenge配合使用与server模式中
    - CMS：老年代收集器，标记清除算法
        - 步骤：
            - 初始标记：需要stop the world，时间极短，仅标记GCRoot能直接关联的对象
            - 并发标记：与用户线程一起进行，执行GC Root Tracing
            - 重新标记：需要stop the world，时间较短，主要用于修正并发标记期间因用户程序继续运作而导致标记变动的那一部分对象的标记记录
            - 并发清除：与用户线程一起进行，执行清除操作
        - 使用：server模式下与parnew配合使用，并使用serialOld作为后备收集器
        - 优点：
            - 并发收集
            - 低停顿
        - 缺点：
            - 对CPU资源敏感
            - 无法处理浮动垃圾：默认老年代使用92%的情况下就会激活CMS
            - 会产生空间碎片
    - G1：CMS的继任者
        - 步骤：
            - 初始标记
            - 并发标记
            - 最终标记
            - 筛选回收
        - 优点：
            - 并行与并发：
            - 分代收集：内部包含了新生代和老年代的所有收集功能，无需与其他收集器配合使用
            - 空间整合：整体看采用标记整理算法，局部看是复制算法，不会产生空间碎片
            - 可预测停顿：
    - ZGC：
    - Epsilon：
- GC：
    - Minor GC：新生代GC，较频繁，速度快
        - 当年轻代内存满时，会引发一次普通GC，该GC仅回收年轻代。需要强调的时，年轻代满是指Eden代满，Survivor满不会引发GC
    - Full GC/Major GC：老年代GC，一般伴随一次到多次Minor GC，速度慢10倍以上
        - 当年老代满时会引发Full GC，Full GC将会同时回收年轻代、年老代
        - 当永久代满时也会引发Full GC，会导致Class、Method元信息的卸载
- 内存分配回收策略
    - 对象优先分配在Eden区：Eden区空间不足触发Minor GC
    - 大对象直接进入老年代：通过-XX:PretenureSizeThreshold参数设置对象大小，大于这个值的对象直接放到老年代，该参数只在Serial和pranew中有效
    - 长期存活的对象进入老年代：对象在新生代中被复制一次年龄加1，即熬过一次Minor GC。当年龄达到15岁（默认为15，可由参数-XX:MaxTenuringThreshold设置）将会被晋升到老年代。
    - 动态的对象年龄判断：如果Survivor中相同年龄的所有对象大小的总和大于Survivor空间的一半，则年龄大于等于该年龄的对象全部晋升老年代
    - 空间分配担保：发生Minor GC之前，先检查老年代最大可用连续空间是否大于新生代所有对象总空间，若大于则校验HandlePromotionFailure参数是否允许担保失败，若允许则再检查老年代最大可用连续空间是否历次晋升老年代对象的而平均大小，若大于则执行Minor GC，否则，或者不允许担保失败，则执行一次Full GC。
- 系统崩溃前的一些现象：
    - 每次垃圾回收的时间越来越长，由之前的10ms延长到50ms左右，FullGC的时间也有之前的0.5s延长到4、5s
    - FullGC的次数越来越多，最频繁时隔不到1分钟就进行一次FullGC
    - 年老代的内存越来越大并且每次FullGC后年老代没有内存被释放
    - 之后系统会无法响应新的请求，逐渐到达OutOfMemoryError的临界值。
#### JVM参数及调优
- -Xmx：堆容量最大值
- -Xmn：新生代容量，所以老年代容量 = 堆容量 - 新生代容量 
- -Xms：堆容量初始值
- -Xss：线程堆栈空间大小
- -XX:MaxDirectMemorySize:Direct Buffer Memory大小
- -XX:SurvivorRatio：Eden区与Survivor区的大小比值
- -XX:PermSize：永久代初始大小
- -XX:MaxPermSize：永久代最大值
- -XX:MaxTenuringThreshold：设置对象进入老年代的经历的Minor GC次数
- -XX:PretenureSizeThreshold：设置大于设定值的对象直接放到老年代
- -XX:CMSInitiatingOccupancyFraction=80:老年代使用80％后开始CMS收集
#### Java对象模型
oop-klass、对象头
#### HotSpot
- 对象
    - 创建：new指令->定位类的符号引用->类加载->分配内存->初始化0值->设置对象头->执行<init>初始化
    - 内存布局：对象头、实例数据、对齐填充
        - 对象头：Mark word、类型指针
            - Mark word：
            - 类型指针：指向对应的类元数据的指针，可以通过它确定对象的类型
        - 实例数据：主要是字段内容，包括继承自父类的字段
        - 对齐填充：占位符，用于补齐对象的实例数据部分
    - 访问定位：
        - 句柄：需要在堆中建立句柄池，用于存储对象类型数据和实例数据的指针，栈中保存句柄地址。
        - 直接指针：栈中直接保存对象实例数据地址，其中在对象头中保存类型指针，指向对象类型数据。HotSpot采用直接指针
- 即时编译器
- 编译优化
#### 虚拟机性能监控与故障处理工具
- jps：虚拟机进程状况工具（JVM Process Status Tool），用于罗列正在运行的虚拟机进程
    - -l：输出主类全名
    - -v：输出JVM启动参数
- jstack：Java堆栈跟踪工具（Stack Trace for Java），用于生成虚拟机当前线程快照
- jmap：Java内存映像工具（Memory Map for Java）
    - -dump：用于生成堆转储快照，即dump文件
    - -finalizerinfo：查看F-QUEUE中对象
    - -heap：显示Java堆信息
    - -histo：显示堆中对象的信息
    - -F：强制生成dump快照文件
- jstat：监视JVM进程的工具（JVM Statistics Monitoring Tool），可以显示本地或远程的虚拟机进程的类装载、内存、垃圾回收、JIT编译等运行数据
    - -gc：显示Java堆状况
    - -compiler：显示JIT编译器编译过的方法，耗时信息
    - -gcnew：监控新生代
    - -gcold：监控老年代
    - -class：监控类装载、卸载数量、总空间以及耗时
    - interval count：查询间隔和次数，位于命令末尾
- jconsole：Java监视与管理控制台（Java Monitoring and Management Console）是基于JMX的可视化监控工具。
- jinfo：Java配置信息工具（Configuration Info for Java），实时查看和调整Java虚拟机的各项参数
    - pid：线程ID，位于末尾，表示要查询的线程的Id
- jhat：虚拟机堆转储快照分析工具（JVM heap Analysis Tool），与jmap搭配使用
- javap：反编译工具，可以获取到可读性好的字节码文件
- btrac
- TProfiler
- Arthas
#### 平台无关性
- Java如何实现的平台无关：通过class字节码文件和JVM配合来实现的，首先使用JVM来屏蔽各种操作系统平台的不统一，统一对上层提供一致的入口。然后我们的Java程序会先被编译成class字节码然后被JVM加载执行。
- JVM还支持哪些语言（Kotlin、Groovy、JRuby、Jython、Scala）
- JVM的语言无关性，只要能编译成为同一个class字节码格式文件，无论你之前是什么语言编写的都没有关系，JVM只关心结果是它能处理的文件即可，来源无所谓。
#### 字节码、class文件格式

#### 类加载机制
- classLoader类加载器
- [类加载过程]()
- 类加载过程简要记忆：加载链接初始化，验证准备和解析
- 双亲委派模型（破坏双亲委派）
- 模块化（jboss modules、osgi、jigsaw）

#### 执行引擎

#### 编译与反编译
- 什么是编译（前端编译、后端编译）
- 什么是反编译
- JIT
- JIT优化（逃逸分析、栈上分配、标量替换、锁优化）
- 编译工具：javac
- 反编译工具：
    - javap
    - jad
    - CRF
#### Java内存模型
- 计算机内存模型
- 缓存一致性
- MESI协议
- 三大特性：
    - 可见性
    - 原子性
    - 顺序性
- happens-before
- 内存屏障
- synchronized
- volatile
- final
- 锁
#### CPU缓存，L1，L2，L3和伪共享
#### 尾递归
#### 位运算
用位运算实现加、减、乘、除、取余
#### 线程
- 线程模型
    - 内核线程实现：轻量级进程和内核线程一对一线程模型，需要内核态与用户态的频繁切换，较耗资源，Java采用的就是这种模型
    - 用户线程实现：进程和用户线程一对多的线程模型，完全由程序来控制线程的生命周期与CPU映射，一般依赖于线程库来完成
    - 用户线程+轻量级进程混合实现：用户线程与轻量级进程多对多的线程模型，由轻量级进行来作为用户线程与内核线程之前的桥梁
- 线程调度：系统为线程分配CPU使用权
    - 协同式线程调度：由线程来管理自己的执行时间
    - 抢占式线程调度：有系统来统一调配线程的执行时间，Java采用抢占式线程调度
- 状态转换
    - NEW：新建，创建后尚未启动的线程
    - RUNNABLE：可运行，包括两种子状态
        - READY：等待执行，等待CPU为它分配时间段
        - RUNNING：正在执行
    - WAITING：等待，被一些方法设置后处于等待中，可被唤醒
    - TIMED WAITING：限时等待，被一些方法设置后处于等待中，可被唤醒，或者时限到了自动苏醒
    - BLOCKED：阻塞，抢锁失败之后，线程被挂起，阻塞，当锁被释放后重新发起抢占
    - TERMINATED：终结，线程执行完毕
- 线程状态转换图

![线程状态转换](Images/线程状态转换.png)
### 性能优化
使用单例、使用Future模式、使用线程池、选择就绪、减少上下文切换、减少锁粒度、数据压缩、结果缓存
### 新技术
#### Java 8

lambda表达式、Stream API、时间API

#### Java 9
- modularity System 模块系统,Jigsaw
- HTTP/2
- JShell
- 不可变集合工厂方法
- 私有接口方法
- HTML5风格的Java帮助文档
- 多版本兼容 JAR
- 统一 JVM 日志
- java9的垃圾收集机制，默认G1
- I/O 流新特性
- Reactive Streams

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
[JVM性能调优](https://www.cnblogs.com/csniper/p/5592593.html)
[Java系列笔记(4) - JVM监控与调优](http://www.cnblogs.com/zhguang/p/Java-JVM-GC.html)
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
- 生命周期
- 线程安全问题
- filter和listener
- web.xml中常用配置及作用

### Spring
- Bean的初始化
- AOP原理
- 实现Spring的IOC
- spring四种依赖注入方式
### SpringBoot
- Spring Boot 2.0
- 起步依赖
- 自动配置
- Spring Boot的starter原理
- 自己实现一个starter
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
- 什么是ORMapping
- Hibernate的缓存机制
- Hibernate的懒加载
- Hibernate/Ibatis/MyBatis之间的区别
    - Hibernate
    - Ibatis
    - MyBatis
### 测试
- junit
- mock
- mockito
- 内存数据库（h2）
### 服务器
#### JBoss

#### tomcat

#### jetty

#### Weblogic
### 工具
#### 版本控制工具git & svn
#### 项目管理工具maven & gradle
#### IDE Intellij IDEA & Eclipse
常用插件：Maven Helper 、FindBugs-IDEA、阿里巴巴代码规约检测、GsonFormat

Lombok plugin、.ignore、Mybatis plugin

## 数据库

## Nosql

## 大数据
### Zookeeper
- 基本概念
- 常见用法
- 特点
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
- 怎样打造一个分布式数据库
- 什么时候需要分布式数据库
- mycat
    - 概念：从定义和分类来看，它是一个开源的分布式数据库系统，是一个实现了 MySQL 协议的的Server，前端用户可以把它看作是一个数据库代理，用 MySQL 客户端工具和命令行访问，而其后端可以用MySQL 原生（Native）协议与多个 MySQL 服务器通信，也可以用 JDBC 协议与大多数主流数据库服务器通信，核心功能是分表分库，即将一个大表水平分割为 N 个小表，存储在后端 MySQL 服务器里或者其他数据库里。
    - [Mycat使用](https://github.com/MyCATApache/Mycat-Server/wiki)
    - [mycat 从入门到放弃](https://www.cnblogs.com/bingosblog/p/7171501.html)
    - 分布式事务：Mycat并没有根据二阶段提交协议实现 XA事务，而是只保证 prepare 阶段数据一致性的 弱XA事务
- otter
    - 概念：基于数据库增量日志解析，准实时同步到本机房或异地机房的mysql/oracle数据库. 一个分布式数据库同步系统
    - [otter介绍](https://github.com/alibaba/otter/wiki/Introduction)
- HBase：
    - 概念：HBase是建立在Hadoop文件系统之上的分布式面向列的数据库。HBase是一个数据模型，类似于谷歌的大表设计，可以提供快速随机访问海量结构化数据。它利用了Hadoop的文件系统（HDFS）提供的容错能力。
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
### AR & VR
- VR：虚拟现实技术
- AR：增强现实技术