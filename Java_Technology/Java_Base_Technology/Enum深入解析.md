# Java基础-Enum深入解析
枚举整体就是一个语法糖效果。

定义一个枚举，其实就是继承抽象类Enum。

了解了Enum，就能了解枚举。

### 接口
```java
public abstract class Enum<E extends Enum<E>>
        implements Comparable<E>, Serializable {}
```
枚举类实现了Comparable和Serializable接口，那么也就意味着，每个枚举类都拥有比较（有序）和序列化功能。
### 属性
```java
public abstract class Enum<E extends Enum<E>>
        implements Comparable<E>, Serializable {
    private final String name;
    private final int ordinal;
    public final String name() {
        return name;
    }
    public final int ordinal() {
        return ordinal;
    }    
}
```
这两个属性是枚举的内置属性，name表示的是枚举值的名称，ordinal表示的是枚举值的序号。

其作用后面再说
### 构造器
```java
public abstract class Enum<E extends Enum<E>>
        implements Comparable<E>, Serializable {
    protected Enum(String name, int ordinal) {
        this.name = name;
        this.ordinal = ordinal;
    }
}
```
Enum中只有这一个构造器，其申明为protected就是为了继承它的子类（我们定义的各种枚举）来调用的。
### equals方法
```java
public abstract class Enum<E extends Enum<E>>
        implements Comparable<E>, Serializable {
    public final boolean equals(Object other) {
        return this==other;
    }
}
```
默认的equals方法底层就是使用==实现的，所以在枚举的比较使用equals和==都是可以的。前提是没有在枚举类中重写equals方法。

我们可以在自定义的枚举类中重写该方法，来实现我们自己的比较方式。
### 禁用的功能
```java
public abstract class Enum<E extends Enum<E>>
        implements Comparable<E>, Serializable {
    protected final Object clone() throws CloneNotSupportedException {
        throw new CloneNotSupportedException();
    }
    protected final void finalize() { }
    private void readObject(ObjectInputStream in) throws IOException,
        ClassNotFoundException {
        throw new InvalidObjectException("can't deserialize enum");
    }
    private void readObjectNoData() throws ObjectStreamException {
        throw new InvalidObjectException("can't deserialize enum");
    }   
}
```
这四个方法均是被禁用的方法：
- 克隆：目的为了保证单例唯一
- finalize：
- 序列化中禁用readObject和readObjectNoData方法：目的为了保证单例唯一
### compareTo方法
```java
public abstract class Enum<E extends Enum<E>>
        implements Comparable<E>, Serializable {
    public final int compareTo(E o) {
        Enum<?> other = (Enum<?>)o;
        Enum<E> self = this;
        if (self.getClass() != other.getClass() && // optimization
            self.getDeclaringClass() != other.getDeclaringClass())
            throw new ClassCastException();
        return self.ordinal - other.ordinal;
    }
}
```
这是实现了接口Comparable中的方法。用于定义比较的方式，可以看出这里是使用枚举值的序号作为比较条件的。
### valueOf方法
```java
public abstract class Enum<E extends Enum<E>>
        implements Comparable<E>, Serializable {
    public static <T extends Enum<T>> T valueOf(Class<T> enumType,
                                                String name) {
        T result = enumType.enumConstantDirectory().get(name);
        if (result != null)
            return result;
        if (name == null)
            throw new NullPointerException("Name is null");
        throw new IllegalArgumentException(
            "No enum constant " + enumType.getCanonicalName() + "." + name);
    }
}
```
该方法的作用是获取到指定枚举类型中指定枚举名称的枚举值。
