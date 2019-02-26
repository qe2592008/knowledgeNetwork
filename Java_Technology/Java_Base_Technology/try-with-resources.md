# try-with-resources

这是编译器语法糖之一，用于自动关闭资源。
- 资源必须实现了AutoCloseable或者Closeable接口，表示可关闭。
- 如果在try块中出现了异常，同时在资源关闭也出现异常，那么资源关闭的异常将会被抑制，可通过e.getSuppressed找回被抑制的异常。
- 语法如下：
```java
public class TryWithResourcesTest {
    public static void main(String[] args) {
        try (
                InputStream is = new FileInputStream(new File("")); 
                OutputStream os = new FileOutputStream(new File(""))) {
            byte[] bs = new byte[100];
            is.read(bs);
            os.write(bs);
        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            // do other things
        }
    }
}
```