# 例 6.1 使用 if 语句

```

    #!/usr/bin/python
    # Filename: if.py 
    
    number = 23
    guess = int(raw_input('Enter an integer : '))
    
    if guess == number:
    print 'Congratulations, you guessed it.' # New block starts here
    print "(but you do not win any prizes!)" # New block ends here
    elif guess < number:
    print 'No, it is a little higher than that' # Another block
    # You can do whatever you want in a block ...
    else:
    print 'No, it is a little lower than that' 
    # you must have guess > number to reach here
    
    print 'Done'
    # This last statement is always executed, after the if statement is executed
     
```

（源文件：[code/if.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/if.py)）

**输出**

```

    $ python if.py
    Enter an integer : 50
    No, it is a little lower than that
    Done
    $ python if.py
    Enter an integer : 22
    No, it is a little higher than that
    Done
    $ python if.py
    Enter an integer : 23
    Congratulations, you guessed it.
    (but you do not win any prizes!)
    Done

```


**它如何工作**

在这个程序中，我们从用户处得到猜测的数，然后检验这个数是否是我们手中的那个。我们把变量 number 设置为我们想要的任何整数，在这个例子中是 23。然后，我们使用 raw_input()函数取得用户猜测的数字。函数只是重用的程序段。我们将在[下一章](http://woodpecker.org.cn/abyteofpython_cn/chinese/ch06.html)学习更多关于函数的知识。

我们为内建的 raw_input 函数提供一个字符串，这个字符串被打印在屏幕上，然后等待用户的输入。一旦我们输入一些东西，然后按**回车**键之后，函数返回输入。对于 raw_input 函数来说是一个字符串。我们通过 int 把这个字符串转换为整数，并把它存储在变量 guess 中。事实上，int 是一个类，不过你想在对它所需了解的只是它把一个字符串转换为一个整数（假设这个字符串含有一个有效的整数文本信息）。

接下来，我们将用户的猜测与我们选择的数做比较。如果他们相等，我们打印一个成功的消息。注意我们使用了缩进层次来告诉 Python 每个语句分别属于哪一个块。这就是为什么缩进在 Python 如此重要的原因。我希望你能够坚持“每个缩进层一个制表符”的规则。你是这样的吗？

注意 if 语句在结尾处包含一个冒号——我们通过它告诉 Python 下面跟着一个语句块。

然后，我们检验猜测是否小于我们的数，如果是这样的，我们告诉用户它的猜测大了一点。我们在这里使用的是 elif 从句，它事实上把两个相关联的 if else-if else 语句合并为一个 if-elif-else 语句。这使得程序更加简单，并且减少了所需的缩进数量。

elif 和 else 从句都必须在逻辑行结尾处有一个冒号，下面跟着一个相应的语句块（当然还包括正确的缩进）。

你也可以在一个 if 块中使用另外一个 if 语句，等等——这被称为嵌套的 if 语句。

记住，elif 和 else 部分是可选的。一个最简单的有效 if 语句是：

```

    if True:
        print 'Yes, it is true'

```

在 Python 执行完一个完整的 if 语句以及与它相关联的 elif 和 else 从句之后，它移向 if 语句块的下一个语句。在这个例子中，这个语句块是主块。程序从主块开始执行，而下一个语句是 print 'Done'语句。在这之后，Python 看到程序的结尾，简单的结束运行。

尽管这是一个非常简单的程序，但是我已经在这个简单的程序中指出了许多你应该注意的地方。所有这些都是十分直接了当的（对于那些拥有 C/C++背景的用户来说是尤为简单的）。它们在开始时会引起你的注意，但是以后你会对它们感到熟悉、“自然”。

> **给C/C++程序员的注释**  
在 Python 中没有 switch 语句。你可以使用 if..elif..else 语句来完成同样的工作（在某些场合，使用[字典](http://woodpecker.org.cn/abyteofpython_cn/chinese/ch09s04.html)会更加快捷。）