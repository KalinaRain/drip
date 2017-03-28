# Android面试知识点（整理中）  

>转眼间学习Android已经有3年了，再加上最近要找工作，所以想着把Android面试的各种知识点总结并整理一下，也算是对这一段时间的付出做个总结。  
>要找一份好工作，自然要对Android，Java，数据结构，算法，计算机基础等知识点都非常熟悉，除此之外还要注重细节，如果你已经经历过一些大公司的面试，相信你已经知道了细节的重要性。

我会持续更新的，欢迎watch

<hr width=100% size=3 color=#d8d8d8>

# <p id="top">目录</p>  
[一、Java](#1)  
* Java基本概念
* Java面向对象  

[二、Android](#2)  

[三、数据结构](#3)  

[四、算法](#4)  

[五、计算机基础](#5)  

<hr width=100% size=3 color=#d8d8d8>

<h1 id="1">一、Java</h1>

## Java基本概念
[Java基本概念](Java/Java基本概念.md)  

## Java面向对象
Java是面向对象编程（OOP），因此，面向对象的相关知识如三大特征和六大基本原则也是需要掌握的。  
[Java之面向对象编程](Java/Java之面向对象编程.md)  

### 重载和覆写
对于重载和覆写，除了基本知识外，最重要的就是子类和父类中重载和覆写需要注意的事项。  
[重载和覆写](Java/重载和覆写.md)

### Java语法基础

#### 8种基本数据类型的大小，以及他们的封装类  
|数据类型|大小(字节)|   范围    |封装类|
|:------:|:----:| :----:|---|
|byte    |   1  |  -2^7～2^7-1  | Byte |
|short   |   2  | -2^15～2^15-1 |Short|
|int     |   4  | -2^31～2^31-1 |Integer|
|long    |   8  |-2^63 ～2^63-1 |Long|
|float   |   4  |-3.4E38～3.4E38 |Float|
|double  |   8  | -1.7E308～1.7E308 |Double|
|boolean |   1  |  true或false  |Boolean|
|char    |   2  |从字符型对应的整型数来划分，其表示范围是0～65535||

整数默认int，小数默认double

自动装箱是 Java 编译器在基本数据类型和对应的对象包装类型之间做的一个转化。比如：把 int 转化成 Integer ，double 转化成 Double，等等。反之就是自动拆箱。

#### 运算符的优先级
#### 值传递和引用传递
对象被值传递，意味着传递了对象的一个副本。因此，就算是改变了对象副本，也不会影响源对象的值。  
对象被引用传递，意味着传递的并不是实际的对象，而是对象的引用。因此，外部对引用对象所做的改变会反映到所有的对象上。  
所有的基本数据类型都是值传递，而

### 不同编码下字母与中文的大小

>一个 ".java" 源文件中是否可以包括多个类（不是内部类）？有什么限制？  
可以有多个类，但只能有一个 public 的类(除了内部类)，并且 public 的类名必须与文件名相一致。

静态变量和实例变量的区别？
在语法定义上的区别：静态变量前要加 static 关键字，而实例变量前则不加。  
在程序运行时的区别：实例变量属于某个对象的属性，必须创建了实例对象，其中的实例变量才会被分配空间，才能使用这个实例变量。静态变量不属于某个实例对象，而是属于类，所以也称为类变量，只要程序加载了类的字节码，不用创建任何实例对象，静态变量就会被分配空间，静态变量就可以被使用了。总之，实例变量必须创建对象后才可以通过这个对象来使用，静态变量则可以直接使用类名来引用。

例如，对于下面的程序，无论创建多少个实例对象，永远都只分配了一个 staticVar 变量，并且每创建一个实例对象，这个 staticVar 就会加 1 ；但是，每创建一个实例对象，就会分配一个 instanceVar ，即可能分配多个 instanceVar ，并且每个instanceVar 的值都只自加了 1 次。  
<pre><code>  
 public class VariantTest{   
    public static int staticVar = 0;    
    public int instanceVar = 0;    
    public VariantTest(){    
        staticVar++;    
        instanceVar++;    
        System.out.println(“staticVar=” + staticVar + ”,instanceVar=” + instanceVar);   
        } 
 }    </code></pre>  

不通过构造函数也能创建对象吗?
>可以。Java 创建对象的几种方式（重要）：  
(1) 用 new 语句创建对象，这是最常见的创建对象的方法。  
(2) 运用反射手段,调用 java.lang.Class 或者 java.lang.reflect.Constructor 类的 newInstance() 实例方法。  
(3) 调用对象的 clone() 方法。  
(4) 运用反序列化手段，调用 java.io.ObjectInputStream 对象的 readObject() 方法。  
(1)和(2)都会明确的显式的调用构造函数 ；(3)是在内存上对已有对象的影印，所以不会调用构造函数 ；(4)是从文件中还原类的对象，也不会调用构造函数。

静态变量和实例变量的区别？
>答：静态变量是被 static 修饰符修饰的变量，也称为类变量，它属于类，不属于类的任何一个对象，一个类不管创建多少个对象，静态变量在内存中有且仅有一个拷贝；实例变量必须依存于某一实例，需要先创建对象然后通过对象才能访问到它。静态变量可以实现让多个对象共享内存。在 Java 开发中，上下文类和工具类中通常会有大量的静态成员。

是否可以从一个静态（static）方法内部发出对非静态（non-static）方法的调用？
>答：不可以，静态方法只能访问静态成员，因为非静态方法的调用要先创建对象，因此在调用静态方法时可能对象并没有被初始化。

 如何实现对象克隆？
>答：有两种方式：   
1.实现 Cloneable 接口并重写 Object 类中的 clone() 方法；  
2.实现 Serializable 接口，通过对象的序列化和反序列化实现克隆，可以实现真正的深度克隆。

 一个“.java”源文件中是否可以包含多个类（不是内部类）？有什么限制？
>答：可以，但一个源文件中最多只能有一个公开类（public class）而且文件名必须和公开类的类名完全保持一致。

Anonymous Inner Class(匿名内部类)是否可以继承其它类？是否可以实现接口？
>答：可以继承其他类或实现其他接口，在Swing编程中常用此方式来实现事件监听和回调。

内部类可以引用它的包含类（外部类）的成员吗？有没有什么限制？
>答：一个内部类对象可以访问创建它的外部类对象的成员，包括私有成员

列出自己常用的 jdk 包.
>答：JDK 常用的 package  
java.lang：这个是系统的基础类，比如 String 等都是这里面的，这个 package 是唯一一个可以不用 import 就可以使用的 Package  
java.io: 这里面是所有输入输出有关的类，比如文件操作等  
java.net: 这里面是与网络有关的类，比如 URL,URLConnection 等。  
java.util: 这个是系统辅助类，特别是集合类 Collection,List,Map 等。  
java.sql: 这个是数据库操作的类，Connection, Statememt，ResultSet 等


### 几个关键字volatile、transient、synchronized、native  
transient变量不会进行序列化。例如一个实现Serializable接口的类在序列化到ObjectStream的时候，transient类型的变量不会被写入流中，同时，反序列化回来的时候，对应变量的值为null。

### abstract类和interface
[abstract类和interface] (Java/interface和abstract classs.md)  

### 实例变量，局部变量，类变量，final变量的区别

### 访问修饰符public protected private default（不写）的区别：
|修饰符  |当前类 |同包 |子类 |其他包|
|:------:|:-----:|:---:|:---:|:----:|
| public |  √   |  √ |  √ |  √  |
|protected| √   |  √ |  √ |  ×  |
| default|  √   |  √ |  × |  ×  |
| private|  √   |  × |  × |  ×  |

### 基础
Object有哪些公用方法？

Override和Overload的使用规则和区别

Switch的作用类型
能否用string做参数？

equals与==的区别

try catch finally，try里有return，finally还执行么？

### 类的加载机制和初始化机制

### 数据在内存中的存储




### 同步和异步
数据一致性如何保证；Synchronized关键字，类锁，方法锁，重入锁
同步的方法；多进程开发以及多进程应用场景
服务器只提供数据接收接口，在多线程或多进程条件下，如何保证数据的有序到达

### ThreadLocal原理，实现及如何保证Local属性

### String StringBuilder StringBuffer对比


接口与回调；回调的原理；写一个回调demo；

#### 泛型原理，举例说明；

解析与分派



***

静态属性和静态方法是否可以被继承？是否可以被重写？原因

修改对象A的equals方法的签名，那么使用HashMap存放这个对象实例的时候，会调用哪个equals方法

### Collection（Set|List）与Map
[Collection与Map](Collection与Map.md)
Map、Set、List、Queue、Stack的特点与用法

### Excption与Error包结构,OOM和SOF

### HashMap和HashTable的区别

HashMap源码分析

### IO流
[IO流知识](Java/IO流.md)  

Hashcode的作用


从源码分析String、StringBuffer与StringBuilder区别和联系

### 线程
多线程下生产者消费者问题的五种同步方法实现
多线程与线程池
实现多线程的两种方法
ThreadLocal的使用规则和源码分析

ThreadPool用法与示例
wait()和sleep()的区别
线程同步的方法：sychronized、lock、reentrantLock分析


方法锁、对象锁和类锁的意义和区别

四种引用，强弱软虚，用到的场景


集合框架的层次结构和使用规则梳理

static的作用和意义

多态实现的JVM调用过程


### java反射


java回调

Java泛型

java 新特性

Java IO与NIO

foreach与正常for循环效率对比

多线程
http://droidyue.com/blog/2014/12/21/string-literal-pool-in-java/
http://droidyue.com/blog/2014/12/07/differences-between-stack-and-heap-in-java/
http://droidyue.com/blog/2014/12/21/java-runtime-data-areas/
http://www.importnew.com/18548.html

java 面试整理：
https://sunchenglong.gitbooks.io/java-interview  

java面试一定会遇到的56个面试题：
http://mp.weixin.qq.com/s?__biz=MzI0MjE3OTYwMg==&mid=2649547702&idx=1&sn=431dcb8cef6518fd852c32b57d79d538&scene=21#wechat_redirect

 http://blog.csdn.net/sinat_35512245/article/details/59056120

问：如果main方法被声明为private会怎样？  
>答：能正常编译，但运行的时候会提示”main方法不是public的”。

<a href="#top" style="display:block;text-align:right;">返回顶部</a>
<hr width=100% size=3 color=#d8d8d8>

<h1 id="2">二、Android</h1>  
### 面试

#### Android开机过程：  
* BootLoder引导,然后加载Linux内核.
* 0号进程init启动.加载init.rc配置文件,配置文件有个命令启动了zygote进程
* zygote开始fork出SystemServer进程
* SystemServer加载各种JNI库,然后init1,init2方法,init2方法中开启了新线程ServerThread.
* 在SystemServer中会创建一个socket客户端，后续AMS（ActivityManagerService）会通过此客户端和zygote通信
* ServerThread的run方法中开启了AMS,还孵化新进程ServiceManager,加载注册了一溜的服务,最后一句话进入loop 死循环
run方法的SystemReady调用resumeTopActivityLocked打开锁   屏界面

#### App启动过程：

#### ART和Dalvik区别：  
Art上应用启动快，运行快，但是耗费更多存储空间，安装时间长，总的来说ART的功效就是"空间换时间"。
ART: Ahead of Time Dalvik: Just in Time
什么是Dalvik：Dalvik是Google公司自己设计用于Android平台的Java虚拟机。Dalvik虚拟机是Google等厂商合作开发的Android移动设备平台的核心组成部分之一，它可以支持已转换为.dex(即Dalvik Executable)格式的Java应用程序的运行，.dex格式是专为Dalvik应用设计的一种压缩格式，适合内存和处理器速度有限的系统。Dalvik经过优化，允许在有限的内存中同时运行多个虚拟机的实例，并且每一个Dalvik应用作为独立的Linux进程执行。独立的进程可以防止在虚拟机崩溃的时候所有程序都被关闭。

什么是ART:Android操作系统已经成熟，Google的Android团队开始将注意力转向一些底层组件，其中之一是负责应用程序运行的Dalvik运行时。Google开发者已经花了两年时间开发更快执行效率更高更省电的替代ART运行时。ART代表Android Runtime,其处理应用程序执行的方式完全不同于Dalvik，Dalvik是依靠一个Just-In-Time(JIT)编译器去解释字节码。开发者编译后的应用代码需要通过一个解释器在用户的设备上运行，这一机制并不高效，但让应用能更容易在不同硬件和架构上运行。ART则完全改变了这套做法，在应用安装的时候就预编译字节码到机器语言，这一机制叫Ahead-Of-Time(AOT)编译。在移除解释代码这一过程后，应用程序执行将更有效率，启动更快。

ART优点：

系统性能的显著提升
应用启动更快、运行更快、体验更流畅、触感反馈更及时
更长的电池续航能力
支持更低的硬件

ART缺点：
更大的存储空间占用，可能会增加10%-20%
更长的应用安装时间

#### 各种Context的区别：  
* Activity和Service以及Application的Context是不一样的,Activity继承自ContextThemeWraper.其他的继承自ContextWrapper
* 每一个Activity和Service以及Application的Context都是一个新的ContextImpl对象
* getApplication()用来获取Application实例的，但是这个方法只有在Activity和Service中才能调用的到。那么也许在绝大多数情况下我们都是在Activity或者Service中使用Application的，但是如果在一些其它的场景，比如BroadcastReceiver中也想获得Application的实例，这时就可以借助getApplicationContext()方法，getApplicationContext()比getApplication()方法的作用域会更广一些，任何一个Context的实例，只要调用getApplicationContext()方法都可以拿到我们的Application对象。
* Activity在创建的时候会new一个ContextImpl对象并在attach方法中关联它，Application和Service也差不多。ContextWrapper的方法内部都是转调ContextImpl的方法
*创建对话框传入Application的Context是不可以的
* 尽管Application、Activity、Service都有自己的ContextImpl，并且每个ContextImpl都有自己的mResources成员，但是由于它们的mResources成员都来自于唯一的ResourcesManager实例，所以它们看似不同的mResources其实都指向的是同一块内存
* Context的数量等于Activity的个数 + Service的个数 + 1，这个1为Application

#### 四大组件与Fragment
Activity 与Fragment（生命周期，四种启动模式） 生命周期：
电话打进来：
home键：

Service全面总结与IntentService

IntentService使用详解和实例介绍 

Android 名企面试题及答案整理（一）

View的绘制流程；自定义View如何考虑机型适配；自定义View的事件分发机制；View和ViewGroup分别有哪些事件分发相关的回调方法；自定义View如何提供获取View属性的接口；  
Art和Dalvik对比；虚拟机原理，如何自己设计一个虚拟机(内存管理，类加载，双亲委派)；JVM内存模型及类加载机制；内存对象的循环引用及避免  
内存回收机制与GC算法(各种算法的优缺点以及应用场景)；GC原理时机以及GC对象；内存泄露场景及解决方法；OOM的避免及解决方法
四大组件及生命周期；ContentProvider的权限管理(读写分离，权限控制-精确到表级，URL控制)；Activity的四种启动模式对比；Activity状态保存于恢复  
Fragment生命周期；Fragment状态保存  
startActivityForResult是哪个类的方法，在什么情况下使用，如果在Adapter中使用应该如何解耦  
AsyncTask原理及不足;IntentService原理  
AstncTask+HttpClient与AsyncHttpClient有什么区别  
如何保证一个后台服务不被杀死；比较省电的方式是什么  
如何通过广播拦截和abort一条短信；广播是否可以请求网络；广播引起anr的时间限制  
进程间通信，AIDL  
Handler机制及底层实现  
Binder机制及底层实现  
ApplicationContext和ActivityContext的区别  
一张Bitmap所占内存以及内存占用的计算  
对于应用更新这块是如何做的？(灰度，强制更新，分区域更新)  
混合开发，RN，weex，H5，小程序(做Android的了解一些前端js等还是很有好处的)  
说一款你认为当前比较火的应用并设计(直播APP)


消息处理机制
Binder
AIDL
VIew绘制
事件分发机制

jvm

GC

### 产品架构 MVP MVC MVVM
### Android中设计模式的应用与Android 源码中的设计模式

### 性能优化

### 源码分析
内存泄露
进程保活
AsyncTask

Serializable 和Pacleable
Handler Message Looper
IntentService和Service  HandlerThread ServiceHandler 
Parcelable和Serializable

Fragment 全解析

ContentProvider实例详解

BroadcastReceiver使用总结

Android异步任务机制之AsycTask

Android启动过程图解

Android 自定义View入门

Android 自定义ViewGroup入门实践

Android 缓存机制

Android 数据存储五种方式使用与总结

Android 异步消息处理机制源码解析

Android View事件分发机制源码分析

Android SQLite的使用入门

AIDL的使用情况和实例介绍

Android中弱引用与软引用的应用场景

Android长连接，怎么处理心跳机制

Asset目录与res目录的区别

Binder机制原理和底层实现

Json优劣势

ListView优化

android中图片缓存

两类动画

五大布局易混淆知识

保证service不被杀死

加速启动activity

怎样退出终止App

activity切换动画

贝赛尔曲线（安卓水波运动效果）

性能优化
启动加速
布局性能优化(include, viewstub, merge)
OOM
电量

XML解析（DOM、SAX、Pull的区别和优缺点）

### 热修复


除此之外，也有不少大牛将安卓面试的知识点整理过，有兴趣的可以访问看看。
https://hit-alibaba.github.io/interview
https://github.com/karmalove/AndroidInterview

<a href="#top" style="display:block;text-align:right;">返回顶部</a>
<hr width=100% size=3 color=#d8d8d8>

<h1 id="3">数据结构</h1>  
堆和栈在内存中的区别是什么(数据结构方面以及实际实现方面)
最快的排序算法是哪个？给阿里2万多名员工按年龄排序应该选择哪个算法？堆和树的区别；写出快排代码；链表逆序代码
求1000以内的水仙花数以及40亿以内的水仙花数
子串包含问题(KMP 算法)写代码实现
万亿级别的两个URL文件A和B，如何求出A和B的差集C,(Bit映射->hash分组->多文件读写效率->磁盘寻址以及应用层面对寻址的优化)
蚁群算法与蒙特卡洛算法
写出你所知道的排序算法及时空复杂度，稳定性
百度POI中如何试下查找最近的商家功能(坐标镜像+R树)

哈弗曼树（建立）
建堆
死锁的四个必要条件
常见编码方式；utf-8编码中的中文占几个字节；int型几个字节
实现一个Json解析器(可以通过正则提高速度)
MVC MVP MVVM; 常见的设计模式；写出观察者模式的代码


5枚硬币，2正3反如何划分为两堆然后通过翻转让两堆中正面向上的硬币和反面向上的硬币个数相同
时针走一圈，时针分针重合几次
N * N的方格纸,里面有多少个正方形
现在下载速度很慢,试从网络协议的角度分析原因,并优化(网络的5层都可以涉及)

已知进栈的顺序，求出栈的顺序

完全二叉树的深度表达式
已知前序遍历和中序遍历，求后序遍历；已知后序遍历和中序遍历，求前序遍历；
合法的堆

已知栈的输入序列为1.2.3，则经过栈的作用后可以得到几种不同的输出序列——卡特兰数

递归转化为非递归（不是所有的递归转化为非递归都要用到栈，方法有两种，对于尾递归和单向递归可以使用循环结构算法替代，另外一个才是栈）
二叉树的宽度优先遍历和深度优先遍历 按层遍历

字符串的nextval和next KMP算法

<a href="#top" style="display:block;text-align:right;">返回顶部</a>
<hr width=100% size=3 color=#d8d8d8>

<h2 id="4">算法</h2>
>对于算法，本人一直认为这是个很高大上的东西，而且事实上他也确实很高大上，如果真的要想提升自己的算法水平，最好是去刷题，单纯的看别人的博客，效果不是很大。目前比较出名的算法刷题网站（online judge）有[lintcode](http://www.lintcode.com/zh-cn/)、 [leetcode](https://leetcode.com/)、 [hihocoder](http://hihocoder.com/)，以及各大高校的网站[参考](http://www.cnblogs.com/Xredman/archive/2009/03/23/1420015.html)。

Trie树  

https://github.com/Dev-XYS/Algorithms  
https://leetcode.com/problemset/algorithms/  
http://blog.csdn.net/v_july_v/article/details/6543438  
http://blog.csdn.net/v_july_v/article/details/7041827  
http://selfboot.cn/2016/07/24/leetcode_guide_why/  
https://github.com/xuelangZF/LeetCode/tree/master/HashTable  
https://github.com/scottszb1987/LeetCodeInCSharp  
https://github.com/shawnfan/LintCode  
http://hihocoder.com/problemset  
http://www.lintcode.com/zh-cn/problem/  
https://nanti.jisuanke.com/  
排序
https://zhuanlan.zhihu.com/p/25498681
https://juejin.im/post/5874bff0128fe1006b443fa0
http://www.jianshu.com/p/1b824e26105b
https://gold.xitu.io/post/57dcd394a22b9d00610c5ec8
https://juejin.im/post/57dcd394a22b9d00610c5ec8

https://github.com/GeniusVJR/LearningNotes

http://blog.tingyun.com/web/article/detail/155
http://www.jianshu.com/p/89f19d67b348
http://www.trinea.cn/android/java-annotation-android-open-source-analysis/
http://www.tuicool.com/articles/QB73eyf
https://gist.github.com/errord/7801466

<a href="#top" style="display:block;text-align:right;">返回顶部</a>
<hr width=100% size=3 color=#d8d8d8>

<h1 id="5">计算机基础</h1>
### 计算机网络

Http TCP/IP 
TCP与UDP的区别
TCP的三次握手和四次挥手
HTTP协议；HTTP1.0与2.0的区别；HTTP报文结构
HTTP与HTTPS的区别以及如何实现安全性

sql语句：

### 操作系统
后缀表达式（逆波兰）
16进制转化8进制 2进制

实模式和保护模式 http://blog.csdn.net/rosetta/article/details/8933200
线程与进程
线程和进程的区别联系：
1，进程：子进程是父进程的复制品。子进程获得父进程数据空间、堆和栈的复制品。
2，线程：相对与进程而言，线程是一个更加接近与执行体的概念，它可以与同进程的其他线程共享数据，但拥有自己的栈空间，拥有独立的执行序列。   
两者都可以提高程序的并发度，提高程序运行效率和响应时间。   
线程和进程在使用上各有优缺点：线程执行开销小，但不利于资源管理和保护；而进程正相反。同时，线程适合于在SMP机器上运行，而进程则可以跨机器迁移。
根本区别就一点：用多进程每个进程有自己的地址空间(address space)，线程则共享地址空间。所有其它区别都是由此而来的： 
1、速度：线程产生的速度快，线程间的通讯快、切换快等，因为他们在同一个地址空间内。 
2、资源利用率：线程的资源利用率比较好也是因为他们在同一个地址空间内。 
3、同步问题：线程使用公共变量/内存时需要使用同步机制还是因为他们在同一个地址空间内
1.进程有独立的进程空间，进程中的数据存放空间（堆空间和栈空间）是独立的。
2.线程的堆空间是共享的，栈空间是独立的，线程消耗的资源也比进程小，二者之间可以相互影响。
进程间的通信方式
1.管道
2.信号量
3.消息队列
4.信号
5.共享内存
6.套接字

# OS

**进程和线程**

关系：

一个进程可以创建和撤销另一个线程，同一个进程中的线程可以并发执行。

**死锁的必要条件，怎么处理死锁。**

**Window内存管理方式：段存储，页存储，段页存储。**

**进程的几种状态和转换**

**什么是虚拟内存。**

**Linux下的IPC几种通信方式**

1. 管道(pipe):管道可用于具有亲缘关系的进程间的通信，是一种半双工的方式，数据只能单向流动，允许一个进程和另一个与它有公共祖先的进程之间进行通信。
2. 命名管道(named pipe):命名管道克服了管道没有名字的限制，同时除了具有管道的功能外(也是半双工)，它还允许无亲缘关系进程间的通信。命令管道在文件系统中有对应的文件名。命令管道通过命令mkfifo或系统调用mkfifo来创建。
3. 信号(signal):信号是比较复杂的通信方式，用于通知接收进程有某种事件发生了，除了进程间通信外，进程还可以发送信号给进程本身。
4. 消息队列:消息队列是消息的链接表，包括Posix消息队列和system V消息队列。有足够权限的进程可以向队列中添加消息，被赋予读权限的进程可以读走队列中的消息。消息队列克服了信号承载信息少，管道只能承载无格式字节流以及缓冲区大小受限等缺点。
5. 共享内存:使得多个进程可以访问同一块内存空间，是最快的IPC形式。是针对其他通信机制运行效率低而设计的。往往与其他通信机制，如信号量结合使用，来达到进程间的同步及互斥。
6. 内存映射:内存映射允许任何多个进程间通信每一个使用该机制的进程通过把一个共享的文件映射到自己的进程地址空间来实现它。
7. 信号量(semaphore):主要作为进程间以及同一进程不同线程之间的同步手段。
8. 套接字(Socket):更为一般的进程间通信机制，可用于不同机器之间的进程间通信。
 
**逻辑地址、物理地址的区别**

**进程调度算法**


# Linux系统的IPC

**线程之间不存在通信,因为本来就共享同一片内存**

各个线程可以访问进程中的公共变量，资源，所以使用多线程的过程中需要注意的问题是如何防止两个或两个以上的线程同时访问同一个数据，以免破坏数据的完整性。数据之间的相互制约包括
1、直接制约关系,即一个线程的处理结果,为另一个线程的输入,因此线程之间直接制约着，这种关系可以称之为同步关系
2、间接制约关系，即两个线程需要访问同一资源,该资源在同一时刻只能被一个线程访问,这种关系称之为线程间对资源的互斥访问，某种意义上说互斥是一种制约关系更小的同步

## 线程间同步

* 临界区
  * 每个线程中访问临界资源的代码,一个线程拿到临界区的所有权后,可以多次重入.只有前一个线程放弃,后一个才可以进来

* 互斥量
  * 互斥量就是简化版的信号量
  * 互斥量由于也有线程所有权的概念，故也只能进行线程间的资源互斥访问，不能由于线程同步
  * 由于互斥量是内核对象，因此其可以进行进程间通信，同时还具有一个很好的特性，就是在进程间通信时完美的解决了"遗弃"问题


* 信号量
  * 信号量的用法和互斥的用法很相似，不同的是它可以同一时刻允许多个线程访问同一个资源，PV操作
  * 信号量也是内核对象,也可以进行进程间通信

## 进程间通信

* 管道
  * 半双工
  * 只能在具有父子关系的进程间使用
  * FIFO的共享内存实现
* 命名管道
  * 以linux中的文件的形式存在
  * 不要求进程有用父子关系,甚至通过网络也是可以的
  * 半双工
* 信号量
  * 有up和down操作
  * 共享内存实现


* 消息队列
  * 队列数据结构
  * 共享内存实现
* 信号
  * 较为复杂的方式,用于通知进程某事件已经发生.例如kill信号


* 共享内存
  * 将同一个物理内存附属到两个进程的虚拟内存中
* socket
  * 可以跨网络通信

