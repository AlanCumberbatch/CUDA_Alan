# Environment setup/环境搭建

## How to use C++ in Mac/ Mac 中

- 需要安装 xcode 作为 Cpp的运行环境
- 检查是否安装XCode： xcode-select -p
  - 安装： 输出 Xcode 的安装路径
  - 未安装： 输出 ‘xcode-select: command not found’
- 安装方法：
  - A： 软件商店安装XCode
  - B： 使用命令行安装 Xcode Command Line Tools： xcode-select --install // 它是 Xcode 的一部分，包含开发所需的一些工具和库。

## In Linux / Linux 中


# Key things to know / 一些需要知道的事情

## C++ about / C++相关


- [Grammar/语法](./Grammer.md)
- [DataStructure数据结构](./dataStructure.md)
- [Pointer/指针](./pointer.md)
- C++ 支持的编程范式：
  C++是一种多范式（multi-paradigm）编程语言，这意味着它支持多种不同的编程范式，允许程序员根据任务的要求选择最合适的编程方式。以下是C++支持的主要编程范式：

  1. **过程式编程（Procedural Programming）：**
     - 过程式编程是一种基于过程或函数的编程范式，其中程序由一系列函数组成，这些函数按顺序执行来完成任务。
     - C++支持过程式编程，程序员可以编写函数来执行特定任务，这些函数可以接受参数和返回值。

  2. **面向对象编程（Object-Oriented Programming，OOP）：**
     - C++是一种面向对象编程语言，它支持面向对象的编程范式。
     - 面向对象编程通过定义类和对象来组织和封装数据和行为。C++中的类允许数据成员和成员函数的封装，继承和多态。
     - 面向对象编程有助于提高代码的可维护性和可重用性。

  3. **泛型编程（Generic Programming）：**
     - C++支持泛型编程，允许编写通用的、可重用的代码，不依赖于特定的数据类型。
     - 泛型编程通过使用模板（template）来实现，它允许编写通用的函数和类，这些函数和类可以用于不同的数据类型。

  4. **函数式编程（Functional Programming）：**
     - C++在一定程度上支持函数式编程，允许函数作为一等公民，可以将函数作为参数传递给其他函数，也可以从函数中返回函数。
     - C++11引入了Lambda表达式，增强了对函数式编程的支持。

  5. **元编程（Metaprogramming）：**
     - C++允许元编程，这意味着程序可以在编译时生成代码或进行代码分析。
     - 元编程通常使用模板元编程技术，允许在编译时执行计算，生成代码或进行元信息的操作。

  6. **并发编程（Concurrent Programming）：**
     - C++提供了多线程支持，允许编写并发程序，利用多核处理器来提高性能。
     - C++11引入了 `<thread>` 头文件，引入了线程、互斥锁、条件变量等多线程编程的标准库支持。

  7. **事件驱动编程（Event-Driven Programming）：**
     - 在图形用户界面（GUI）和游戏开发中，C++可以用于事件驱动编程，通过处理事件（如鼠标点击或键盘输入）来实现交互式应用程序。

  8. **面向服务编程（Service-Oriented Programming）：**
     - C++可以用于构建面向服务的应用程序，特别是在网络和分布式系统中，使用库和框架来提供和消费服务。

  C++的多范式性质使其非常灵活，可以用于各种类型的应用程序开发，从系统编程到图形用户界面和科学计算等不同领域。程序员可以根据任务的需求选择合适的编程范式或将它们结合使用。这使得C++成为一种强大且多才多艺的编程语言。

- ...

...

[另外一种学习方式--变量的生命周期入手/Another way to learn --- start from The life cycle of the variable [还没开始写]](./LifeCycleOfTheVariable.md)

