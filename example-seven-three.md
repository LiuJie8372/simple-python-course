例 7.3 使用局部变量

```

    #!/usr/bin/python
    # Filename: func_local.py
    
    def func(x):
        print 'x is', x
        x = 2
         print 'Changed local x to', x
    
    x = 50
    func(x)
    print 'x is still', x

```

（源文件：[code/func_local.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/func_local.py)）

**输出**

```

    $ python func_local.py
    x is 50
    Changed local x to 2
    x is still 50

```

**它如何工作**

在函数中，我们第一次使用 x 的 *值* 的时候，Python 使用函数声明的形参的值。

接下来，我们把值 2 赋给 x。x 是函数的局部变量。所以，当我们在函数内改变 x 的值的时候，在主块中定义的 x 不受影响。

在最后一个 print 语句中，我们证明了主块中的 x 的值确实没有受到影响。
