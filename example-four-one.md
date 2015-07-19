
# 例 4.1 使用变量和字面意义上的常量

```

    # Filename : var.py
    i = 5
    print i
    i = i + 1
    print i
    
    s = '''This is a multi-line string.
    This is the second line.'''
    print s
    
```

（源文件：[code/var.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/var.py)）


**输出**

```

    $ python var.py
    5
    6
    This is a multi-line string.
    This is the second line.

```
     
**它如何工作**

下面来说明一下这个程序如何工作。首先我们使用赋值运算符（=）把一个字面意义上的常数 5 赋给变量 i。这一行称为一个语句。语句声明需要做某件事情，在这个地方我们把变量名 i 与值 5 连接在一起。接下来，我们用print 语句打印 i 的值，就是把变量的值打印在屏幕上。

然后我们对i中存储的值加 1，再把它存回 i。我们打印它时，得到期望的值 6。

类似地，我们把一个字面意义上的字符串赋给变量 s 然后打印它。

> **给 C/C++程序员的注释**  
使用变量时只需要给它们赋一个值。不需要声明或定义数据类型。