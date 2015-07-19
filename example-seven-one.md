# 例 7.1 定义函数

```

    #!/usr/bin/python
    # Filename: function1.py
    
    def sayHello():
        print 'Hello World!' # block belonging to the function
    
    sayHello() # call the function

```

（源文件：[code/function1.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/function1.py)）

**输出**

```

    $ python function1.py
    Hello World!

```

**它如何工作**

我们使用上面解释的语法定义了一个称为 sayHello 的函数。这个函数不使用任何参数，因此在圆括号中没有声明任何变量。参数对于函数而言，只是给函数的输入，以便于我们可以传递不同的值给函数，然后得到相应的结果。
