# 例 8.3 如何创建你自己的模块

```

    #!/usr/bin/python
    # Filename: mymodule.py
    
    def sayhi():
        print 'Hi, this is mymodule speaking.'
    
    version = '0.1'
    
    # End of mymodule.py

```


（源文件：[code/mymodule.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/mymodule.py)）

上面是一个 模块 的例子。你已经看到，它与我们普通的 Python 程序相比并没有什么特别之处。我们接下来将看看如何在我们别的Python程序中使用这个模块。

记住这个模块应该被放置在我们输入它的程序的同一个目录中，或者在 sys.path 所列目录之一。

```

    #!/usr/bin/python
    # Filename: mymodule_demo.py
    
    import mymodule
    
    mymodule.sayhi()
    print 'Version', mymodule.version

```


（源文件：[code/mymodule_demo.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/mymodule_demo.py)）

**输出**

```

    $ python mymodule_demo.py
    Hi, this is mymodule speaking.
    Version 0.1

```

**它如何工作**

注意我们使用了相同的点号来使用模块的成员。Python 很好地重用了相同的记号来，使我们这些 Python 程序员不需要不断地学习新的方法。

### from..import

下面是一个使用 from..import 语法的版本。

```

    #!/usr/bin/python
    # Filename: mymodule_demo2.py
    
    from mymodule import sayhi, version
    # Alternative:
    # from mymodule import *
    
    sayhi()
    print 'Version', version

```

（源文件：[code/mymodule_demo2.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/mymodule_demo2.py)）

mymodule_demo2.py 的输出与 mymodule_demo.py 完全相同。