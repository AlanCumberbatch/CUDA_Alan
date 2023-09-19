## 数据结构

C++是一种多范式编程语言，它允许程序员创建各种数据结构来组织和管理数据。以下是C++中常见的数据结构：

1. **数组（Array）：**
   - 数组是一种线性数据结构，用于存储具有相同数据类型的元素序列。
   - C++提供了内置的数组类型，例如 `int myArray[5];`，也支持标准库中的 `std::array` 和 `std::vector`。

   ```cpp
   int myArray[5] = {1, 2, 3, 4, 5};
   ```

2. **向量（Vector）：**
   - 向量是C++标准库中的动态数组，它提供了可变大小的数组功能。
   - `std::vector` 可以动态增长或缩小，适合动态管理数据集合。

   ```cpp
   #include <vector>
   std::vector<int> myVector = {1, 2, 3, 4, 5};
   ```

3. **链表（Linked List）：**
   - 链表是一种动态数据结构，由节点组成，每个节点包含数据和指向下一个节点的指针。
   - C++中可以使用自定义类或标准库中的 `std::list` 来实现链表。

   ```cpp
   struct Node {
       int data;
       Node* next;
   };
   ```

4. **栈（Stack）：**
   - 栈是一种线性数据结构，遵循后进先出（LIFO）的原则。
   - C++中可以使用 `std::stack` 类来实现栈。

   ```cpp
   #include <stack>
   std::stack<int> myStack;
   ```

5. **队列（Queue）：**
   - 队列是一种线性数据结构，遵循先进先出（FIFO）的原则。
   - C++中可以使用 `std::queue` 或 `std::deque` 来实现队列。

   ```cpp
   #include <queue>
   std::queue<int> myQueue;
   ```

6. **集合（Set）：**
   - 集合是一种不允许重复元素的数据结构，通常用于存储独立的元素。
   - C++标准库提供了 `std::set` 和 `std::unordered_set` 来实现集合。

   ```cpp
   #include <set>
   std::set<int> mySet = {1, 2, 3};
   ```

7. **映射（Map）：**
   - 映射是一种键-值对的数据结构，允许通过键来访问值。
   - C++标准库提供了 `std::map` 和 `std::unordered_map` 来实现映射。

   ```cpp
   #include <map>
   std::map<std::string, int> myMap;
   ```

8. **树（Tree）：**
   - 树是一种分层数据结构，通常用于表示层次关系。
   - C++中可以使用自定义类来实现二叉树、红黑树等，也可以使用 `std::map` 和 `std::set` 来表示树结构。

9. **图（Graph）：**
   - 图是一种复杂的数据结构，由节点和边组成，用于表示多对多关系。
   - 图的实现通常需要自定义类或使用图算法库。

C++还允许程序员自定义数据结构，以满足特定需求。这些数据结构可以用于各种应用，包括数据存储、算法实现、图形和游戏开发等。标准库提供了许多有用的数据结构和容器，使数据结构的创建和使用变得更加方便。

[回到C++ Basic](./README.md)

### 关于如何自定义数据类型

自定义数据结构是C++中的一个关键概念，它允许程序员定义自己的数据类型，以便更好地组织和管理数据。以下是自定义数据结构的基本步骤：

1. **选择数据结构类型**：首先，确定您要创建的数据结构的类型。根据需要选择合适的数据结构，例如结构体（`struct`）或类（`class`）。

2. **定义数据结构**：使用 `struct` 或 `class` 关键字来定义数据结构。在数据结构内部，您可以定义成员变量和成员函数。

   ```cpp
   // 使用 struct 定义结构体
   struct MyStruct {
       int data;
       double value;
   };

   // 使用 class 定义类
   class MyClass {
   public:
       int data;
       void setData(int d) {
           data = d;
       }
   };
   ```

3. **添加成员变量**：根据数据结构的需求，定义成员变量，它们将用于存储数据。成员变量可以具有不同的数据类型，可以是内置类型、自定义类型或标准库容器。

4. **添加成员函数**：如果需要，在数据结构内部定义成员函数，这些函数可以用于操作数据或执行特定任务。成员函数可以访问成员变量，并且可以具有各种访问控制权限（`public`、`private`、`protected`）。

   ```cpp
   struct MyStruct {
       int data;
       double value;

       void printData() {
           std::cout << "Data: " << data << std::endl;
       }
   };
   ```

5. **实例化对象**：在使用自定义数据结构之前，需要实例化一个或多个对象。对象是数据结构的具体实例，可以通过构造函数来创建。

   ```cpp
   MyStruct myInstance;
   MyClass myObject;
   ```

6. **访问成员**：使用对象来访问数据结构的成员变量和成员函数。通过点运算符 `.` 来访问成员。

   ```cpp
   myInstance.data = 42;
   myObject.setData(10);
   myInstance.printData();
   ```

7. **使用数据结构**：将数据结构用于您的程序中，可以进行数据存储、处理和传递。根据需要创建多个对象，每个对象都可以独立管理自己的数据。

下面是一个完整的示例，展示了如何创建自定义数据结构和使用它：

```cpp
#include <iostream>

struct Point {
    double x;
    double y;

    void print() {
        std::cout << "Point(" << x << ", " << y << ")" << std::endl;
    }
};

int main() {
    Point p1; // 创建 Point 结构体对象
    p1.x = 3.0;
    p1.y = 4.0;
    p1.print();

    Point p2 = {1.0, 2.0}; // 使用初始化列表创建对象
    p2.print();

    return 0;
}
```

这是一个简单的示例，展示了如何创建和使用自定义数据结构。您可以根据需要扩展数据结构，并添加更多的成员变量和成员函数来满足特定的需求。自定义数据结构是C++编程中的重要概念，允许您更好地组织和抽象数据。