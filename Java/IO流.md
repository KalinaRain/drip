# IO流  

IO流分为字符流和字节流，分类基本上只有笔试的时候会考到，但是说道IO流，最常考也是最常用的就是使用IO流读取数据

## IO流分类图片
![IO](image/IO流分类.jpg)  

如上所示，
面向字节的操作为以 8 位为单位对二进制的数据进行操作，对数据不进行转换，这些类都是 InputStream 和 OutputStream 的子类。

面向字符的操作为以字符为单位对数据进行操作，在读的时候将二进制数据转为字符，在写的时候将字符转为二进制数据，这些类都是 Reader 和 Writer 的子类。

总结：以 InputStream（输入）/OutputStream（输出）为后缀的是字节流；以Reader（输入）/Writer（输出）为后缀的是字符流。

2. 阅读 Shape 和 Circle 两个类的定义。在序列化一个 Circle 的对象 circle 到文件时，下面哪个字段会被保存到文件中？
<pre><code>
class Shape {

       public String name;

}

class Circle extends Shape implements Serializable{

       private float radius;

       transient int color;

       public static String type = "Circle";

}</code></pre>
A. name B. radius C. color D. type

答案：B

解析：这里有详细的解释：http://www.cnblogs.com/lanxuezaipiao/p/3369962.html

什么是 Java 序列化，如何实现 Java 序列化？  
序列化就是一种用来处理对象流的机制，所谓对象流也就是将对象的内容进行流化。可以对流化后的对象进行读写操作，也可将流化后的对象传输于网络之间。序列化是为了解决在对对象流进行读写操作时所引发的问题。

序列化的实现：将需要被序列化的类实现 Serializable 接口，该接口没有需要实现的方法， implements Serializable 只是为了标注该对象是可被序列化的，然后使用一个输出流(如：FileOutputStream)来构造一个ObjectOutputStream(对象流)对象，接着，使用ObjectOutputStream对象的writeObject(Object obj)方法就可以将参数为obj的对象写出(即保存其状态)，要恢复的话则用输入流。

## 读取文件