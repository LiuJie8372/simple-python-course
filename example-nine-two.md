# 例 9.2 使用元组

```

    #!/usr/bin/python
    # Filename: using_tuple.py
    
    zoo = ('wolf', 'elephant', 'penguin')
    print 'Number of animals in the zoo is', len(zoo)
    
    new_zoo = ('monkey', 'dolphin', zoo)
    print 'Number of animals in the new zoo is', len(new_zoo)
    print 'All animals in new zoo are', new_zoo
    print 'Animals brought from old zoo are', new_zoo[2]
    print 'Last animal brought from old zoo is', new_zoo[2][2]

```

（源文件：[code/using_tuple.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/using_tuple.py)）

**输出**

```

    $ python using_tuple.py
    Number of animals in the zoo is 3
    Number of animals in the new zoo is 3
    All animals in new zoo are ('monkey', 'dolphin', ('wolf', 'elephant', 'penguin'))
    Animals brought from old zoo are ('wolf', 'elephant', 'penguin')
    Last animal brought from old zoo is penguin

```


**它如何工作**

变量 zoo 是一个元组，我们看到 len 函数可以用来获取元组的长度。这也表明元组也是一个[序列](http://woodpecker.org.cn/abyteofpython_cn/chinese/ch09s05.html)。

由于老动物园关闭了，我们把动物转移到新动物园。因此，new_zoo 元组包含了一些已经在那里的动物和从老动物园带过来的动物。回到话题，注意元组之内的元组不会失去它的身份。

我们可以通过一对方括号来指明某个项目的位置从而来访问元组中的项目，就像我们对列表的用法一样。这被称作 *索引* 运算符。我们使用 new_zoo[2]来访问 new_zoo 中的第三个项目。我们使用 new_zoo[2][2]来访问 new_zoo 元组的第三个项目的第三个项目。

**含有 0 个或 1 个项目的元组**。一个空的元组由一对空的圆括号组成，如 myempty = ()。然而，含有单个元素的元组就不那么简单了。你必须在第一个（唯一一个）项目后跟一个逗号，这样 Python 才能区分元组和表达式中一个带圆括号的对象。即如果你想要的是一个包含项目2的元组的时候，你应该指明 singleton = (2 , )。

> **给 Perl 程序员的注释**
列表之中的列表不会失去它的身份，即列表不会像 Perl 中那样被打散。同样元组中的元组，或列表中的元组，或元组中的列表等等都是如此。只要是 Python，它们就只是使用另一个对象存储的对象。
    