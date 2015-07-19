# 例 7.8 使用 DocStrings

```

    #!/usr/bin/python
    # Filename: func_doc.py
    
    def printMax(x, y):
        '''Prints the maximum of two numbers.
    
        The two values must be integers.'''
        x = int(x) # convert to integers, if possible
        y = int(y)
    
        if x > y:
             print x, 'is maximum'
        else:
             print y, 'is maximum'
    
    printMax(3, 5)
    print printMax.__doc__

```

（源文件：[code/func_doc.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/func_doc.py)）

**输出**

```

    $ python func_doc.py
    5 is maximum
    Prints the maximum of two numbers.
    
        The two values must be integers.

```


**它如何工作**

在函数的第一个逻辑行的字符串是这个函数的 文档字符串 。注意，DocStrings 也适用于[模块](http://woodpecker.org.cn/abyteofpython_cn/chinese/ch08.html)和[类](http://woodpecker.org.cn/abyteofpython_cn/chinese/ch11.html)，我们会在后面相应的章节学习它们。

文档字符串的惯例是一个多行字符串，它的首行以大写字母开始，句号结尾。第二行是空行，从第三行开始是详细的描述。 *强烈建议* 你在你的函数中使用文档字符串时遵循这个惯例。

你可以使用__doc__（注意双下划线）调用 printMax 函数的文档字符串属性（属于函数的名称）。请记住 Python 把 *每一样东西* 都作为对象，包括这个函数。我们会在后面的[类](http://woodpecker.org.cn/abyteofpython_cn/chinese/ch11.html)一章学习更多关于对象的知识。

如果你已经在 Python 中使用过 help()，那么你已经看到过 DocStings 的使用了！它所做的只是抓取函数的__doc__属性，然后整洁地展示给你。你可以对上面这个函数尝试一下——只是在你的程序中包括 help(printMax)。记住按 q 退出 help。

自动化工具也可以以同样的方式从你的程序中提取文档。因此，我 *强烈建议* 你对你所写的任何正式函数编写文档字符串。随你的 Python 发行版附带的 pydoc 命令，与 help()类似地使用 DocStrings。
