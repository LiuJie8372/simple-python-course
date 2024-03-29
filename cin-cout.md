# 输入/输出

在很多时候，你会想要让你的程序与用户（可能是你自己）交互。你会从用户那里得到输入，然后打印一些结果。我们可以分别使用 raw_input 和 print 语句来完成这些功能。对于输出，你也可以使用多种多样的 str（字符串）类。例如，你能够使用 rjust 方法来得到一个按一定宽度右对齐的字符串。利用 help(str)获得更多详情。

另一个常用的输入/输出类型是处理文件。创建、读和写文件的能力是许多程序所必需的，我们将会在这章探索如何实现这些功能。

## 文件
你可以通过创建一个 file 类的对象来打开一个文件，分别使用 file 类的 read、readline 或 write 方法来恰当地读写文件。对文件的读写能力依赖于你在打开文件时指定的模式。最后，当你完成对文件的操作的时候，你调用 close 方法来告诉 Python 我们完成了对文件的使用。
     
### 使用文件

**例 12.1 使用文件**

```

    #!/usr/bin/python
    # Filename: using_file.py
    
    poem = '''\
    Programming is fun
    When the work is done
    if you wanna make your work also fun:
        use Python!
    '''
    
    f = file('poem.txt', 'w') # open for 'w'riting
    f.write(poem) # write text to file
    f.close() # close the file
    
    f = file('poem.txt')
    # if no mode is specified, 'r'ead mode is assumed by default
    while True:
    line = f.readline()
    if len(line) == 0: # Zero length indicates EOF
        break
    print line,
    # Notice comma to avoid automatic newline added by Python
    f.close() # close the file

```


（源文件：[code/using_file.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/using_file.py)）

**输出**

```

    $ python using_file.py
    Programming is fun
    When the work is done
    if you wanna make your work also fun:
        use Python!

```

**它如何工作**

首先，我们通过指明我们希望打开的文件和模式来创建一个 file 类的实例。模式可以为读模式（'r'）、写模式（'w'）或追加模式（'a'）。事实上还有多得多的模式可以使用，你可以使用 help(file)来了解它们的详情。

我们首先用写模式打开文件，然后使用 file 类的 write 方法来写文件，最后我们用 close 关闭这个文件。

接下来，我们再一次打开同一个文件来读文件。如果我们没有指定模式，读模式会作为默认的模式。在一个循环中，我们使用 readline 方法读文件的每一行。这个方法返回包括行末换行符的一个完整行。所以，当一个 空的 字符串被返回的时候，即表示文件末已经到达了，于是我们停止循环。

注意，因为从文件读到的内容已经以换行符结尾，所以我们在 print 语句上使用逗号来消除自动换行。最后，我们用 close 关闭这个文件。

现在，来看一下 poem.txt 文件的内容来验证程序确实工作正常了

## 储存器

Python 提供一个标准的模块，称为 pickle。使用它你可以在一个文件中储存**任何** Python 对象，之后你又可以把它完整无缺地取出来。这被称为 *持久地* 储存对象。

还有另一个模块称为 cPickle，它的功能和 pickle 模块完全相同，只不过它是用 C 语言编写的，因此要快得多（比pickle 快 1000 倍）。你可以使用它们中的任一个，而我们在这里将使用 cPickle 模块。记住，我们把这两个模块都简称为 pickle 模块。
     
### 储存与取储存

**例 12.2 储存与取储存**

```

    #!/usr/bin/python
    # Filename: pickling.py
    
    import cPickle as p
    #import pickle as p
    
    shoplistfile = 'shoplist.data'
    # the name of the file where we will store the object
    
    shoplist = ['apple', 'mango', 'carrot']
    
    # Write to the file
    f = file(shoplistfile, 'w')
    p.dump(shoplist, f) # dump the object to a file
    f.close()
    
    del shoplist # remove the shoplist
    
    # Read back from the storage
    f = file(shoplistfile)
    storedlist = p.load(f)
    print storedlist

```

（源文件：[code/pickling.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/pickling.py)）

**输出**

```

    $ python pickling.py
    ['apple', 'mango', 'carrot']

```

**它如何工作**

首先，请注意我们使用了 import..as 语法。这是一种便利方法，以便于我们可以使用更短的模块名称。在这个例子中，它还让我们能够通过简单地改变一行就切换到另一个模块（cPickle 或者 pickle）！在程序的其余部分的时候，我们简单地把这个模块称为 p。

为了在文件里储存一个对象，首先以写模式打开一个 file 对象，然后调用储存器模块的 dump 函数，把对象储存到打开的文件中。这个过程称为 *储存* 。

接下来，我们使用 pickle 模块的 load 函数的返回来取回对象。这个过程称为 *取储存* 。



## 概括

我们已经讨论了多种类型的输入/输出，及文件处理和使用储存器模块。

接下来，我们将探索异常的概念。

