# Collection与Map

#### ArrayList、LinkedList、Vector的区别 Map Collection 
首先我们来看一下继承关系：

![这里写图片描述](http://img.blog.csdn.net/20160408150531095)

 - 我们可以看出ArrayList、LinkedList、Vector都实现了List的接口。
        接下来分别看一下三个数据结构的说明。

> public class **ArrayList<E>** extends AbstractList<E>
implements List<E>, RandomAccess, Cloneable, Serializable

>List 接口的**大小可变数组**的实现。实现了所有可选列表操作，并**允许包括 null 在内的所有元素**。除了实现 List 接口外，此类还提供一些方法来操作内部用来存储列表的数组的大小。（此类大致上等同于 Vector 类，除了**此类是不同步的**。）
>
每个 ArrayList 实例都有一个容量。该容量是指用来存储列表元素的数组的大小。它总是至少等于列表的大小。随着向 ArrayList 中不断添加元素，其容量也自动增长。并未指定增长策略的细节，因为这不只是添加元素会带来分摊固定时间开销那样简单。

>在添加大量元素前，应用程序可以使用 ensureCapacity 操作来增加 ArrayList 实例的容量。这可以减少递增式再分配的数量。
>
        List list = Collections.synchronizedList(new ArrayList(...)); 
        
>此类的 iterator 和 listIterator 方法返回的迭代器是快速失败的：在创建迭代器之后，除非通过迭代器自身的 remove 或 add 方法从结构上对列表进行修改，否则在任何时间以任何方式对列表进行修改，迭代器都会抛出 ConcurrentModificationException。因此，面对并发的修改，迭代器很快就会完全失败，而不是冒着在将来某个不确定时间发生任意不确定行为的风险。
注意，迭代器的快速失败行为无法得到保证，因为一般来说，不可能对是否出现不同步并发修改做出任何硬性保证。快速失败迭代器会尽最大努力抛出 ConcurrentModificationException。因此，为提高这类迭代器的正确性而编写一个依赖于此异常的程序是错误的做法：迭代器的快速失败行为应该仅用于检测 bug。

 - 然后是LinkedList
 

> public class **LinkedList**<E>  extends AbstractSequentialList<E>
implements List<E>, Deque<E>, Cloneable, Serializable

>List 接口的链接列表实现。实现所有可选的列表操作，并且允许所有元素（**包括 null**）。除了实现 List 接口外，LinkedList 类还为在列表的开头及结尾 get、remove 和 insert 元素提供了统一的命名方法。这些操作允许将链接列表用作堆栈、队列或双端队列。

>此类实现 Deque 接口，为 add、poll 提供先进先出队列操作，以及其他堆栈和双端队列操作。

>所有操作都是按照**双重链接列表**的需要执行的。在列表中编索引的操作将从开头或结尾遍历列表（从靠近指定索引的一端）。

>注意，此实现**不是同步**的。如果多个线程同时访问一个链接列表，而其中至少一个线程从结构上修改了该列表，则它必须 保持外部同步。（结构修改指添加或删除一个或多个元素的任何操作；仅设置元素的值不是结构修改。）这一般通过**对自然封装该列表的对象进行同步操作来完成**。如果不存在这样的对象，则应该使用 Collections.synchronizedList 方法来“包装”该列表。最好在创建时完成这一操作，以防止对列表进行意外的不同步访问，如下所示：

 >  List list = Collections.synchronizedList(new LinkedList(...));
 >  
此类的 iterator 和 listIterator 方法返回的迭代器是快速失败 的：在迭代器创建之后，如果从结构上对列表进行修改，除非通过迭代器自身的 remove 或 add 方法，其他任何时间任何方式的修改，迭代器都将抛出 ConcurrentModificationException。因此，面对并发的修改，迭代器很快就会完全失败，而不冒将来不确定的时间任意发生不确定行为的风险。

>注意，迭代器的快速失败行为不能得到保证，一般来说，存在不同步的并发修改时，不可能作出任何硬性保证。快速失败迭代器尽最大努力抛出 ConcurrentModificationException。因此，编写依赖于此异常的程序的方式是错误的，正确做法是：迭代器的快速失败行为应该仅用于检测程序错误。

 - 最后是Vector

> public class **Vector**<E> extends AbstractList<E>
implements List<E>, RandomAccess, Cloneable, Serializable

> Vector 类可以**实现可增长的对象数组**。与数组一样，它包含可以使用整数索引进行访问的组件。但是，Vector 的大小可以根据需要增大或缩小，以适应创建 Vector 后进行添加或移除项的操作。

> 每个向量会试图通过维护 capacity 和 capacityIncrement 来优化存储管理。capacity 始终至少应与向量的大小相等；这个值通常比后者大些，因为随着将组件添加到向量中，其存储将按 capacityIncrement 的大小增加存储块。应用程序可以在插入大量组件前增加向量的容量；这样就减少了增加的重分配的量。

> 由 Vector 的 iterator 和 listIterator 方法所返回的迭代器是快速失败的：如果在迭代器创建后的任意时间从结构上修改了向量（通过迭代器自身的 remove 或 add 方法之外的任何其他方式），则迭代器将抛出 ConcurrentModificationException。因此，面对并发的修改，迭代器很快就完全失败，而不是冒着在将来不确定的时间任意发生不确定行为的风险。Vector 的 elements 方法返回的 Enumeration 不是 快速失败的。

> 注意，迭代器的快速失败行为不能得到保证，一般来说，存在不同步的并发修改时，不可能作出任何坚决的保证。快速失败迭代器尽最大努力抛出 ConcurrentModificationException。因此，编写依赖于此异常的程序的方式是错误的，正确做法是：迭代器的快速失败行为应该仅用于检测 bug。

> 从 Java 2 平台 v1.2 开始，此类改进为可以实现 List 接口，使它成为 Java Collections Framework 的成员。与新 collection 实现不同，**Vector 是同步的**。

 - 区别
    

	ArrayList 本质上是一个可改变大小的**数组**.当元素加入时,其大小将会动态地增长.内部的元素可以直接通过get与set方法进行访问.元素顺序存储 ,**随机访问很快，删除非头尾元素慢，新增元素慢而且费资源** ,较适用于无频繁增删的情况 ,比数组效率低，如果不是需要可变数组，可考虑使用数组 ,**非线程安全**.

	LinkedList 是一个**双链表**,在添加和删除元素时具有比ArrayList更好的性能.但在get与set方面弱于ArrayList. 适用于 ：没有大规模的随机读取，大量的增加/删除操作.**随机访问很慢，增删操作很快**，不耗费多余资源 ,允许null元素,**非线程安全.** 

	Vector （类似于ArrayList）但其是**同步**的，开销就比ArrayList要大。如果你的程序本身是线程安全的，那么使用ArrayList是更好的选择。
Vector和ArrayList在更多元素添加进来时会请求更大的空间。Vector每次请求其大小的双倍空间，而ArrayList每次对size增长50%.


#### Collection包结构，与Collections的区别
> Collection家族

![这里写图片描述](http://img.blog.csdn.net/20160408150531095) 



Collection是集合继承结构中的顶层接口

Collections 是提供了对集合进行操作的强大方法的工具类 ，它包含有各种有关集合操作的静态多态方法。此类不能实例化


#### 集合类以及集合框架；HashMap与HashTable实现原理，线程安全性，hash冲突及处理算法；ConcurrentHashMap

http://www.cnblogs.com/yuanermen/archive/2009/08/05/1539917.html 
http://alexyyek.github.io/2015/04/06/Collection/   
http://tianmaying.com/tutorial/java_collection  

#### hashmap和hashtable的区别-乐视-小米

http://www.233.com/ncre2/JAVA/jichu/20100717/084230917.html

#### ArrayMap对比HashMap

http://lvable.com/?p=217


----------------------------------------------
1. 下列说法正确的是（）
A. LinkedList继承自List B. AbstractSet继承自Set C. HashSet继承自AbstractSet D. WeakMap继承自HashMap

答案：AC

解析：下面是一张下载的 Java 中的集合类型的继承关系图，一目了然。


2. ArrayList list = new ArrayList(20);中的 list 扩充几次?
A. 0
B. 1
C. 2
D. 3

答案：A

解析：这里有点迷惑人，大家都知道默认 ArrayList 的长度是 10 个，所以如果你要往 list 里添加 20 个元素肯定要扩充一次（扩充为原来的 1.5 倍），但是这里显示指明了需要多少空间，所以就一次性为你分配这么多空间，也就是不需要扩充了。

3. Java集合类框架的基本接口有哪些？
Java 集合类提供了一套设计良好的支持对一组对象进行操作的接口和类。Java集合类里面最基本的接口有：

Collection：代表一组对象，每一个对象都是它的子元素。

Set：不包含重复元素的 Collection。

List：有顺序的 collection，并且可以包含重复元素。

Map：可以把键(key)映射到值(value)的对象，键不能重复。

4. 为什么集合类没有实现 Cloneable 和 Serializable 接口？
集合类接口指定了一组叫做元素的对象。集合类接口的每一种具体的实现类都可以选择以它自己的方式对元素进行保存和排序。有的集合类允许重复的键，有些不允许。

5. 什么是迭代器(Iterator)？
Iterator 接口提供了很多对集合元素进行迭代的方法。每一个集合类都包含了可以返回迭代器实例的 迭代方法。迭代器可以在迭代的过程中删除底层集合的元素。

克隆(cloning)或者是序列化(serialization)的语义和含义是跟具体的实现相关的。因此，应该由集合类的具体实现来决定如何被克隆或者是序列化。

6. Iterator和ListIterator的区别是什么？
下面列出了他们的区别：

Iterator 可用来遍历 Set 和 List 集合，但是 ListIterator 只能用来遍历 List 。

Iterator 对集合只能是前向遍历，ListIterator 既可以前向也可以后向。

ListIterator 实现了 Iterator 接口，并包含其他的功能，比如：增加元素，替换元素，获取前一个和后一个元素的索引，等等。

7. 快速失败(fail-fast)和安全失败(fail-safe)的区别是什么？
Iterator 的安全失败是基于对底层集合做拷贝，因此，它不受源集合上修改的影响。java.util 包下面的所有的集合类都是快速失败的，而 java.util.concurrent 包下面的所有的类都是安全失败的。快速失败的迭代器会抛出 ConcurrentModificationException 异常，而安全失败的迭代器永远不会抛出这样的异常。

8. Java 中的 HashMap 的工作原理是什么？
Java 中的 HashMap 是以键值对(key-value)的形式存储元素的。HashMap 需要一个hash函数，它使用 hashCode()和 equals()方法来向集合/从集合添加和检索元素。当调用 put()方法的时候，HashMap会计算 key 的 hash 值，然后把键值对存储在集合中合适的索引上。如果 key 已经存在了，value 会被更新成新值。HashMap 的一些重要的特性是它的容量(capacity)，负载因子(load factor)和扩容极限(threshold resizing)。

9. hashCode() 和 equals() 方法的重要性体现在什么地方？
Java 中的 HashMap 使用 hashCode() 和 equals() 方法来确定键值对的索引，当根据键获取值的时候也会用到这两个方法。如果没有正确的实现这两个方法，两个不同的键可能会有相同的 hash 值，因此，可能会被集合认为是相等的。而且，这两个方法也用来发现重复元素。所以这两个方法的实现对 HashMap 的精确性和正确性是至关重要的。

10. HashMap 和 Hashtable 有什么区别？
HashMap 和 Hashtable 都实现了 Map 接口，因此很多特性非常相似。但是，他们有以下不同点： HashMap 允许键和值是 null，而 Hashtable 不允许键或者值是 null。

Hashtable 是同步的，而 HashMap 不是。因此， HashMap 更适合于单线程环境，而 Hashtable 适合于多线程环境。

HashMap 提供了可供应用迭代的键的集合，因此，HashMap 是快速失败的。另一方面，Hashtable 提供了对键的列举(Enumeration)。

一般认为 Hashtable 是一个遗留的类。

11. 数组(Array)和列表(ArrayList)有什么区别？什么时候应该使用 Array 而不是 ArrayList？
下面列出了 Array 和 ArrayList 的不同点：

Array 可以包含基本类型和对象类型，ArrayList 只能包含对象类型。

Array 大小是固定的，ArrayList 的大小是动态变化的。

ArrayList 提供了更多的方法和特性，比如：addAll()，removeAll()，iterator()等等。 对于基本类型数据，集合使用自动装箱来减少编码工作量。但是，当处理固定大小的基本数据类型的时候，这种方式相对比较慢。

12. ArrayList 和 LinkedList 有什么区别？
ArrayList 和 LinkedList 都实现了 List 接口，他们有以下的不同点：

ArrayList 是基于索引的数据接口，它的底层是数组。它可以以O(1)时间复杂度对元素进行随机访问。与此对应，LinkedList 是以元素列表的形式存储它的数据，每一个元素都和它的前一个和后一个元素链接在一起，在这种情况下，查找某个元素的时间复杂度是O(n)。

相对于 ArrayList，LinkedList 的插入，添加，删除操作速度更快，因为当元素被添加到集合任意位置的时候，不需要像数组那样重新计算大小或者是更新索引。

LinkedList 比 ArrayList 更占内存，因为 LinkedList 为每一个节点存储了两个引用，一个指向前一个元素，一个指向下一个元素。

也可以参考 ArrayList vs. LinkedList。

13. Comparable 和Comparator 接口是干什么的？列出它们的区别。
Java 提供了只包含一个 compareTo() 方法的 Comparable 接口。这个方法可以个给两个对象排序。具体来说，它返回负数，0，正数来表明输入对象小于，等于，大于已经存在的对象。

Java 提供了包含 compare() 和 equals() 两个方法的 Comparator 接口。compare() 方法用来给两个输入参数排序，返回负数，0，正数表明第一个参数是小于，等于，大于第二个参数。equals() 方法需要一个对象作为参数，它用来决定输入参数是否和 comparator 相等。只有当输入参数也是一个 comparator 并且输入参数和当前 comparator 的排序结果是相同的时候，这个方法才返回 true。

14. Java集合类框架的最佳实践有哪些？
根据应用的需要正确选择要使用的集合的类型对性能非常重要，比如：假如元素的大小是固定的，而且能事先知道，我们就应该用 Array 而不是 ArrayList。 有些集合类允许指定初始容量。因此，如果我们能估计出存储的元素的数目，我们可以设置初始容量来避免重新计算 hash 值或者是扩容。

为了类型安全，可读性和健壮性的原因总是要使用泛型。同时，使用泛型还可以避免运行时的 ClassCastException。

使用 JDK 提供的不变类(immutable class)作为Map的键可以避免为我们自己的类实现 hashCode() 和 equals() 方法。

编程的时候接口优于实现。

底层的集合实际上是空的情况下，返回长度是0的集合或者是数组，不要返回 null。

15. Enumeration 接口和 Iterator 接口的区别有哪些？
Enumeration 速度是 Iterator 的2倍，同时占用更少的内存。但是，Iterator 远远比 Enumeration 安全，因为其他线程不能够修改正在被 iterator 遍历的集合里面的对象。同时，Iterator 允许调用者删除底层集合里面的元素，这对 Enumeration 来说是不可能的。

16. HashSet 和 TreeSet 有什么区别？
HashSet 是由一个 hash 表来实现的，因此，它的元素是无序的。add()，remove()，contains()方法的时间复杂度是 O(1)。

另一方面，TreeSet 是由一个树形的结构来实现的，它里面的元素是有序的。因此，add()，remove()，contains() 方法的时间复杂度是 O(logn)。

17. List、Set、Map 是否继承自 Collection 接口？
答：List、Set 是，Map 不是。Map 是键值对映射容器，与 List 和 Set 有明显的区别，而 Set 存储的零散的元素且不允许有重复元素（数学中的集合也是如此），List 是线性结构的容器，适用于按数值索引访问元素的情形。

18. 说出 ArrayList、Vector、LinkedList 的存储性能和特性？
答：ArrayList 和 Vector 都是使用数组方式存储数据，此数组元素数大于实际存储的数据以便增加和插入元素，它们都允许直接按序号索引元素，但是插入元素要涉及数组元素移动等内存操作，所以索引数据快而插入数据慢，Vector 由于使用了 synchronized 方法（线程安全），通常性能上较 ArrayList 差，而 LinkedList 使用双向链表实现存储（将内存中零散的内存单元通过附加的引用关联起来，形成一个可以按序号索引的线性结构，这种链式存储方式与数组的连续存储方式相比，其实对内存的利用率更高），按序号索引数据需要进行前向或后向遍历，但是插入数据时只需要记录本项的前后项即可，所以插入速度较快。

Vector 属于遗留容器（早期的 JDK 中使用的容器，除此之外 Hashtable、Dictionary、BitSet、Stack、Properties 都是遗留容器），现在已经不推荐使用，但是由于 ArrayList 和 LinkedListed 都是非线程安全的，如果需要多个线程操作同一个容器，那么可以通过工具类 Collections 中的 synchronizedList 方法将其转换成线程安全的容器后再使用（这其实是装潢模式最好的例子，将已有对象传入另一个类的构造器中创建新的对象来增加新功能）。

19. List、Map、Set 三个接口存储元素时各有什么特点？
答：

1）List 是有序的 Collection，使用此接口能够精确的控制每个元素插入的位置。用户能够使用索引（元素在 List 中的位置，类似于数组下标）来访问 List 中的元素，这类似于 Java 的数组。

2）Set 是一种不包含重复的元素的 Collection，即任意的两个元素 e1 和 e2 都有e1.equals(e2)=false，Set 最多有一个 null 元素。

3）Map 接口 ：请注意，Map 没有继承 Collection 接口，Map 提供 key 到 value 的映射

20. 判断下列语句是否正确，如果有错误，请指出错误所在？
List a = new ArrayList();

a.add(5);

答：错误,默认封装 int 类型。

21. 你是怎么理解 Java 泛型的？
答： 在 Java SE 1.5之前，没有泛型的情况的下，通过对类型 Object 的引用来实现参数的“任意化”，“任意化”带来的缺点是要做显式的强制类型转换，而这种转换是要求开发者对实际参数类型可以预知的情况下进行的。对于强制类型转换错误的情况，编译器可能不提示错误，在运行的时候才出现异常，这是一个安全隐患。

泛型是 Java SE 1.5的新特性，泛型的本质是参数化类型，也就是说所操作的数据类型被指定为一个参数。这种参数类型可以用在类、接口和方法的创建中，分别称为泛型类、泛型接口、泛型方法。

泛型的好处是在编译的时候检查类型安全，并且所有的强制转换都是自动和隐式的，提高代码的重用率。