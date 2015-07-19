# 例 5.1 使用表达式

```

    #!/usr/bin/python
    # Filename: expression.py
    
    length = 5
    breadth = 2
    area = length * breadth
    print 'Area is', area
    print 'Perimeter is', 2 * (length + breadth)

```

（源文件：[code/expression.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/expression.py)）

**输出**

```

    $ python expression.py
    Area is 10
    Perimeter is 14

```

**它如何工作**

矩形的长度与宽度存储在以它们命名的变量中。我们借助表达式使用它们计算矩形的面积和边长。我们表达式 length * breadth 的结果存储在变量 area 中，然后用 print 语句打印。在另一个打印语句中，我们直接使用表达式 2 * (length + breadth)的值。

另外，注意 Python 如何打印“漂亮的”输出。尽管我们没有在'Area is'和变量 area 之间指定空格，Python 自动在那里放了一个空格，这样我们就可以得到一个清晰漂亮的输出，而程序也变得更加易读（因为我们不需要担心输出之间的空格问题）。这是 Python 如何使程序员的生活变得更加轻松的一个例子。
