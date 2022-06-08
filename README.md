# 数据结构学习笔记
## 1 基本概念和术语

![数据关系图](https://github.com/Aspetto33/data-structure/blob/master/images/1-3/%E6%95%B0%E6%8D%AE%E5%85%B3%E7%B3%BB%E5%9B%BE.png)

### 1.1 数据

数据包括整型、实型等数值类型，还包括字符、声音、图像、视频等非数值类型。

### 1.2 数据元素

组成数据的、有一定意义的基本单位，通常作为整体处理，也称为记录。例如在人类中的数据元素是人。

### 1.3 数据项

一个数据元素可以由若干个数据项组成。例如人可以有眼耳鼻喉等。数据项是数据不可分割的最小单位。

### 1.4 数据对象

性质相同的数据元素的集合，是数据的子集。例如人都有姓名、生日、性别等相同的数据项。

### 1.5 数据结构

相互之间存在一种或多种特定关系的数据元素的集合。

## 2 逻辑结构和物理结构

![数据结构图](https://github.com/Aspetto33/data-structure/blob/master/images/1-3/%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84%E5%9B%BE.png)

### 2.1 逻辑结构

数据对象中数据元素之间的相互关系。逻辑结构包括：

1）集合结构

集合结构中的数据元素除了同属于一个集合外，没有其他任何关系，如下图：

![集合结构图](https://github.com/Aspetto33/data-structure/blob/master/images/1-3/%E9%9B%86%E5%90%88%E7%BB%93%E6%9E%84%E5%9B%BE.png)

2）线性结构

数据元素关系是一对一的，如下图：

![线性结构图](https://github.com/Aspetto33/data-structure/blob/master/images/1-3/%E7%BA%BF%E6%80%A7%E7%BB%93%E6%9E%84%E5%9B%BE.png)

3）树形结构

一对多的层次关系，如下图：

![树形结构图](https://github.com/Aspetto33/data-structure/blob/master/images/1-3/%E6%A0%91%E5%BD%A2%E7%BB%93%E6%9E%84%E5%9B%BE.png)

4）图形结构

多对多的关系，如下图：

![图形结构图](https://github.com/Aspetto33/data-structure/blob/master/images/1-3/%E5%9B%BE%E5%BD%A2%E7%BB%93%E6%9E%84%E5%9B%BE.png)

### 2.2 物理结构

数据的逻辑结构在计算机中的存储形式。

1）顺序存储结构

把数据元素存放在地址连续的存储单元里，数据见的逻辑关系和物理关系是一致的。例如数组。

![顺序存储结构图](https://github.com/Aspetto33/data-structure/blob/master/images/1-3/%E9%A1%BA%E5%BA%8F%E5%AD%98%E5%82%A8%E7%BB%93%E6%9E%84%E5%9B%BE.png)

2）链式存储结构

把数据元素存放在任意的存储单元里，这组存储单元是可以连续的，也可以是不连续的。因为数据元素的存储关系并不能反映其逻辑关系，因此需要使用指针存放数据元素的地址。

![链式存储结构图](https://github.com/Aspetto33/data-structure/blob/master/images/1-3/%E9%93%BE%E5%BC%8F%E5%AD%98%E5%82%A8%E7%BB%93%E6%9E%84%E5%9B%BE.png)

## 3 抽象数据类型

### 3.1 数据类型

一组性质相同的值的集合及定义在此集合上的一些操作的总称。在C语言中，按照取值的不同，数据类型可以分为两类：

1）原子类型

不可分解，包括整型、实型、字符型。

2）结构类型

由若干个类型组合而成，可再分解。例如整型数组。

### 3.2 抽象数据类型

指一个数学模型及定义在该模型上的一组操作。

## 4 算法

### 4.1 算法定义

描述解决问题的方法。

### 4.2 算法特性

具有五个基本特性：输入、输出、有穷性、确定性和可行性。

1）输入输出

算法具有0个或多个输入，但一定有输出，可以是打印值也可以是返回值。

2）有穷性

指算法在执行有限的步骤之后，自动结束而不会出现无限循环，并且每一个步骤在可接受的时间内完成。

3）确定性

算法的每一步骤都具有确定的含义，不会出现二义性。

4）可行性

算法的每一步都必须是可行的，即每一步都能够通过执行有限次数完成。

### 4.3 算法设计要求

1）正确性

算法至少应该具有输入、输出和加工处理无歧义性，能正确反映问题的需求，能够得到问题的正确答案。

2）可读性

便于阅读、理解和交流。

3）健壮性

当输入数据不合法时，算法也能做出相关处理，而不是产生异常或莫名其妙的结果。

4）时间效率高和存储量低

时间花费少，占用存储空间低。

### 4.4 算法效率的度量方法

1）事后统计方法

通过设计好的测试程序和数据，利用计算机计时器对不同算法编译的程序的运行时间进行比较，从而确定算法效率的高低。但是有很大缺陷：

- 必须依据算法事先编译好程序
- 时间的比较依赖于计算机硬件和软件等环境因素
- 算法的测试数据设计困难

2）事前分析估算方法

在计算机程序编译前依据统计方法对算法进行估算

### 4.5 函数的渐进增长

给定两个函数f（n）和g（n），如果存在一个整数N，使得对于所有的n>N，f（n）总是比g（n）大，那么，我们说f（n）的增长渐近快于g（n）。

结论：判断一个算法的效率时，函数中的常数和其他次要项常常可以忽略，而更应该关注主项（最高阶项）的阶数。

### 4.6 算法时间复杂度

1）算法时间复杂度定义

T（n）=O（f（n））。表示随问题规模n的增大，算法执行时间的增长率和f（n）的增长率相同，称作算法的渐近时间复杂度，简称为时间复杂度。其中f（n）是问题规模n的某个函数。

2）推导大O阶方法

- 用常数1取代运行时间中的所有加法常数
- 在修改后的运行次数函数中，只保留最高阶项
- 如果最高阶项存在且不是1，则去除与这个项相乘的常数

3）常数阶

无论常数是几，统统计为O（1）

![常数阶](https://github.com/Aspetto33/data-structure/blob/master/images/4/%E5%B8%B8%E6%95%B0%E9%98%B6.png)

4）线性阶

分析算法的复杂度，关键就是要分析循环结构的运行情况。O（n）

![线性阶](https://github.com/Aspetto33/data-structure/blob/master/images/4/%E7%BA%BF%E6%80%A7%E9%98%B6.png)

5）对数阶

![对数阶](https://github.com/Aspetto33/data-structure/blob/master/images/4/%E5%AF%B9%E6%95%B0%E9%98%B6.png)

6）平方阶

![平方阶](https://github.com/Aspetto33/data-structure/blob/master/images/4/%E5%B9%B3%E6%96%B9%E9%98%B6.png)

### 4.7 常见的时间复杂度

![常见时间复杂度](https://github.com/Aspetto33/data-structure/blob/master/images/4/%E5%B8%B8%E8%A7%81%E6%97%B6%E9%97%B4%E5%A4%8D%E6%9D%82%E5%BA%A6.png)

常见时间复杂度排序如下图：

![时间复杂度排序](https://github.com/Aspetto33/data-structure/blob/master/images/4/%E6%97%B6%E9%97%B4%E5%A4%8D%E6%9D%82%E5%BA%A6%E6%8E%92%E5%BA%8F.png)

### 4.8 最坏情况与平均情况

最坏情况运行时间是一种保证，那就是运行时间将不会再坏了。在应用中，这是一种最重要的需求，通常，除非特别指定，提到的运行时间都是最坏情况的运行时间。

平均运行时间是所有情况中最有意义的，因为他是期望的运行时间。

### 4.9 算法空间复杂度

算法的空间复杂度通过计算算法所需的存储空间实现，算法空间复杂度的计算公式记作：s（n）=O（f（n））。其中，n为问题的规模，f（n）为语句关于n所占存储空间的函数。

## 5 线性表

零个或者多个数据元素的有限序列

### 5.1 线性表的定义

首先线性表是一个序列，即元素之间是有顺序的，若元素存在多个，则第一个元素无前驱，最后一个元素无后继，其他每个元素都有且只有一个前驱和后继。然后，线性表强调有限。

![线性表数学定义](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E7%BA%BF%E6%80%A7%E8%A1%A8%E6%95%B0%E5%AD%A6%E5%AE%9A%E4%B9%89.png)

线性表元素的个数n（n>0）定义为线性表的长度，当n=0时，称为空表。

### 5.2 线性表的抽象数据类型

线性表的抽象数据类型定义如下图：

![线性表抽象数据类型定义](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E7%BA%BF%E6%80%A7%E8%A1%A8%E6%8A%BD%E8%B1%A1%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B%E5%AE%9A%E4%B9%89.png)

### 5.3 线性表的顺序存储结构

1）顺序存储定义

用一段地址连续的存储单元依次存储线性表的数据元素。

2）顺序存储方式

因为线性表的每个数据元素的类型都相同，所以可以用C语言的一维数组来实现顺序存储结构。如下图：

![线性表顺序存储图](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E7%BA%BF%E6%80%A7%E8%A1%A8%E9%A1%BA%E5%BA%8F%E5%AD%98%E5%82%A8%E5%9B%BE.png)

3）数据长度与线性表长度区别

数组长度时存放线性表的存储空间的长度。线性表的长度是线性表中数据元素的个数，随着线性表插入和删除操作的进行，这个量是变化的。在任意时刻，线性表的长度应该小于等于数组的长度。

4）地址计算方法

数据元素的序号和存放它的数组下标之间存在对应关系如下图所示：

![数据元素符号和数组下标关系](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E6%95%B0%E6%8D%AE%E5%85%83%E7%B4%A0%E5%BA%8F%E5%8F%B7%E4%B8%8E%E6%95%B0%E7%BB%84%E4%B8%8B%E6%A0%87%E5%85%B3%E7%B3%BB.png)

### 5.4 顺序存储结构的插入与删除

1）获得元素操作

![线性表获得元素代码](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E7%BA%BF%E6%80%A7%E8%A1%A8%E8%8E%B7%E5%BE%97%E5%85%83%E7%B4%A0%E4%BB%A3%E7%A0%81.png)

2）插入操作

![线性表插入元素代码](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E7%BA%BF%E6%80%A7%E8%A1%A8%E6%8F%92%E5%85%A5%E5%85%83%E7%B4%A0%E4%BB%A3%E7%A0%81.png)

3）删除操作

![线性表删除元素代码](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E7%BA%BF%E6%80%A7%E8%A1%A8%E5%88%A0%E9%99%A4%E5%85%83%E7%B4%A0%E4%BB%A3%E7%A0%81.png)

4）线性表顺序存储结构的优缺点

优点：无须为表示表中元素之间的逻辑关系而增加额外的存储空间，可以快速地存取表中任一位置的元素。

缺点：插入和删除操作需要移动大量元素，当线性表长度变化较大，难以确定存储空间的容量，造成存储空间的“碎片”。

![线性表顺序存储结构优缺点](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E7%BA%BF%E6%80%A7%E8%A1%A8%E9%A1%BA%E5%BA%8F%E5%AD%98%E5%82%A8%E7%BB%93%E6%9E%84%E4%BC%98%E7%BC%BA%E7%82%B9%20.png)

### 5.5 线性表的链式存储结构

1）顺序存储结构不足的解决办法

线性表的顺序存储结构有缺点是插入和删除时需要移动大量元素，显然就需要消耗时间，解决方法时使用链式存储结构

2）线性表链式存储结构定义

链式存储结构的特点是用一组任意的存储单元存储线性表的数据元素，这组存储单元可以是连续的，也可以是不连续的。

为了表示每个数据元素ai与其直接后继数据元素ai+1之间的逻辑关系，对数据元素ai来说，除了存储其本身的信息之外，还需存储一个指示其直接后继的信息。

把存储数据元素信息的域称为指针域。指针域中存储的信息称作指针或者链。这两部分组成数据元素ai的存储映像，称为结点（Node）。

把链表中的第一个结点的存储位置叫做头指针，线性链表的最后一个结点指针为“空”，通常用NULL或“^‘符号表示。为了方便对链表进行操作，会在链表的第一个结点前附设一个结点，称为头结点。头结点的数据域可以不存储任何信息。

![线性表链式存储结构图](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E7%BA%BF%E6%80%A7%E8%A1%A8%E9%93%BE%E5%BC%8F%E5%AD%98%E5%82%A8%E7%BB%93%E6%9E%84%E5%9B%BE.png)

3）头指针和头结点的异同

![头指针和头结点的异同](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E5%A4%B4%E6%8C%87%E9%92%88%E5%92%8C%E5%A4%B4%E7%BB%93%E7%82%B9%E7%9A%84%E5%BC%82%E5%90%8C.png)

4）线性表链式存储结构代码描述

若线性表为空表，则头结点的指针域为空，空链表如下图所示：

![空链表](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E7%A9%BA%E9%93%BE%E8%A1%A8.png)

不带头结点的单链表如下图所示：

![不带头结点的单链表存储示意图](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E4%B8%8D%E5%B8%A6%E5%A4%B4%E7%BB%93%E7%82%B9%E7%9A%84%E5%8D%95%E9%93%BE%E8%A1%A8%E5%AD%98%E5%82%A8%E7%A4%BA%E6%84%8F%E5%9B%BE.png)

带头结点的单链表如下图所示：

![带头结点的单链表存储示意图](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E5%B8%A6%E5%A4%B4%E7%BB%93%E7%82%B9%E7%9A%84%E5%8D%95%E9%93%BE%E8%A1%A8%E5%AD%98%E5%82%A8%E7%A4%BA%E6%84%8F%E5%9B%BE.png)

由结构定义可以看出结点由存放数据元素的数据域存放后继结点地址的指针域组成。

5.6 单链表的读取

思路：

- 声明一个结点p指向链表第一个结点，初始化j从1开始
- 当j<i时，就遍历链表，让p的指针向后移动，不断指向下一结点，j累加1
- 若到链表末尾p为空，则说明第i个元素不存在
- 否则查找成功，返回结点p的数据。

![单链表查找元素代码](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E5%8D%95%E9%93%BE%E8%A1%A8%E6%9F%A5%E6%89%BE%E5%85%83%E7%B4%A0%E4%BB%A3%E7%A0%81.png)

### 5.7 单链表的插入与删除

1）单链表的插入

思路：

- 声明一结点p指向链表第一个结点，初始化j从1开始
- 当j<i时，就遍历链表，让p的指针向后移动，不断指向下一结点，j累加1
- 若到链表末尾p为空，则说明第i个元素不存在
- 否则查找成功，在系统中生成一个空结点s
- 将数据元素e赋值给s->data
- 单链表的插入标准语句s->next = p->next p->next = s
- 返回成功

![单链表插入元素代码](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E5%8D%95%E9%93%BE%E8%A1%A8%E6%8F%92%E5%85%A5%E5%85%83%E7%B4%A0%E4%BB%A3%E7%A0%81.png)

2）单链表的删除

思路：

- 声明一结点p指向链表第一个结点，初始化j从1开始
- 当j<i时，就遍历链表，让p的指针向后移动，不断指向下一个结点，j累加1
- 若到链表末尾p为空，则说明第i个元素不存在
- 否则查找成功，将欲删除的结点p->next赋给q
- 单链表的删除标准语句p->next = q->next
- 将q结点中的数据赋值给e作为返回
- 释放q结点
- 返回成功

![单链表删除元素代码](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E5%8D%95%E9%93%BE%E8%A1%A8%E5%88%A0%E9%99%A4%E5%85%83%E7%B4%A0%E4%BB%A3%E7%A0%81.png)

5.8 单链表的整表创建

头插法思路：

- 声明一结点p和计数器变量i

- 初始化一空链表L

- 让L的头结点的指针指向NULL，再建立一个带头结点的单链表

- 循环：

  - 生成一新结点赋值给p

  - 随机生成一数字赋值给p的数据域p->data

  - 将p插入到头结点与前一新结点之间

![头插法生成整个链表代码](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E5%A4%B4%E6%8F%92%E6%B3%95%E7%94%9F%E6%88%90%E6%95%B4%E4%B8%AA%E9%93%BE%E8%A1%A8%E4%BB%A3%E7%A0%81.png)

尾插法思路：

每次把新结点插在终端结点的后面

![尾插法生成整个链表代码](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E5%B0%BE%E6%8F%92%E6%B3%95%E7%94%9F%E6%88%90%E6%95%B4%E4%B8%AA%E9%93%BE%E8%A1%A8%E4%BB%A3%E7%A0%81.png)

### 5.9 单链表的整表删除

思路：

- 声明一结点p和q
- 将第一个结点赋值给p
- 循环：
  - 将下一结点赋值给q
  - 释放p
  - 将q赋值给p

![单链表整表删除代码](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E5%8D%95%E9%93%BE%E8%A1%A8%E6%95%B4%E8%A1%A8%E5%88%A0%E9%99%A4%E4%BB%A3%E7%A0%81.png)

### 5.10 单链表结构与顺序存储结构优缺点

![单链表结构与顺序存储结构优缺点](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E5%8D%95%E9%93%BE%E8%A1%A8%E7%BB%93%E6%9E%84%E4%B8%8E%E9%A1%BA%E5%BA%8F%E5%AD%98%E5%82%A8%E7%BB%93%E6%9E%84%E4%BC%98%E7%BC%BA%E7%82%B9.png)

经验性结论：

若线性表需要频繁查找，很少进行插入和删除操作时，宜采用顺序存储结构。

若需要频繁插入和删除时，宜采用单链表结构

当线性表中的元素个数变化较大或根本不知道有多大时，最好用单链表结构，这样可以不用考虑存储空间的大小问题。

如果事先知道线性表的大致长度，则用顺序存储结构的效率会高很多。

### 5.11 静态链表

用数组描述的链表叫做静态链表，也可以叫做游标实现法。

![静态链表存储结构](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E9%9D%99%E6%80%81%E9%93%BE%E8%A1%A8%E5%AD%98%E5%82%A8%E7%BB%93%E6%9E%84.png)

个人理解：每一个元素存放下一个元素的下标，最后一个存放元素的位置因为下面已经没有元素，所以存0。

数组第一个位置存放第一个空闲位置的下标，最后一个位置存放第一个元素的下标。

静态链表初始化如下图所示：

![静态链表初始化代码](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E9%9D%99%E6%80%81%E9%93%BE%E8%A1%A8%E5%88%9D%E5%A7%8B%E5%8C%96%E4%BB%A3%E7%A0%81.png)

1）静态链表的插入操作

要解决的是如何用静态模拟动态链表结构的存储空间的分配，需要时申请，无用时释放。

申请结点代码如下图所示：

![静态链表申请结点代码](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E9%9D%99%E6%80%81%E9%93%BE%E8%A1%A8%E7%94%B3%E8%AF%B7%E7%BB%93%E7%82%B9%E4%BB%A3%E7%A0%81.png)

插入元素代码如下图所示：

![静态链表插入元素代码](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E9%9D%99%E6%80%81%E9%93%BE%E8%A1%A8%E6%8F%92%E5%85%A5%E5%85%83%E7%B4%A0%E4%BB%A3%E7%A0%81.png)

2）静态链表的删除操作

释放结点代码如下图所示：

![静态链表释放结点代码](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E9%9D%99%E6%80%81%E9%93%BE%E8%A1%A8%E9%87%8A%E6%94%BE%E7%BB%93%E7%82%B9%E4%BB%A3%E7%A0%81.png)

删除元素代码如下图所示：

![静态链表删除元素代码](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E9%9D%99%E6%80%81%E9%93%BE%E8%A1%A8%E5%88%A0%E9%99%A4%E5%85%83%E7%B4%A0%E6%93%8D%E4%BD%9C.png)

3）静态链表优缺点

![静态链表优缺点](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E9%9D%99%E6%80%81%E9%93%BE%E8%A1%A8%E4%BC%98%E7%BC%BA%E7%82%B9.png)

### 5.12 循环链表

将单链表中终端结点的指针端由空指针改为指向头结点，使得整个单链表形成一个环，这种头尾相接的单链表称为单循环链表，简称循环链表。

空循环链表如下图所示：

![空循环链表](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E7%A9%BA%E5%BE%AA%E7%8E%AF%E9%93%BE%E8%A1%A8.png)

非空循环链表如下图所示：

![非空循环链表](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E9%9D%9E%E7%A9%BA%E5%BE%AA%E7%8E%AF%E9%93%BE%E8%A1%A8.png)

循环链表和单链表的主要差异在于循环的判断条件上。单链表判断p->next为空则结束，循环链表判断p->next等于头结点则结束。

### 5.13 双向链表

双向链表是在单链表的每个结点中，再设置一个指向其前驱结点的指针域。所以在双向链表中的结点都有两个指针域，一个指向直接后继，另一个指向直接前驱。

双向链表循环带头结点的空链表如下图所示：

![双向链表循环带头结点的空链表](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E5%8F%8C%E5%90%91%E9%93%BE%E8%A1%A8%E5%BE%AA%E7%8E%AF%E5%B8%A6%E5%A4%B4%E7%BB%93%E7%82%B9%E7%9A%84%E7%A9%BA%E9%93%BE%E8%A1%A8.png)

非空循环带头结点的双向链表如下图所示：

![非空循环带头结点的双向链表](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E9%9D%9E%E7%A9%BA%E5%BE%AA%E7%8E%AF%E5%B8%A6%E5%A4%B4%E7%BB%93%E7%82%B9%E7%9A%84%E5%8F%8C%E5%90%91%E9%93%BE%E8%A1%A8.png)

双向链表插入元素顺序为：

先搞定插入元素的前驱和后继，再搞定后边元素的前驱，最后搞定前面元素的后继。

![双向链表插入元素](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E5%8F%8C%E5%90%91%E9%93%BE%E8%A1%A8%E6%8F%92%E5%85%A5%E5%85%83%E7%B4%A0.png)

双向链表删除元素顺序为：

先把前面元素的后继连接到后面元素上，再把后面元素的前驱连接到前面元素上。

![双向链表删除元素](https://github.com/Aspetto33/data-structure/blob/master/images/5/%E5%8F%8C%E5%90%91%E9%93%BE%E8%A1%A8%E5%88%A0%E9%99%A4%E5%85%83%E7%B4%A0.png)

## 6 栈与队列

### 6.1 栈的定义

1）栈的定义

栈是限定仅在表尾进行插入和删除操作的线性表。把允许插入和删除的一端称为栈顶，另一端称为栈底，不包含任何数据元素的栈称为空栈。栈又称为后进先出的线性表，简称LIFO结构。

栈的插入操作，叫做进栈，也称压栈、入栈

栈的删除操作，叫做出栈，也叫做弹栈

2）进栈出栈变化形式

栈对线性表的插入和删除的位置进行了限制，并没有对元素进出的时间进行限制。即，在不是所有元素都进栈的情况下，事先进去的元素也可以出栈。

![123出栈次序](https://github.com/Aspetto33/data-structure/blob/master/images/6/123%E5%87%BA%E6%A0%88%E6%AC%A1%E5%BA%8F.png)

### 6.2 栈的抽象数据类型

![栈的抽象数据类型](https://github.com/Aspetto33/data-structure/blob/master/images/6/%E6%A0%88%E7%9A%84%E6%8A%BD%E8%B1%A1%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B.png)

### 6.3 栈的顺序存储结构及实现

1）栈的顺序存储结构

![栈的结构定义](https://github.com/Aspetto33/data-structure/blob/master/images/6/%E6%A0%88%E7%9A%84%E7%BB%93%E6%9E%84%E5%AE%9A%E4%B9%89.png)

栈的各个情况如下图：

![栈情况图](https://github.com/Aspetto33/data-structure/blob/master/images/6/%E6%A0%88%E6%83%85%E5%86%B5%E5%9B%BE.png)

2）栈的顺序存储结构-进栈操作

![进栈操作图](https://github.com/Aspetto33/data-structure/blob/master/images/6/%E8%BF%9B%E6%A0%88%E6%93%8D%E4%BD%9C%E5%9B%BE.png)

![进栈操作代码](https://github.com/Aspetto33/data-structure/blob/master/images/6/%E8%BF%9B%E6%A0%88%E6%93%8D%E4%BD%9C%E4%BB%A3%E7%A0%81.png)

3）栈的顺序存储结构-出栈操作

![出栈操作代码](https://github.com/Aspetto33/data-structure/blob/master/images/6/%E5%87%BA%E6%A0%88%E6%93%8D%E4%BD%9C%E4%BB%A3%E7%A0%81.png)

### 6.4 两栈共享空间

![两栈共享空间图](https://github.com/Aspetto33/data-structure/blob/master/images/6/%E4%B8%A4%E6%A0%88%E5%85%B1%E4%BA%AB%E5%9B%BE.png)

![两栈共享空间结构代码](https://github.com/Aspetto33/data-structure/blob/master/images/6/%E4%B8%A4%E6%A0%88%E5%85%B1%E4%BA%AB%E7%A9%BA%E9%97%B4%E7%BB%93%E6%9E%84%E4%BB%A3%E7%A0%81.png)

![两栈共享空间进栈代码](https://github.com/Aspetto33/data-structure/blob/master/images/6/%E4%B8%A4%E6%A0%88%E5%85%B1%E4%BA%AB%E7%A9%BA%E9%97%B4%E8%BF%9B%E6%A0%88%E4%BB%A3%E7%A0%81.png)

![两栈共享空间出栈代码](https://github.com/Aspetto33/data-structure/blob/master/images/6/%E4%B8%A4%E6%A0%88%E5%85%B1%E4%BA%AB%E7%A9%BA%E9%97%B4%E5%87%BA%E6%A0%88%E4%BB%A3%E7%A0%81.png)

### 6.5 栈的链式存储结构及实现

1）栈的链式存储结构

![栈的链式存储结构图](https://github.com/Aspetto33/data-structure/blob/master/images/6/%E6%A0%88%E7%9A%84%E9%93%BE%E5%BC%8F%E5%AD%98%E5%82%A8%E7%BB%93%E6%9E%84%E5%9B%BE.png)

![链栈结构代码](https://github.com/Aspetto33/data-structure/blob/master/images/6/%E9%93%BE%E6%A0%88%E7%BB%93%E6%9E%84%E4%BB%A3%E7%A0%81.png)

2）栈的链式存储结构-进栈操作

![链式存储进栈代码](https://github.com/Aspetto33/data-structure/blob/master/images/6/%E9%93%BE%E5%BC%8F%E5%AD%98%E5%82%A8%E8%BF%9B%E6%A0%88%E4%BB%A3%E7%A0%81.png)

3）栈的链式存储结构-出栈操作

![链式存储出栈代码](https://github.com/Aspetto33/data-structure/blob/master/images/6/%E9%93%BE%E5%BC%8F%E5%AD%98%E5%82%A8%E5%87%BA%E6%A0%88%E4%BB%A3%E7%A0%81.png)

如果栈的使用过程中元素变化不可预料，有时很小，有时很大，最好是使用链栈。反之，如果他的变化在可控范围内，用顺序栈较好一点。

### 6.6 栈的应用-递归

1）斐波那契数列实现

![斐波那契数列递归代码](https://github.com/Aspetto33/data-structure/blob/master/images/6/%E6%96%90%E6%B3%A2%E9%82%A3%E5%A5%91%E6%95%B0%E5%88%97%E9%80%92%E5%BD%92%E4%BB%A3%E7%A0%81.png)

2）递归定义

把一个直接调用自己或通过一系列的调用语句间接地调用自己的函数，称作递归函数。为防止递归程序陷入永不结束的无穷递归中，每个递归定义必须至少有一个条件，满足条件时递归不再进行，即不再引用自身而是返回值退出。

### 6.7 栈的应用-四则运算表达式求值

1）后缀（逆波兰）表示法定义

叫后缀的原因在于所有的符号都是在要运算数字的后面出现

2）后缀表达式计算结果

规则：从左到右遍历表达式的每个数字和符号，遇到是数字就进栈，遇到是符号，就将处于栈顶两个数字出栈，进行运算，运算结果进栈，直到最终获得结果。

3）中缀表达式转后缀表达式

“9+（3-1）x3+10/2”->”9 3 1 -3*+10 2 / +“

规则：从左到右遍历中缀表达式的每个数字和符号，若是数字就输出，即成为后缀表达式的一部分；若是符号，则判断其与栈顶符号的优先级，是右括号或优先级低于栈顶符号（乘除优先加减）则栈顶元素依次出栈并输出，并将当前符号进栈，一直到最终输出后缀表达式为止。
