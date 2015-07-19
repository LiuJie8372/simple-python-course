# 例 7.4 使用 global 语句

```

    #!/usr/bin/python
    # Filename: func_global.py
    
    def func():
        global x
    
        print 'x is', x
        x = 2
        print 'Changed local x to', x
    
        x = 50
    func()
    print 'Value of x is', x

```


（源文件：[code/func_global.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/func_global.py)）

**输出**

```

    $ python func_global.py
    x is 50
    Changed global x to 2
    Value of x is 2

```

**它如何工作**

global 语句被用来声明x是全局的——因此，当我们在函数内把值赋给x的时候，这个变化也反映在我们在主块中使用 x 的值的时候。

你可以使用同一个 global 语句指定多个全局变量。例如 global x, y, z。
