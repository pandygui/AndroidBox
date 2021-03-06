### 一、定义
 可以将一个类定义到另一个类的内部，这个类就是内部类；

### 二、分类
#### 1、内部类（内部类对象和外部类对象存在必然的联系）
+ 内部类拥有所有外部类所有成员的访问权，这是因为应用在创建一个内部类的对象时，这个对象就和制造该对象的外部类有了一种联系，既内部类对象会秘密的捕获一个指向外部类对象的引用。（注意：如果是静态内部类的话就不需要这种引用）；
+ 内部类对象需要通过外部类的对象来创建；
+ 在拥有外部类对象之前是不可能拥有内部类对象的，这是因为内部类对象会悄悄自动连接到创建它的外部类对象上。（注意：如果是静态内部类的话就不需要这种引用）；

#### 2、嵌套类（静态内部类）（内部类对象与外部类对象不存在联系）
+ 要创建嵌套类对象，不需要外部类对象；
+ 不能从嵌套类的对象中访问非静态的外部类对象；

### 三、存在意义

一般来说，内部类继承自某个类或者实现某个类的接口，每个内部类都能独立的继承自一个（接口）的实现，所以无论外围类是否继承（接口）的实现，对于内部类没有任何影响。

> 理解：我们可以在一个类的创建多个内部类，相当于带了很多小弟，这些小弟总得认识自己的老大是谁吧（指向外围类对象的引用），这些小弟可以共享我的资源，同时，这些小弟都很优秀，能够独立完成我交给他们的某些工作（一个实现）。

### 四、闭包与回调
+ 闭包：闭包是一个对象，它记录了一些信息，这些信息来自于该对象的作用域；
+ 回调：回调的价值在于它的灵活性——可以在运行时决定调用什么方法；

### 五、内部类的继承

由于内部类对象在创建时能够自动捕获指向外围类的对象的的引用，但是其内部类的导出类的构造器就没有这个能力，所以需要在构造器中手动添加：enclosingClassReference.super();，否则编译不过。


