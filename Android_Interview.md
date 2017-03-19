# Android面试知识点（整理中）  

>转眼间学习Android已经有3年了，再加上最近要找工作，所以想着把Android面试的各种知识点总结并整理一下，也算是对这一段时间的付出做个总结。  
>要找一份好工作，自然要对Android，Java，数据结构，算法，计算机基础等知识点都非常熟悉，除此之外还要注重细节，如果你已经经历过一些大公司的面试，相信你已经知道了细节的重要性。

我会持续更新的，欢迎watch

<hr width=100% size=3 color=#d8d8d8>

## 目录  
[一、Java](#1)  

[二、Android](#2)  

[三、数据结构](#3)  

[四、算法](#4)  

[五、计算机基础](#5)  

<hr width=100% size=3 color=#d8d8d8>

<h2 id="1">一、Java</h2>
### Java基础面试

实例变量，局部变量，类变量，final变量的区别

public protected private default的区别：

#### 面向对象的六大原则  

* 单一职责原则  
　　所谓职责是指类变化的原因。如果一个类有多于一个的动机被改变，那么这个类就具有多于一个的职责。而单一职责原则就是指一个类或者模块应该有且只有一个改变的原因。通俗的说，即一个类只负责一项职责，将一组相关性很高的函数、数据封装到一个类中。

* 开闭原则  
　　对于扩展是开放的，这意味着模块的行为是可以扩展的。当应用的需求改变时，我们可以对模块进行扩展，使其具有满足那些改变的新行为。对于修改是关闭的，对模块行为进行扩展时，不必改动模块的源代码。通俗的说，尽量通过扩展的方式实现系统的升级维护和新功能添加，而不是通过修改已有的源代码。

* 里氏替换原则  
　　使用“抽象(Abstraction)”和“多态(Polymorphism)”将设计中的静态结构改为动态结构，维持设计的封闭性。任何基类可以出现的地方，子类一定可以出现。在软件中将一个基类对象替换成它的子类对象，程序将不会产生任何错误和异常，反过来则不成立。在程序中尽量使用基类类型来对对象进行定义，而在运行时再确定其子类类型，用子类对象来替换父类对象。

* 依赖倒置原则  
　　高层次的模块不应该依赖于低层次的模块，他们都应该依赖于抽象。抽象不应该依赖于具体实现，具体实现应该依赖于抽象。程序要依赖于抽象接口，不要依赖于具体实现。简单的说就是要求对抽象进行编程，不要对实现进行编程，这样就降低了客户与实现模块间的耦合（各个模块之间相互传递的参数声明为抽象类型，而不是声明为具体的实现类）。

* 接口隔离原则  
　　一个类对另一个类的依赖应该建立在最小的接口上。其原则是将非常庞大的、臃肿的接口拆分成更小的更具体的接口。

* 迪米特原则  
　　又叫作最少知识原则，就是说一个对象应当对其他对象有尽可能少的了解。通俗地讲，一个类应该对自己需要耦合或调用的类知道得最少，不关心被耦合或调用的类的内部实现，只负责调用你提供的方法。

#### 几个关键字volatile、transient、synchronized、native  
transient变量不会进行序列化。例如一个实现Serializable接口的类在序列化到ObjectStream的时候，transient类型的变量不会被写入流中，同时，反序列化回来的时候，对应变量的值为null。

#### abstract类和interface的区别


### 基础


进程和线程的区别；多线程与线程池
数据一致性如何保证；Synchronized关键字，类锁，方法锁，重入锁
同步的方法；多进程开发以及多进程应用场景
服务器只提供数据接收接口，在多线程或多进程条件下，如何保证数据的有序到达
#### ThreadLocal原理，实现及如何保证Local属性

#### String StringBuilder StringBuffer对比


接口与回调；回调的原理；写一个回调demo；

#### 泛型原理，举例说明；

解析与分派

抽象类与接口的区别；应用场景；抽象类是否可以没有方法和属性

静态属性和静态方法是否可以被继承？是否可以被重写？原因

修改对象A的equals方法的签名，那么使用HashMap存放这个对象实例的时候，会调用哪个equals方法

### Java Collection与Map
[Collection与Map](Collection与Map.md)


#### Excption与Error包结构,OOM和SOF

#### HashMap和HashTable的区别

HashMap源码分析

#### IO流
[IO流知识](/Java/IO流.md)  

Hashcode的作用

Map、Set、List、Queue、Stack的特点与用法

Object有哪些公用方法？

Override和Overload的使用规则和区别

Switch能否用string做参数？

equals与==的区别

try catch finally，try里有return，finally还执行么？

九种基本数据类型的大小，以及他们的封装类

从源码分析String、StringBuffer与StringBuilder区别和联系

### 线程
多线程下生产者消费者问题的五种同步方法实现

实现多线程的两种方法
ThreadLocal的使用规则和源码分析

ThreadPool用法与示例
wait()和sleep()的区别
线程同步的方法：sychronized、lock、reentrantLock分析


接口（Interface）与 抽象类 （Abstract）使用规则和区别

方法锁、对象锁和类锁的意义和区别

四种引用，强弱软虚，用到的场景


集合框架的层次结构和使用规则梳理

面向对象的三个特征与含义

static的作用和意义

多态实现的JVM调用过程


#### Java与C++对比
指针 Java 没有指针的概念，从而有效地防止了在 C/C++语言中，容易出现的指针操作失误（如指针悬空所造成的系统崩溃）。在 C/C++中，指针操作内存时，经常会出现错误。在Java 中没有指针，更有利于 Java 程序的安全。

多重继承 C++支持多重继承，它允许多父类派生一个子类。也就是说，一个类允许继承多个父类。尽管多重继承功能很强，但使用复杂，而且会引起许多麻烦，编译程序实现它也很不容易。所以 Java 不支持多重继承，但允许一个类实现多个接口。可见，Java 既实现了 C++多重继承的功能，又避免了 C++的许多缺陷。

数据类型 Java 是完全面向对象的语言，所有方法和数据都必须是类的一部分。除了基本数据类型之外，其余类型的数据都作为对象型数据。例如对象型数据包括字符串和数组。类将数据和方法结合起来，把它们封装在其中，这样每个对象都可实现具有自己特点的行为。而 C++将函数和变量定义为全局的，然后再来调用这些函数和变量，从而增加了程序的负担。此外，Java 还取消了 C/C++中的结构和联合，使编译程序更简洁。

自动内存管理 Java 程序中所有的对象都是用 new 操作符建立在堆栈上的，这个操作符类似于 C++的“new”操作符。Java 自动进行无用内存回收操作，不需要程序员进行删除。当 Java 中一个对象不再被用到时，无须使用内存回收器，只需要给它加上标签以示删除。无用内存的回收器在后台运行，利用空闲时间工作。而 C++中必须由程序释放内存资源，增加了程序设计者的负担。

操作符重载 Java 不支持操作符重载，操作符重载被认为是 C++的突出特征。在 Java 中虽然类可以实现这样的功能，但不支持操作符重载，这样是为了保持 Java 语言尽可能简单。

预处理功能 C/C++在编译过程中都有一个预编译阶段，即预处理器。预处理器为开发人员提供了方便，但增加了编译的复杂性。Java 允许预处理，但不支持预处理器功能，因为 Java 没有预处理器，所以为了实现预处理，它提供了引入语句（import），它与 C++预处理器的功能类似。

Java 不支持缺省函数参数，而 C++支持。 在 C 中，代码组织在函数中，函数可以访问程序的全局变量。C++增加了类，提供了类算法，该算法是与类相连的函数，C++类方法与 Java 类方法十分相似。由于 C++仍然支持 C，所以 C++程序中仍然可以使用 C 的函数，结果导致函数和方法混合使用，使得 C++程序比较混乱。

Java 没有函数，作为一个比 C++更纯的面向对象的语言。Java 强迫开发人员把所有例行程序包括在类中。事实上，用方法实现例行程序可激励开发人员更好地组织编码。

字符串 C 和 C++不支持字符串变量，在 C 和 C++程序中使用“Null”终止符代表字符串的结束，在 Java 中字符串是用类对象（String 和 StringBuffer）来实现的，在整个系统中建立字符串和访问字符串元素的方法是一致的。Java 字符串类是作为 Java 语言的一部分定义的，而不是作为外加的延伸部分。此外，Java 还可以对字符串用“+”进行连接操作。

goto 语句 “可怕”的 goto 语句是 C 和 C++的“遗物”。它是该语言技术上的合法部分，引用 goto语句造成了程序结构的混乱，不易理解。goto 语句一般用于无条件转移子程序和多结构分支技术。Java 不提供 goto 语句，其虽然指定 goto 作为关键字，但不支持它的使用，这使程序更简洁易读。

类型转换 在 C 和 C++中，有时出现数据类型的隐含转换，这就涉及了自动强制类型转换问题。例如，在 C++中可将一个浮点值赋予整型变量，并去掉其尾数。Java 不支持 C++中的自动强制类型转换，如果需要，必须由程序显式进行强制类型转换。 

#### java反射


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

>问：如果main方法被声明为private会怎样？  
>>答：能正常编译，但运行的时候会提示”main方法不是public的”。
***

<h2 id="2">二、Android</h2>  
### 面试
#### Android开机过程：
* BootLoder引导,然后加载Linux内核.
* 0号进程init启动.加载init.rc配置文件,配置文件有个命令启动了zygote进程
* zygote开始fork出SystemServer进程
* SystemServer加载各种JNI库,然后init1,init2方法,init2方法中开启了新线程ServerThread.
* 在SystemServer中会创建一个socket客户端，后续AMS（ActivityManagerService）会通过此客户端和zygote通信
* ServerThread的run方法中开启了AMS,还孵化新进程ServiceManager,加载注册了一溜的服务,最后一句话进入loop 死循环
run方法的SystemReady调用resumeTopActivityLocked打开锁屏界面

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

<h2 id="3">数据结构</h2>  
堆和栈在内存中的区别是什么(数据结构方面以及实际实现方面)
最快的排序算法是哪个？给阿里2万多名员工按年龄排序应该选择哪个算法？堆和树的区别；写出快排代码；链表逆序代码
求1000以内的水仙花数以及40亿以内的水仙花数
子串包含问题(KMP 算法)写代码实现
万亿级别的两个URL文件A和B，如何求出A和B的差集C,(Bit映射->hash分组->多文件读写效率->磁盘寻址以及应用层面对寻址的优化)
蚁群算法与蒙特卡洛算法
写出你所知道的排序算法及时空复杂度，稳定性
百度POI中如何试下查找最近的商家功能(坐标镜像+R树)

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

<h2 id="5">计算机基础</h2>
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

