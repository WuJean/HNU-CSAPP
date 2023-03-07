# 第二次小班课

* [ ] ppt制作
* [ ] 剧本制作
* [ ] 材料收集

### 分工 （可以把自己选择的分工写在后面）

* ppt各点内容编写：邱桥、
* 剧本编写：
* ppt排版制作配图 ：
* 大纲、材料收集汇总：wujean、邱桥

## 一、PPT制作

### ppt的大纲：

* 分点说明代码里的未定义操作有哪些
  *
* 还有哪些类似的“未定义的操作”，举例说明。
  *
* 分别说明未定义操作在不同编译器下有什么结果
  * 这个要不要写出代码，然后用不同编译器编译一下获得结果，截图进来？
  * 可以使用在![](file:///C:/Users/qq/AppData/Roaming/Tencent/QQ/Temp/%W@GJ$ACOF\(TYDYECOKVDYB.png)https://godbolt.org/上获取不同编译器的结果
* 从汇编代码来讨论其结果不同的原因。（可在![](file:///C:/Users/qq/AppData/Roaming/Tencent/QQ/Temp/%W@GJ$ACOF\(TYDYECOKVDYB.png)https://godbolt.org/上获取不同编译器的结果）（这个可以现场编译一下，展示汇编代码的区别？）
  * 我们要选哪几个编译器？讲多少个汇编代码？



## 二、剧本制作

## 三、材料收集（将收集好的材料按照二级标题分类存档）

### 3.1 小班题目相关

#### 3.1.1 该段代码中有哪些未定义行为

1. 在一个表达式中修改一个变量的值：在语句“1 \* a\[i++] + 2 \* a\[i++] + 3 \* a\[i++]”中，对于i的后缀自增操作，无法保证i的值被修改的顺序和结果，因为C语言没有规定在表达式中对变量进行的多次修改的顺序。
2. 对同一个变量进行后缀自增或后缀自减操作，并使用该变量的值：在语句“j=j++”中，j的值不能保证会被正确更新，因为C语言没有规定在同一表达式中的自增和自减操作的顺序，这个代码段实际上是未定义行为。

因此，这段代码有两个未定义行为，需要修改为确定的行为。

#### 3.1.2 为什么会出现未定义行为

在C++中，未定义行为是指当程序的行为不可预测或不符合语言规范时会发生的情况。这通常是由于程序员未正确编写程序代码或由于编译器实现不一致而导致的。

C++允许未定义行为的主要原因是为了允许编译器和运行时系统在实现时进行优化，并允许程序员利用底层硬件的细节来提高性能。例如，某些优化技术（如代码重排和死代码消除）可能会导致未定义的行为。此外，允许未定义行为还使C++能够保持简单，而不需要在语言规范中规定所有细节和行为，从而增加了语言的灵活性和可扩展性。

然而，程序员应该避免依赖于未定义的行为，因为这会导致程序不可预测、不可移植或不稳定。相反，程序员应该编写符合C++语言规范的代码，并使用良好的编程实践来确保程序的正确性和可移植性。

#### 3.1.3 如何解决这些未定义行为

#### 3.1.4 编译优化

### 3.2 汇编指令相关

#### 3.2.1 汇编代码中的指令

```asm
mov     DWORD PTR [rbp-4], 0
dword   双字 就是四个字节
ptr     pointer缩写 即指针
[]里的数据是一个地址值，这个地址指向一个双字型数据
```

#### 3.2.2 寄存器和栈帧

[https://blog.csdn.net/ccboby/article/details/6042380](https://blog.csdn.net/ccboby/article/details/6042380) X86-64寄存器和栈帧





### 3.3 未定义操作相关

**3.3.1 一些常见的未定义行为包括：**

* 读取或写入超出数组边界范围的内存。
* 对空指针进行解引用。
* 在函数中使用未初始化的变量。
* 在表达式中多次修改同一变量而没有使用序列点。
* 在函数参数列表中多次对同一参数求值。

(perplexity.ai)在C语言中，有许多未定义的操作。以下是一些常见的未定义行为：

* 1\. 数组越界：当程序试图访问数组元素时，如果下标超出了数组的范围，则会发生未定义行为[\[1\]](https://www.hiczp.com/c-cpp/c-yu-yan-chang-jian-wei-ding-yi-hang-wei.html)[\[2\]](https://c-cpp.com/c/language/behavior)[\[3\]](https://www.nowcoder.com/questionTerminal/8e273aeb2b4147fea72ff08814fc78e6)。
* 2\. 在表达式中修改变量并且没有指定顺序：例如 \`j=j++\` 这样的代码也是未定义的[\[1\]](https://www.hiczp.com/c-cpp/c-yu-yan-chang-jian-wei-ding-yi-hang-wei.html)[\[2\]](https://c-cpp.com/c/language/behavior)。
* 3\. 使用空指针或释放已经释放过的指针：这些都是未定义行为，可能导致程序崩溃或者产生其他错误[\[1\]](https://www.hiczp.com/c-cpp/c-yu-yan-chang-jian-wei-ding-yi-hang-wei.html)[\[3\]](https://www.nowcoder.com/questionTerminal/8e273aeb2b4147fea72ff08814fc78e6)。
* 4\. 对于没有初始化的变量进行读取操作：这个行为也是未定义的，因为它依赖于编译器和运行时环境[\[1\]](https://www.hiczp.com/c-cpp/c-yu-yan-chang-jian-wei-ding-yi-hang-wei.html)。
* 5\. 有符号整数溢出：当有符号整数类型发生溢出时，结果是未定义的[\[2\]](https://c-cpp.com/c/language/behavior)。
* 需要注意的是，在不同编译器上或者不同操作系统或者不同架构CPU上会产生不同结果。因此，在编写 C 代码时应该尽量避免使用未定义行为，并且要注意不同编译器之间可能存在差异。
  * 5 SOURCESView List1![hiczp.com favicon](https://www.google.com/s2/favicons?domain=hiczp.com)hiczp2![c-cpp.com favicon](https://www.google.com/s2/favicons?domain=c-cpp.com)c-cpp3![nowcoder.com favicon](https://www.google.com/s2/favicons?domain=nowcoder.com)nowcoder4![csdn.net favicon](https://www.google.com/s2/favicons?domain=csdn.net)csdn5![juejin.cn favicon](https://www.google.com/s2/favicons?domain=juejin.cn)juejin

<!---->

* [ ] 来个人用相关的例子把这里给填满

**3.3.2 例子**

```c
//比较乱，待整理
int arr[5] = {1, 2, 3, 4, 5};
int x = arr[10]; // 超出数组下标范围

int i = 5;
i = i++; // i++ 和赋值操作之间没有中间值

int *p = NULL;
int x = *p; // 解引用空指针
int *q = malloc(sizeof(int));

free(q);
free(q); // 释放已经释放过的指针

int x;
int y = x; // 未初始化的变量 x 读取其值是未定义行为

int i = INT_MAX;
i = i + 1; // 发生有符号整数溢出

//在表达式中多次修改同一变量而没有使用序列点。
int x = 5;
int y = ++x + ++x;  // 未使用序列点

//在函数参数列表中多次对同一参数求值。
int square(int x) {
    return x * x;
}

int func(int a, int b, int c) {
    int result = square(a++) + square(++b) + square(c);
    return result;
}

int main() {
    int x = 2;
    int y = func(x, x, x);
    return 0;
}

```

### 3.4 拓展阅读相关
