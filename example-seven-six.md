# 例 7.5 使用默认参数值

```

    #!/usr/bin/python
    # Filename: func_default.py
    
    def say(message, times = 1):
    print message * times
    
    say('Hello')
    say('World', 5)

```

（源文件：[code/func_default.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/func_default.py)）

**输出**

```

    $ python func_default.py
    Hello
    WorldWorldWorldWorldWorld

```

**它如何工作**

名为 say 的函数用来打印一个字符串任意所需的次数。如果我们不提供一个值，那么默认地，字符串将只被打印一遍。我们通过给形参 times 指定默认参数值1来实现这一功能。

在第一次使用 say 的时候，我们只提供一个字符串，函数只打印一次字符串。在第二次使用 say 的时候，我们提供了字符串和参数 5，表明我们想要 *说* 这个字符串消息5遍。

> **重要 ** 
只有在形参表末尾的那些参数可以有默认参数值，即你不能在声明函数形参的时候，先声明有默认值的形参而后声明没有默认值的形参。
这是因为赋给形参的值是根据位置而赋值的。例如，def func(a, b=5)是有效的，但是 def func(a=5, b)是 *无效* 的。