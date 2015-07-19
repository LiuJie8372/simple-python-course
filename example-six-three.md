# 例 6.3 使用 for 语句

```

    #!/usr/bin/python
    # Filename: for.py
    
    for i in range(1, 5):
        print i
    else:
        print 'The for loop is over'

```

**输出**

```

    $ python for.py
    1
    2
    3
    4
    The for loop is over

```


**它如何工作**

在这个程序中，我们打印了一个 序列 的数。我们使用内建的 range 函数生成这个数的序列。

我们所做的只是提供两个数，range 返回一个序列的数。这个序列从第一个数开始到第二个数为止。例如，range(1,5)给出序列[1, 2, 3, 4]。默认地，range 的步长为 1。如果我们为range 提供第三个数，那么它将成为步长。例如，range(1,5,2)给出[1,3]。记住，range 向上 延伸到第二个数，即它**不**包含第二个数。

for 循环在这个范围内递归—— for i in range(1,5)等价于 for i in [1, 2, 3, 4]，这就如同把序列中的每个数（或对象）赋值给 i，一次一个，然后以每个 i 的值执行这个程序块。在这个例子中，我们只是打印 i 的值。

记住，else 部分是可选的。如果包含 else，它总是在 for 循环结束后执行一次，除非遇到 [break](http://woodpecker.org.cn/abyteofpython_cn/chinese/ch06s05.html) 语句。

记住，for..in 循环对于任何序列都适用。这里我们使用的是一个由内建 range 函数生成的数的列表，但是广义说来我们可以使用任何种类的由任何对象组成的序列！我们会在后面的章节中详细探索这个观点。

> **给 C/C++/Java/C#程序员的注释**  
Python 的 for 循环从根本上不同于 C/C++的 for 循环。C#程序员会注意到 Python 的 for 循环与 C#中的 foreach 循环十分类似。Java 程序员会注意到它与 Java 1.5 中的 for (int i : IntArray)相似。
在 C/C++中，如果你想要写 for (int i = 0; i < 5; i++)，那么用 Python，你写成 for i in range(0,5)。你会注意到，Python 的 for 循环更加简单、明白、不易出错。
