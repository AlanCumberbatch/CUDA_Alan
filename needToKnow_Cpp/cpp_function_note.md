C++中的函数是程序的基本组成单元之一，它们用于执行特定任务或操作。以下是C++中与函数相关的全部知识点：

1. **函数声明和定义：**
   - 函数的声明包括函数的返回类型、函数名称和参数列表，用于告诉编译器函数的存在。
   - 函数的定义包括函数的实际实现，包括函数体。

   ```cpp
   int add(int x, int y); // 函数声明
   int add(int x, int y) { // 函数定义
       return x + y;
   }
   ```

2. **函数参数和返回值：**
   - 函数可以接受零个或多个参数，这些参数在函数定义中使用。
   - 函数可以返回一个值，这个值的类型由函数的返回类型确定。

   ```cpp
   int add(int x, int y) {
       return x + y;
   }
   ```

3. **函数调用：**
   - 函数在程序中通过名称来调用。
   - 调用函数时，传递给函数的实际参数（实参）与函数声明中的形式参数（形参）匹配。

   ```cpp
   int result = add(10, 20); // 调用add函数
   ```

4. **函数重载（Function Overloading）：**
   - 可以在同一个作用域中定义多个同名函数，只要它们的参数列表不同。
   - 编译器会根据传递的参数类型和数量选择正确的函数进行调用。

   ```cpp
   int add(int x, int y);
   double add(double x, double y); // 函数重载
   ```

5. **函数参数的默认值：**
   - 可以为函数的参数提供默认值，这样在调用函数时可以省略这些参数。

   ```cpp
   int multiply(int x, int y = 2); // y有默认值
   ```

6. **递归函数（Recursive Functions）：**
   - 函数可以调用自身，称为递归函数。
   - 递归函数通常包括基本情况（递归终止条件）和递归情况。

   ```cpp
   int factorial(int n) {
       if (n <= 1) {
           return 1; // 基本情况
       } else {
           return n * factorial(n - 1); // 递归情况
       }
   }
   ```

7. **函数指针（Function Pointers）：**
   - 函数指针是指向函数的指针变量，可以用于动态调用不同的函数。

   ```cpp
   int (*funcPtr)(int, int); // 函数指针的声明
   funcPtr = add; // 函数指针赋值为add函数
   int result = funcPtr(10, 20); // 通过函数指针调用函数
   ```

8. **局部变量和作用域：**
   - 函数内部可以定义局部变量，这些变量只在函数内部可见。
   - 变量的作用域仅限于声明它的代码块。

   ```cpp
   int myFunction() {
       int localVar = 5; // 局部变量
       return localVar;
   }
   ```

9. **全局函数和静态函数：**
   - 函数可以定义为全局函数，这些函数可以在程序的任何地方调用。
   - 静态函数具有文件作用域，只能在当前文件中调用。

   ```cpp
   int globalFunction() {
       // 全局函数
       return 42;
   }

   static int staticFunction() {
       // 静态函数
       return 10;
   }
   ```

10. **内联函数（Inline Functions）：**
    - 内联函数是使用 `inline` 关键字声明的函数，编译器会尝试将函数的代码嵌入到调用处，以提高执行效率。
    - 内联函数通常用于短小的函数。

    ```cpp
    inline int multiply(int x, int y) {
        return x * y;
    }
    ```

这些是与C++函数相关的主要知识点。函数是C++编程中非常重要的概念，用于将代码分解成可管理和可复用的模块。函数的正确使用可以提高代码的可读性和维护性。

[回到语法内容](./Grammer.md)