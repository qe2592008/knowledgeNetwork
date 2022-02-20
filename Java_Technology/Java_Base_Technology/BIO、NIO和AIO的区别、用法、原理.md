# BIO、NIO和AIO的区别、用法、原理
## BIO
### 特点
    BIO是同步阻塞IO
    一个线程对应一个连接
### 原理
    
### 用法
客户端代码：
```java
public class ClientTest {
    public static void main(String[] args) {
        bioClient();
    }

    public static void bioClient(){
        try (Socket socket = new Socket("localhost",12332);
             OutputStream os = socket.getOutputStream();
             ) {
            String s = "test message";
            os.write(s.getBytes());
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```
服务端代码：
```java
public class ServerTest {
    public static void main(String[] args) {
        try (
                ServerSocket serverSocket = new ServerSocket(12332);
                Socket socket = serverSocket.accept();
                InputStream is = socket.getInputStream();
                OutputStream os = new FileOutputStream(new File("C:\\Users\\Administrator\\Desktop\\test.txt"));
                ) {
            byte[] bs = new byte[1024];
            is.read(bs);
            os.write(bs);
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```
## NIO
### 特点
    NIO是同步非阻塞IO，线程一直处于等待中，对应的多个连接注册到了多路复用器之上，多路复用器轮询这些连接，一旦某个连接接收到数据则线程读取这个连接的数据
    一个线程对应多个连接
### 原理
    
### 用法

## AIO
### 特点
    AIO是异步非阻塞IO
    
### 原理
    
### 用法