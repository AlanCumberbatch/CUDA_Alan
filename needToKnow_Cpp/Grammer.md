### 基础语法

C++是一种多范式编程语言，它包含了面向对象编程（OOP）和泛型编程等多种编程范式。以下是C++的一些基础语法和概念：<---> [C Grammar](./Geammar_C.md)

1. **注释：** C++支持两种类型的注释：
   - 单行注释：以`//`开头，注释掉从`//`开始到行尾的内容。
   - 多行注释：以`/*`开头，以`*/`结尾，注释掉两者之间的内容。

  ```cpp
  // 这是单行注释

  /*
     这是
     多行
     注释
  */
  ```

2. **标识符：** 标识符是用于命名变量、函数、类等的名称。标识符必须以 **字母**、**下划线** 或者 **@符号** 开始，后面可以包含<u>字母、数字、下划线或@符号</u>。[延伸](#标识符延伸)

```cpp
int myVariable; // 变量名myVariable
void myFunction(); // 函数名myFunction
class MyClass {}; // 类名MyClass
```

3. **数据类型：** C++支持多种内置数据类型，包括整数、浮点数、字符、布尔值等。[延伸](#数据类型延伸)

```cpp
int myInt = 42; // 整数
double myDouble = 3.14; // 浮点数
char myChar = 'A'; // 字符
bool myBool = true; // 布尔值
```

4. **变量声明和赋值：** 变量必须先声明后使用，可以使用`=`赋值。[延伸](#变量的声明和赋值延伸)

```cpp
int x; // 声明变量x
x = 10; // 赋值
```

5. **运算符：** C++支持多种运算符，包括算术运算符、比较运算符、逻辑运算符等。[延伸](#c的所有运算符)

```cpp
int a = 5, b = 3;
int sum = a + b; // 加法
bool isEqual = (a == b); // 等于
bool isGreater = (a > b); // 大于
```

6. **条件语句：** 使用`if`、`else if`和`else`语句来进行条件判断。

```cpp
if (condition) {
    // 如果条件为真，执行这里的代码
} else if (anotherCondition) {
    // 如果上面的条件为假，且这个条件为真，执行这里的代码
} else {
    // 如果上面的条件都为假，执行这里的代码
}
```

7. **循环语句：** 使用`for`、`while`、`do...while`等语句来进行循环。

```cpp
for (int i = 0; i < 5; i++) {
    // 循环5次
}

while (condition) {
    // 当条件为真时执行
}

do {
    // 执行一次，然后检查条件
} while (condition);
```

8. **函数：** 使用`function`关键字来定义函数，函数可以有参数和返回值。[扩展](./cpp_function_note.md)

```cpp
int add(int a, int b) {
    return a + b;
}
```

9. **类和对象：** C++支持面向对象编程，你可以使用`class`来定义类，创建类的对象，并调用对象的方法。[扩展](./cpp_class_note.md)

```cpp
class MyClass {
public:
    void myMethod() {
        // 类的方法
    }
};

MyClass obj; // 创建对象
obj.myMethod(); // 调用对象的方法
```

这只是C++语言的一些基础语法和概念，C++还包括更多高级特性，如模板、继承、多态、异常处理等。学习C++需要时间和实践，可以查阅C++的相关教程和文档来深入了解这门编程语言。


[回到C++ Basic](./README.md)

### 标识符延伸

C++标识符是用于命名变量、函数、类、对象等各种程序实体的名称。C++中标识符的命名规则如下：

1. **必须以字母、下划线(_)或者@符号开始。** 标识符的首字符只能是字母（包括大写字母和小写字母）、下划线或者@符号。例如，`var_name`、`_value`、`@count` 都是有效的标识符。

2. **后续字符可以是字母、数字、下划线或者@符号。** 标识符的后续字符可以是字母（包括大写字母和小写字母）、数字、下划线或者@符号。例如，`myVariable`、`value123`、`data_2` 都是有效的标识符。

3. **大小写敏感。** C++是大小写敏感的，所以大写字母和小写字母被视为不同的字符。例如，`myVariable` 和 `MyVariable` 是不同的标识符。

4. **不能使用关键字。** 不能使用C++的关键字（保留字）作为标识符。例如，不能使用 `int`、`while`、`class` 等作为标识符。

5. **长度没有限制。** 标识符的长度理论上没有限制，但通常建议使用有意义且不过长的标识符，以提高代码的可读性。

以下是一些示例，展示了有效的C++标识符和无效的标识符：

有效的标识符：
```cpp
myVariable
Value123
_data
_count
variable1
```

无效的标识符：
```cpp
123value (数字不能作为首字符)
while (关键字不能用作标识符)
my-variable (不能使用破折号)
@special (不能使用@符号作为首字符以外的位置)
```

总之，C++标识符需要遵守一定的命名规则和规范，以确保代码的可读性和正确性。虽然标识符的长度理论上没有限制，但建议使用有意义的、清晰的标识符，以提高代码的可维护性。

[回顶部](#基础语法)

### 数据类型延伸

C++包含多种数据类型，包括基本数据类型、派生数据类型和用户自定义数据类型。以下是所有可能的C++数据类型以及相应的示例：

**基本数据类型（Primitive Data Types）：**

1. **整数类型（Integer Types）：**
   - `int`：整数类型。
     ```cpp
     int x = 42;
     ```

   - `short`：短整数类型。
     ```cpp
     short y = 10;
     ```

   - `long`：长整数类型。
     ```cpp
     long z = 1000000L;
     ```

   - `long long`：长长整数类型。
     ```cpp
     long long bigNumber = 123456789012345LL;
     ```

2. **浮点数类型（Floating-Point Types）：**
   - `float`：单精度浮点数。
     ```cpp
     float pi = 3.14159f;
     ```

   - `double`：双精度浮点数。
     ```cpp
     double e = 2.71828;
     ```

   - `long double`：扩展精度浮点数。
     ```cpp
     long double someValue = 0.12345678901234567890L;
     ```

3. **字符类型（Character Types）：**
   - `char`：字符类型，通常为8位，用于存储单个字符。
     ```cpp
     char grade = 'A';
     ```

   - `wchar_t`：宽字符类型，用于处理宽字符集。
     ```cpp
     wchar_t wideChar = L'宽';
     ```

   - `char16_t` 和 `char32_t`：用于支持Unicode字符集。

4. **布尔类型（Boolean Type）：**
   - `bool`：布尔类型，用于表示真（true）或假（false）。
     ```cpp
     bool isTrue = true;
     ```

5. **空类型（Void Type）：**
   - `void`：空类型，通常用于函数返回值或指针。
     ```cpp
     void printMessage() {
         std::cout << "Hello, World!" << std::endl;
     }
     ```

**派生数据类型（Derived Data Types）：**

6. **指针类型（Pointer Types）：**
   - `T*`：指向类型 `T` 的指针。
     ```cpp
     int* ptr = nullptr; // 指向整数的空指针
     ```

7. **数组类型（Array Types）：**
   - `T[]` 或 `T[n]`：包含元素类型 `T` 的数组，其中 `n` 是数组的大小。
     ```cpp
     int numbers[5] = {1, 2, 3, 4, 5};
     ```

8. **引用类型（Reference Types）：**
   - `T&`：引用类型，用于创建变量的别名。
     ```cpp
     int a = 42;
     int& ref = a; // a的引用
     ```

**用户自定义数据类型（User-Defined Data Types）：**

9. **结构体（Structures）：**
   - 定义和使用结构体：
     ```cpp
     struct Person {
         std::string name;
         int age;
     };

     Person john;
     john.name = "John";
     john.age = 30;
     ```

10. **类（Classes）：**
    - 定义和使用类：
      ```cpp
      class Circle {
      public:
          double radius;

          double calculateArea() {
              return 3.14159 * radius * radius;
          }
      };

      Circle myCircle;
      myCircle.radius = 5.0;
      double area = myCircle.calculateArea();
      ```

11. **枚举类型（Enumeration Types）：**
    - 定义和使用枚举类型：
      ```cpp
      enum Color { Red, Green, Blue };
      Color selectedColor = Green;
      ```

12. **联合类型（Union Types）：**
    - 定义和使用联合类型：
      ```cpp
      union Data {
          int i;
          double d;
          char c;
      };
      Data value;
      value.i = 42;
      ```

这些是C++中所有可能的数据类型，包括基本数据类型、派生数据类型和用户自定义数据类型。你可以根据编程需求选择合适的数据类型来存储和操作数据。

此外，当考虑 "signed" 和 "unsigned" 时，C++中的整数类型（Integer Types）可以进一步分类。以下是包括 "signed" 和 "unsigned" 的所有整数类型：

**整数类型（Integer Types）：**

1. **有符号整数（Signed Integer Types）：**
   - `int`：整数类型，通常为32位。
     ```cpp
     int x = 42;
     ```

   - `short`：短整数类型，通常为16位。
     ```cpp
     short y = 10;
     ```

   - `long`：长整数类型，通常为32位或64位。
     ```cpp
     long z = 1000000L;
     ```

   - `long long`：长长整数类型，通常为64位。
     ```cpp
     long long bigNumber = 123456789012345LL;
     ```

2. **无符号整数（Unsigned Integer Types）：**
   - `unsigned int`：无符号整数类型，通常为32位。
     ```cpp
     unsigned int a = 100;
     ```

   - `unsigned short`：无符号短整数类型，通常为16位。
     ```cpp
     unsigned short b = 20;
     ```

   - `unsigned long`：无符号长整数类型，通常为32位或64位。
     ```cpp
     unsigned long c = 1000000UL;
     ```

   - `unsigned long long`：无符号长长整数类型，通常为64位。
     ```cpp
     unsigned long long hugeNumber = 123456789012345ULL;
     ```

对于这些整数类型，"signed" 表示有符号整数，可以表示正数、负数和零，而 "unsigned" 表示无符号整数，只能表示非负数和零。

其他基本数据类型（浮点数、字符、布尔和空类型）仍然保持不变。你可以根据需要选择适当的数据类型来存储和操作数据。

[回顶部](#基础语法)

## 变量的声明和赋值延伸

在C++中，变量声明和赋值可以以多种方式进行。以下是一些常见的变量声明和赋值的方式：

1. **声明并初始化**：在声明变量的同时进行初始化。

   ```cpp
   int x = 42; // 声明并初始化整数变量x为42
   ```

2. **分开声明和初始化**：先声明变量，然后在稍后的代码行初始化它。

   ```cpp
   int y;     // 声明整数变量y
   y = 10;    // 初始化y为10
   ```

3. **多个变量的声明和初始化**：同时声明并初始化多个变量。

   ```cpp
   int a = 1, b = 2, c = 3; // 同时声明并初始化多个整数变量
   ```

4. **复制初始化**：使用等号进行初始化。

   ```cpp
   int m;
   m = 5; // 复制初始化
   ```

5. **列表初始化**：使用花括号 `{}` 进行初始化。

   ```cpp
   int numbers[] = {1, 2, 3}; // 使用列表初始化数组
   ```

6. **默认初始化**：变量在声明时没有显式初始化，将根据数据类型进行默认初始化。[默认初始化时各个类型的变量的初始值](#默认初始化时各个类型的变量的初始值)

   ```cpp
   int n; // 默认初始化为0
   ```

7. **动态初始化**：在运行时根据条件进行初始化。

   ```cpp
   int age;
   std::cout << "请输入年龄：";
   std::cin >> age;
   ```

8. **引用初始化**：初始化引用变量时，它必须与另一个变量绑定在一起。

   ```cpp
   int original = 10;
   int& ref = original; // 初始化引用
   ```

9. **const 变量初始化**：const 变量必须在声明时进行初始化。

   ```cpp
   const double pi = 3.14159; // 初始化const变量
   ```

10. **auto 类型推断**：使用 `auto` 关键字进行类型推断，编译器根据初始化表达式的类型确定变量类型。

    ```cpp
    auto value = 42; // 编译器推断value为整数类型
    ```

这些是一些常见的变量声明和赋值的方式。你可以根据具体的情况和编程需求选择适当的方式来初始化变量。请注意，C++允许不同的初始化方式，以便灵活地处理不同的编程场景。

[回顶部](#基础语法)

## C++的所有运算符

[运算符demo](./demoForOperator.md)

C++支持多种运算符，这些运算符用于执行各种操作，包括算术运算、逻辑运算、关系运算、位运算等。以下是C++中的常见运算符分类及示例：

**1. 算术运算符（Arithmetic Operators）：**
- `+`：加法
- `-`：减法
- `*`：乘法
- `/`：除法
- `%`：取模（取余数）

```cpp
int a = 10;
int b = 5;
int sum = a + b; // 加法
int difference = a - b; // 减法
int product = a * b; // 乘法
int quotient = a / b; // 除法
int remainder = a % b; // 取模
```

**2. 关系运算符（Relational Operators）：**
- `==`：等于
- `!=`：不等于
- `<`：小于
- `>`：大于
- `<=`：小于等于
- `>=`：大于等于

```cpp
int x = 10;
int y = 5;
bool isEqual = (x == y); // 等于
bool isNotEqual = (x != y); // 不等于
bool isLessThan = (x < y); // 小于
bool isGreaterThan = (x > y); // 大于
bool isLessThanOrEqual = (x <= y); // 小于等于
bool isGreaterThanOrEqual = (x >= y); // 大于等于
```

**3. 逻辑运算符（Logical Operators）：**
- `&&`：逻辑与（AND）
- `||`：逻辑或（OR）
- `!`：逻辑非（NOT）

```cpp
bool condition1 = true;
bool condition2 = false;
bool andResult = (condition1 && condition2); // 逻辑与
bool orResult = (condition1 || condition2); // 逻辑或
bool notResult = !condition1; // 逻辑非
```

**4. 位运算符（Bitwise Operators）：**
- `&`：按位与
- `|`：按位或
- `^`：按位异或
- `~`：按位取反
- `<<`：左移位
- `>>`：右移位

```cpp
int num1 = 5; // 二进制：0101
int num2 = 3; // 二进制：0011
int andResult = num1 & num2; // 按位与
int orResult = num1 | num2; // 按位或
int xorResult = num1 ^ num2; // 按位异或
int notResult = ~num1; // 按位取反
int leftShiftResult = num1 << 1; // 左移位
int rightShiftResult = num1 >> 1; // 右移位
```

**5. 赋值运算符（Assignment Operators）：**
- `=`：赋值
- `+=`：加法赋值
- `-=`：减法赋值
- `*=`：乘法赋值
- `/=`：除法赋值
- `%=`：取模赋值
- `&=`：按位与赋值
- `|=`：按位或赋值
- `^=`：按位异或赋值
- `<<=`：左移位赋值
- `>>=`：右移位赋值

```cpp
int x = 10;
int y = 5;
x += y; // 加法赋值，x变为15
x -= y; // 减法赋值，x变为10
x *= y; // 乘法赋值，x变为50
x /= y; // 除法赋值，x变为10
x %= y; // 取模赋值，x变为0
x &= y; // 按位与赋值
x |= y; // 按位或赋值
x ^= y; // 按位异或赋值
x <<= 2; // 左移位赋值
x >>= 1; // 右移位赋值
```

这些是C++中的一些常见运算符。C++还包含其他运算符，如条件运算符（三元运算符 `? :`）、逗号运算符 `,`、成员访问运算符 `.` 和 `->` 等。每个运算符都有其特定的用途，根据需要选择适当的运算符来执行操作。

[回顶部](#基础语法)


### 默认初始化时各个类型的变量的初始值

在C++中，变量的默认初始化值取决于变量的类型和声明方式。以下是一些常见数据类型的默认初始化值：

1. **整数类型（Integer Types）**：
   - `int`、`short`、`long` 和 `long long`：默认初始化为0。
   - `unsigned int`、`unsigned short`、`unsigned long` 和 `unsigned long long`：默认初始化为0。

   例如：
   ```cpp
   int x; // 默认初始化为0
   unsigned long y; // 默认初始化为0
   ```

2. **浮点数类型（Floating-Point Types）**：
   - `float` 和 `double`：默认初始化为0.0。
   - `long double`：默认初始化为0.0。

   例如：
   ```cpp
   double pi; // 默认初始化为0.0
   ```

3. **字符类型（Character Types）**：
   - `char`：默认初始化为'\0'，即空字符。
   - `wchar_t`：默认初始化为0。
   - `char16_t` 和 `char32_t`：默认初始化为0。

   例如：
   ```cpp
   char ch; // 默认初始化为'\0'
   ```

4. **布尔类型（Boolean Type）**：
   - `bool`：默认初始化为`false`。

   例如：
   ```cpp
   bool isTrue; // 默认初始化为false
   ```

5. **空类型（Void Type）**：`void` 类型不具有默认初始化值，因为它通常用于函数返回值或指针。

   例如：
   ```cpp
   void* ptr; // 默认不初始化，通常需要手动赋值
   ```

需要注意的是，默认初始化值只在不显式提供初始化值的情况下才会应用。如果你在声明变量时提供了初始值，那么该初始值将覆盖默认初始化值。如果你希望确保变量被默认初始化，可以使用以下方式：

```cpp
int x = int(); // 使用类型的默认构造函数进行默认初始化
```

上述代码将 `x` 初始化为整数类型的默认值，即0。对于其他数据类型，也可以类似地使用其默认构造函数来进行默认初始化。