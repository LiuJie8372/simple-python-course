# 例 13.1 处理异常

```

    #!/usr/bin/python
    # Filename: try_except.py
    
    import sys
    
    try:
        s = raw_input('Enter something --> ')
    except EOFError:
        print '\nWhy did you do an EOF on me?'
        sys.exit() # exit the program
    except:
        print '\nSome error/exception occurred.'
        # here, we are not exiting the program

    print 'Done'

```

（源文件：[code/try_except.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/try_except.py)）

**输出**

```

    $ python try_except.py
    Enter something -->
    Why did you do an EOF on me?
    
    $ python try_except.py
    Enter something --> Python is exceptional!
    Done

```

**它如何工作**

我们把所有可能引发错误的语句放在 try 块中，然后在 except 从句/块中处理所有的错误和异常。 except 从句可以专门处理单一的错误或异常，或者一组包括在圆括号内的错误/异常。如果没有给出错误或异常的名称，它会处理 *所有的* 错误和异常。对于每个 try 从句，至少都有一个相关联的  except 从句。

如果某个错误或异常没有被处理，默认的 Python 处理器就会被调用。它会终止程序的运行，并且打印一个消息，我们已经看到了这样的处理。

你还可以让 try..catch 块关联上一个 else 从句。当没有异常发生的时候，else 从句将被执行。

我们还可以得到异常对象，从而获取更多有个这个异常的信息。这会在下一个例子中说明。
