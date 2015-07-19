# 例 11.2 使用对象的方法

```

    #!/usr/bin/python
    # Filename: method.py

    class Person:
        def sayHi(self):
            print 'Hello, how are you?'

    p = Person()
    p.sayHi()

    # This short example can also be written as Person().sayHi()

```

（源文件：[code/method.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/method.py)）

**输出**

```

    $ python method.py
    Hello, how are you?

```

**它如何工作**

这里我们看到了 self 的用法。注意 sayHi 方法没有任何参数，但仍然在函数定义时有 self。

