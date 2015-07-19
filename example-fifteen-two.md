# 例 15.2 使用 lambda 形式

```

    #!/usr/bin/python
    # Filename: lambda.py
    
    def make_repeater(n):
        return lambda s: s*n
    
    twice = make_repeater(2)
    
    print twice('word')
    print twice(5)

```

（源文件：[code/lambda.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/lambda.py)）

**输出**

```

    $ python lambda.py
    wordword
    10

```

**它如何工作**

这里，我们使用了 make_repeater 函数在运行时创建新的函数对象，并且返回它。lambda 语句用来创建函数对象。本质上，lambda 需要一个参数，后面仅跟单个表达式作为函数体，而表达式的值被这个新建的函数返回。注意，即便是 print 语句也不能用在 lambda 形式中，只能使用表达式。
