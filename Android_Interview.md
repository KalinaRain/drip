# Android面试知识点（整理中）  

>转眼间学习Android已经有3年了，再加上最近要找工作，所以想着把Android面试的各种知识点总结并整理一下，也算是对这一段时间的付出做个总结。  
>要找一份好工作，自然要对Android，Java，数据结构，算法，计算机基础等知识点都非常熟悉，除此之外还要注重细节，如果你已经经历过一些大公司的面试，相信你已经知道了细节的重要性。

我会持续更新的，欢迎watch

***

## 目录  
[一、Java](#1)  

[二、Android](#2)  

[三、数据结构](#3)  

[四、算法](#4)  

[五、计算机基础](#5)  


<h2 id="1">一、Java</h2>

ArrayList、LinkedList、Vector的区别 Map Collection 

Collection包结构，与Collections的区别

Excption与Error包结构,OOM和SOF

HashMap和HashTable的区别

HashMap源码分析

Hashcode的作用

Map、Set、List、Queue、Stack的特点与用法

Object有哪些公用方法？

Override和Overload的使用规则和区别

Switch能否用string做参数？

ThreadLocal的使用规则和源码分析

ThreadPool用法与示例

equals与==的区别

try catch finally，try里有return，finally还执行么？

九种基本数据类型的大小，以及他们的封装类

从源码分析String、StringBuffer与StringBuilder区别和联系

多线程下生产者消费者问题的五种同步方法实现

实现多线程的两种方法

接口（Interface）与 抽象类 （Abstract）使用规则和区别

方法锁、对象锁和类锁的意义和区别

四种引用，强弱软虚，用到的场景

线程同步的方法：sychronized、lock、reentrantLock分析

集合框架的层次结构和使用规则梳理

面向对象的三个特征与含义

static的作用和意义

多态实现的JVM调用过程

wait()和sleep()的区别

git命令使用

Java与C++对比
java反射

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

<h2 id="2">二、Android</h2>  

Activity 与Fragment（生命周期，四种启动模式）

Android 名企面试题及答案整理（一）
生命周期：
电话打进来：
home键：
消息处理机制
Binder
AIDL
VIew绘制
事件分发机制
常用设计模式
jvm
GC
### 产品架构 MVP MVC MVVM
### Android中设计模式的应用与Android 源码中的设计模式

### 性能优化

### 源码分析
内存泄露
进程保活
AsyncTask

Service全面总结

IntentService使用详解和实例介绍

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

性能优化
启动加速
布局性能优化(include, viewstub, merge)
OOM
电量

XML解析（DOM、SAX、Pull的区别和优缺点）



<h2 id="3">数据结构</h2>  

<h2 id="4">算法</h2>
>对于算法，本人一直认为这是个很高大上的东西，而且事实上他也确实很高大上，如果真的要想提升自己的算法水平，最好是去刷题，单纯的看别人的博客，效果不是很大。目前比较出名的算法刷题网站（online judge）有[lintcode](http://www.lintcode.com/zh-cn/)、 [leetcode](https://leetcode.com/)、 [hihocoder](http://hihocoder.com/)，以及各大高校的网站[参考](http://www.cnblogs.com/Xredman/archive/2009/03/23/1420015.html)。

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
http://www.devstore.cn/essay/essayInfo/7195.html
https://www.diycode.cc/topics/165
http://mp.weixin.qq.com/s?__biz=MzI0MjE3OTYwMg==&mid=2649548612&idx=1&sn=8e46b6dd47bd8577a5f7098aa0889098&chksm=f1180c39c66f852fd955a29a9cb4ffa9dc4d528cab524059bcabaf37954fa3f04bc52c41dae8&scene=21#wechat_redirect
http://mp.weixin.qq.com/s?__biz=MzI0MjE3OTYwMg==&mid=401462221&idx=1&sn=dda1f3500c993d643dcdae6dd2cc3d6f&scene=21#wechat_redirect
http://mp.weixin.qq.com/s?__biz=MzI0MjE3OTYwMg==&mid=2649547668&idx=1&sn=b2667c46188c6674c90aa72c2fba4719&scene=21#wechat_redirect
http://mp.weixin.qq.com/s?__biz=MzI0MjE3OTYwMg==&mid=2649547696&idx=1&sn=e0694067af35df118c4e949a238719f0&scene=21#wechat_redirect
http://blog.csdn.net/sinat_35512245/article/details/59056120

https://github.com/GeniusVJR/LearningNotes
https://github.com/GeniusVJR/LearningNotes/blob/master/Part1/Android/Zygote%E5%92%8CSystem%E8%BF%9B%E7%A8%8B%E7%9A%84%E5%90%AF%E5%8A%A8%E8%BF%87%E7%A8%8B.md
https://github.com/GeniusVJR/LearningNotes/blob/master/Part1/Android/Binder%E6%9C%BA%E5%88%B6.md
https://github.com/GeniusVJR/LearningNotes/blob/master/Part1/Android/AIDL.md
https://github.com/GeniusVJR/LearningNotes/blob/master/Part6/InterviewExperience/%E7%BE%8E%E5%9B%A2.md
http://mp.weixin.qq.com/s?__biz=MzI2OTQxMTM4OQ==&mid=2247484286&idx=1&sn=e5843fb79d8a36ab063699b5fb9a0711&chksm=eae1f62cdd967f3a576396f8402581326b835b8327ed5f20f23896fcd22c2115e77863b4115b#rd
http://blog.tingyun.com/web/article/detail/155
http://www.jianshu.com/p/89f19d67b348
http://www.trinea.cn/android/java-annotation-android-open-source-analysis/
http://www.tuicool.com/articles/QB73eyf
https://gist.github.com/errord/7801466

<h2 id="5">计算机基础</h2>
Http TCP/IP 