例 8.2 使用模块的__name__

```

    #!/usr/bin/python
    # Filename: using_name.py

    if __name__ == '__main__':
        print 'This program is being run by itself'
     else:
        print 'I am being imported from another module'

```

（源文件：[code/using_name.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/using_name.py)）

**输出**

    $ python using_name.py
    This program is being run by itself
    
    $ python
    >>> import using_name
    I am being imported from another module
    >>>

｀｀｀

**它如何工作**

每个 Python 模块都有它的__name__，如果它是'__main__'，这说明这个模块被用户单独运行，我们可以进行相应的恰当操作。
