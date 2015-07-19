# 例 13.2 如何引发异常

```

    #!/usr/bin/python
    # Filename: raising.py

    class ShortInputException(Exception):
        '''A user-defined exception class.'''
        def __init__(self, length, atleast):
            Exception.__init__(self)
             self.length = length
            self.atleast = atleast

    try:
        s = raw_input('Enter something --> ')
        if len(s) < 3:
            raise ShortInputException(len(s), 3)
        # Other work can continue as usual here
    except EOFError:
        print '\nWhy did you do an EOF on me?'
    except ShortInputException, x:
        print 'ShortInputException: The input was of length %d, \
              was expecting at least %d' % (x.length, x.atleast)
    else:
        print 'No exception was raised.'

```

源文件（[code/raising.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/raising.py)）

**输出**

```

    $ python raising.py
    Enter something -->
    Why did you do an EOF on me?
    
    $ python raising.py
    Enter something --> ab
    ShortInputException: The input was of length 2, was expecting at least 3
    
    $ python raising.py
    Enter something --> abc
    No exception was raised.

```

**它如何工作**

这里，我们创建了我们自己的异常类型，其实我们可以使用任何预定义的异常/错误。这个新的异常类型是 ShortInputException 类。它有两个域—— length 是给定输入的长度，atleast 则是程序期望的最小长度。

在 except 从句中，我们提供了错误类和用来表示错误/异常对象的变量。这与函数调用中的形参和实参概念类似。在这个特别的 except 从句中，我们使用异常对象的 length 和 atleast 域来为用户打印一个恰当的消息。
