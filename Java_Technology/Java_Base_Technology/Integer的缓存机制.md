# Integer的缓存机制

Integer的valueOf是装箱方法，源码如下：
```java
public final class Integer extends Number implements Comparable<Integer> {
    public static Integer valueOf(int i) {
        if (i >= IntegerCache.low && i <= IntegerCache.high)
            return IntegerCache.cache[i + (-IntegerCache.low)];
        return new Integer(i);
    }
}
```
这里涉及到了一个内部类：IntegerCache。
```java
public final class Integer extends Number implements Comparable<Integer> {
    private static class IntegerCache {
        static final int low = -128;// 最小值固定位-128
        static final int high;
        static final Integer cache[];

        static {
            // high value may be configured by property
            int h = 127;// 最大值默认为127
            String integerCacheHighPropValue =
                sun.misc.VM.getSavedProperty("java.lang.Integer.IntegerCache.high");// 读取属性的值作为备用最大值
            if (integerCacheHighPropValue != null) {
                try {
                    int i = parseInt(integerCacheHighPropValue);
                    i = Math.max(i, 127);// 如果设置的最大值比127小，将延用127
                    // Maximum array size is Integer.MAX_VALUE
                    h = Math.min(i, Integer.MAX_VALUE - (-low) -1);// 但如果设置额最大值比Integer.MAX_VALUE-129还大，则使用后者，保证缓存数组的最大容量不会超过Integer.MAX_VALUE
                } catch( NumberFormatException nfe) {
                    // If the property cannot be parsed into an int, ignore it.
                }
            }
            high = h;

            cache = new Integer[(high - low) + 1];// 创建缓存数组，数组容量最大为Integer.MAX_VALUE
            int j = low;
            for(int k = 0; k < cache.length; k++)
                cache[k] = new Integer(j++);

            // range [-128, 127] must be interned (JLS7 5.1.7)
            assert IntegerCache.high >= 127;
        }

        private IntegerCache() {}
    }
}
```
这个类用于描述Integer中的缓存：
- 缓存的最小值固定位-128
- 缓存的最大值默认为127，其实最大值的最小值也为127，如果设置的最大值小于127，会被忽略
- 缓存的最大值可通过VM参数设置`-XX:AutoBoxCacheMax=200`的方式设置缓存的数值范围，这里设置成200，那么最大值为71。
- 如果设置的最大值比127小，将延用127
- 如果设置额最大值比Integer.MAX_VALUE-129还大，则使用后者，保证缓存数组的最大容量不会超过Integer.MAX_VALUE

实例：
```java
public class IntegerTest {
    public static void main(String[] args) {
        Integer i = 100;// 经历装箱-使用缓存
        Integer j = 100;// 经历装箱-使用缓存
        Integer k = 128;// 经历装箱-不使用缓存
        Integer h = 128;// 经历装箱-不使用缓存
        int l = 100;// 数值
        int m = 100;// 数值
        int n = 128;// 数值
        Integer o = new Integer(100);// 堆中创建对象
        Integer p = new Integer(100);// 堆中创建对象
        Integer q = new Integer(128);// 堆中创建对象
        System.out.println(i==j);// true-经历装箱，使用缓存，所以一致
        System.out.println(l==m);// true-基本类型比较值，当然一致
        System.out.println(o==p);// false-分别在堆中创建，位置不同
        System.out.println(i==l);// true-需要进行拆箱，变成两个基本类型比较，当然一致
        System.out.println(k==n);// true-同上
        System.out.println(l==o);// true-同上
        System.out.println(n==q);// true-同上
        System.out.println(i==o);// false-一个经历装箱，使用缓存值，一个在堆中建立，位置不同
        System.out.println(k==h);// false-经历装箱，但无法使用缓存，位置不同
    }
}
```