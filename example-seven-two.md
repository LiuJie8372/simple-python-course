# 7.2 使用函数形参

```

    #!/usr/bin/python
    # Filename: func_param.py
    
        def printMax(a, b):
          if a > b:
              print a, 'is maximum'
          else:
              print b, 'is maximum'
    
    printMax(3, 4) # directly give literal values
    
    x = 5
    y = 7
    
    printMax(x, y) # give variables as arguments

```


（源文件：[code/func_param.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/func_param.py)）

**输出**

```

    $ python func_param.py
    4 is maximum
    7 is maximum

```

**它如何工作**

这里，我们定义了一个称为 printMax 的函数，这个函数需要两个形参，叫做 a 和 b。我们使用 if..else 语句找出两者之中较大的一个数，并且打印较大的那个数。

在第一个 printMax 使用中，我们直接把数，即实参，提供给函数。在第二个使用中，我们使用变量调用函数。printMax(x, y)使实参 x 的值赋给形参a，实参y的值赋给形参 b。在两次调用中，printMax 函数的工作完全相同。