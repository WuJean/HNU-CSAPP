# 第二次小班课

* [ ] ppt制作
* [ ] 剧本制作
* [ ] 材料收集

### 分工 （可以把自己选择的分工写在后面）

* ppt各点内容编写：邱桥、
* 剧本编写：
* ppt排版制作配图 ：

## 一、PPT制作

### ppt的大纲：

* 分点说明代码里的未定义操作有哪些
  *   （ChatGPT）以下是代码中的未定义操作：

      1. 在一个表达式中修改一个变量的值：在语句“1 \* a\[i++] + 2 \* a\[i++] + 3 \* a\[i++]”中，对于i的后缀自增操作，无法保证i的值被修改的顺序和结果，因为C语言没有规定在表达式中对变量进行的多次修改的顺序。
         1. 对同一个变量进行后缀自增或后缀自减操作，并使用该变量的值：在语句“j=j++”中，j的值不能保证会被正确更新，因为C语言没有规定在同一表达式中的自增和自减操作的顺序，这个代码段实际上是未定义行为。

      因此，这段代码有两个未定义行为，需要修改为确定的行为。
* 还有哪些类似的“未定义的操作”，举例说明。
  *   ## (PERPLEXITY.ai)在c语言中，有哪些未定义的操作？

      在C语言中，有许多未定义的操作。以下是一些常见的未定义行为：

      * 1\. 数组越界：当程序试图访问数组元素时，如果下标超出了数组的范围，则会发生未定义行为[\[1\]](https://www.hiczp.com/c-cpp/c-yu-yan-chang-jian-wei-ding-yi-hang-wei.html)[\[2\]](https://c-cpp.com/c/language/behavior)[\[3\]](https://www.nowcoder.com/questionTerminal/8e273aeb2b4147fea72ff08814fc78e6)。
      * 2\. 修改一个变量两次而没有使用中间值：例如 `i = i++` 这样的代码是未定义的[\[4\]](https://blog.csdn.net/houzijushi/article/details/102754339)。
      * 3\. 在表达式中修改变量并且没有指定顺序：例如 \`j=j++\` 这样的代码也是未定义的[\[1\]](https://www.hiczp.com/c-cpp/c-yu-yan-chang-jian-wei-ding-yi-hang-wei.html)[\[2\]](https://c-cpp.com/c/language/behavior)。
      * 4\. 使用空指针或释放已经释放过的指针：这些都是未定义行为，可能导致程序崩溃或者产生其他错误[\[1\]](https://www.hiczp.com/c-cpp/c-yu-yan-chang-jian-wei-ding-yi-hang-wei.html)[\[3\]](https://www.nowcoder.com/questionTerminal/8e273aeb2b4147fea72ff08814fc78e6)。
      * 5\. 对于没有初始化的变量进行读取操作：这个行为也是未定义的，因为它依赖于编译器和运行时环境[\[1\]](https://www.hiczp.com/c-cpp/c-yu-yan-chang-jian-wei-ding-yi-hang-wei.html)。
      * 6\. 有符号整数溢出：当有符号整数类型发生溢出时，结果是未定义的[\[2\]](https://c-cpp.com/c/language/behavior)。
      * 7\. 解引用空指针或者解引用一个超出数组边界或者解引用一个未初始化指针等指针相关操作都属于未定义行为[\[3\]](https://www.nowcoder.com/questionTerminal/8e273aeb2b4147fea72ff08814fc78e6)[\[5\]](https://juejin.cn/post/7031078151841120264)。需要注意的是，在不同编译器上或者不同操作系统或者不同架构CPU上会产生不同结果。因此，在编写 C 代码时应该尽量避免使用未定义行为，并且要注意不同编译器之间可能存在差异。
        * 5 SOURCESView List1![hiczp.com favicon](https://www.google.com/s2/favicons?domain=hiczp.com)hiczp2![c-cpp.com favicon](https://www.google.com/s2/favicons?domain=c-cpp.com)c-cpp3![nowcoder.com favicon](https://www.google.com/s2/favicons?domain=nowcoder.com)nowcoder4![csdn.net favicon](https://www.google.com/s2/favicons?domain=csdn.net)csdn5![juejin.cn favicon](https://www.google.com/s2/favicons?domain=juejin.cn)juejin
* 分别说明未定义操作在不同编译器下有什么结果
* 从汇编代码来讨论其结果不同的原因。（可在![](file:///C:/Users/qq/AppData/Roaming/Tencent/QQ/Temp/%W@GJ$ACOF\(TYDYECOKVDYB.png)https://godbolt.org/上获取不同编译器的结果）（这个可以现场编译一下，展示汇编代码的区别？）



## 二、剧本制作

## 三、材料收集（将收集好的材料按照二级标题分类存档）

### 3.1 小班题目相关

### 3.2 汇编指令相关

### 3.3 未定义操作相关

### 3.4 拓展阅读相关
