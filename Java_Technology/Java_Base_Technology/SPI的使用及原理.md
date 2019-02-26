# SPI的使用及原理
## SPI的使用
### 第一步：创建服务接口
```java
package com.dh.spi;

public interface Fruit {
    String getName();
}
```
### 第二步：创建多个服务实现
```java
package com.dh.spi;

public class Apple implements Fruit {
    @Override
    public String getName() {
        return "apple";
    }
}
```
```java
package com.dh.spi;

public class Banana implements Fruit {
    @Override
    public String getName() {
        return "Banana";
    }
}
```
这里的两个服务实现类，针对的是两个服务是现方，一方实现了Apple，另一方实现了Banana。
### 第三步：创建配置文件
在resource下创建/META-INF/services目录，在services目录下创建以服务接口全限定名为名称的文件：com.dh.spi.Fruit

文件内容为，当前服务实现的服务实现者类的全限定名
```text
com.dh.spi.Apple
```
### 第四步：创建测试类
```java
public class Test {
    public static void main(String[] args) {
        ServiceLoader<Fruit> s = ServiceLoader.load(Fruit.class);
        Iterator<Fruit> it = s.iterator();
        while(it.hasNext())
            System.out.println(it.next().getName());
    }
}
```
执行结果为：
```text
apple
```
## SPI的实现原理
SPI的实现主要依靠的就是ServiceLoader类。使用该类加载接口类型（例如：Fruit.class）
```text
ServiceLoader<Fruit> s = ServiceLoader.load(Fruit.class);
```
虽然是一个load方法，但是并没有加载到指定的服务实现类，这里仅仅是对加载服务实现类做一些准备工作：
- 创建ServiceLoader
- 为service赋值
- 为loader赋值
- 为acc赋值
- 清空providers缓存
- 为lookupIterator赋值，其实就是创建一个LazyIterator延迟迭代器。

然后创建迭代器：
```text
Iterator<Fruit> it = s.iterator();
```
iterator方法中采用了匿名内部类的方式定义了一个新的迭代器，这个迭代器中每一个方法都是通过调用之前创建好的延迟迭代器lookupIterator来完成的

最后就是进行迭代加载了。
```text
while(it.hasNext())
    System.out.println(it.next().getName());
```
hasNext方法调用了延迟迭代器的hasNext方法，内部调用了hasNextService方法，在这个方法中就会设法去找到指定名称（META-INF/services/+接口全限定名）的资源文件。并完成读取文件内容的操作。

然后执行it.next()操作，这个又会调用延迟迭代器的对应方法hasNext，内部调用了nextService方法，这个方法主要功能就是加载上面从文件中读取到的全限定名称表示的类。并生成实例，将实例保存到providers中。
```text
private LinkedHashMap<String,S> providers = new LinkedHashMap<>();
```

