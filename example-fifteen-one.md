# 例 15.1 使用列表综合

```

    #!/usr/bin/python
    # Filename: list_comprehension.py
    
    listone = [2, 3, 4]
    listtwo = [2*i for i in listone if i > 2]
    print listtwo

```

[（源文件：code/list_comprehension.py）](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/list_comprehension.py)

**输出**

```

    $ python list_comprehension.py
    [6, 8]

```

**它如何工作**

这里我们为满足条件（if i > 2）的数指定了一个操作（2*i），从而导出一个新的列表。注意原来的列表并没有发生变化。在很多时候，我们都是使用循环来处理列表中的每一个元素，而使用列表综合可以用一种更加精确、简洁、清楚的方法完成相同的工作。