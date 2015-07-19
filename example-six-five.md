# 例 6.5 使用 continue 语句

```

    #!/usr/bin/python
    # Filename: continue.py
    
    while True:
        s = raw_input('Enter something : ')
        if s == 'quit':
            break
        if len(s) < 3:
            continue
    print 'Input is of sufficient length'
    # Do other kinds of processing here...

```

（源文件：[code/continue.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/continue.py)）

**输出**

```

    $ python continue.py
    Enter something : a
    Enter something : 12
    Enter something : abc
    Input is of sufficient length
    Enter something : quit

```

**它如何工作**

在这个程序中，我们从用户处取得输入，但是我们仅仅当它们有至少 3 个字符长的时候才处理它们。所以，我们使用内建的 len 函数来取得长度。如果长度小于 3，我们将使用 continue 语句忽略块中的剩余的语句。否则，这个循环中的剩余语句将被执行，我们可以在这里做我们希望的任何处理。

注意，continue 语句对于 for 循环也有效。