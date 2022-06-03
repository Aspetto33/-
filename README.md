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

