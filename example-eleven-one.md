# 例 11.1 创建一个类

```

    #!/usr/bin/python
    # Filename: simplestclass.py

    class Person:
        pass # An empty block

    p = Person()
    print p

```

（源文件：[code/simplestclass.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/simplestclass.py)）

**输出**

```

    $ python simplestclass.py
    <__main__.Person instance at 0xf6fcb18c>

```

**它如何工作**

我们使用 class 语句后跟类名，创建了一个新的类。这后面跟着一个缩进的语句块形成类体。在这个例子中，我们使用了一个空白块，它由 pass 语句表示。

接下来，我们使用类名后跟一对圆括号来创建一个对象/实例。（我们将在下面的章节中学习[更多的如何创建实例的方法](http://woodpecker.org.cn/abyteofpython_cn/chinese/ch11s05.html)）。为了验证，我们简单地打印了这个变量的类型。它告诉我们我们已经在__main__模块中有了一个 Person 类的实例。

可以注意到存储对象的计算机内存地址也打印了出来。这个地址在你的计算机上会是另外一个值，因为 Python 可以在任何空位存储对象。