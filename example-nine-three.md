# 例 9.3 使用元组输出

```

    #!/usr/bin/python
    # Filename: print_tuple.py
    
    age = 22
    name = 'Swaroop'
    
    print '%s is %d years old' % (name, age)
    print 'Why is %s playing with that python?' % name

```

（源文件：code/print_tuple.py）

**输出**

```

    $ python print_tuple.py
    Swaroop is 22 years old
    Why is Swaroop playing with that python?

```

**它如何工作**

print 语句可以使用跟着%符号的项目元组的字符串。这些字符串具备定制的功能。定制让输出满足某种特定的格式。定制可以是%s 表示字符串或%d表示整数。元组必须按照相同的顺序来对应这些定制。

观察我们使用的第一个元组，我们首先使用%s，这对应变量 name，它是元组中的第一个项目。而第二个定制是%d，它对应元组的第二个项目 age。

Python 在这里所做的是把元组中的每个项目转换成字符串并且用字符串的值替换定制的位置。因此%s 被替换为变量 name 的值，依此类推。

print 的这个用法使得编写输出变得极其简单，它避免了许多字符串操作。它也避免了我们一直以来使用的逗号。

在大多数时候，你可以只使用%s 定制，而让 Python 来提你处理剩余的事情。这种方法对数同样奏效。然而，你可能希望使用正确的定制，从而可以避免多一层的检验程序是否正确。

在第二个print语句中，我们使用了一个定制，后面跟着%符号后的单个项目——没有圆括号。这只在字符串中只有一个定制的时候有效。