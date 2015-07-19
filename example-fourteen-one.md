# 例 14.1 使用 sys.argv

```

    #!/usr/bin/python
    # Filename: cat.py
    
    import sys
    
    def readfile(filename):
    '''Print a file to the standard output.'''
    f = file(filename)
    while True:
    line = f.readline()
    if len(line) == 0:
    break
    print line, # notice comma
    f.close()
    
    # Script starts from here
    if len(sys.argv) < 2:
    print 'No action specified.'
    sys.exit()
    
    if sys.argv[1].startswith('--'):
    option = sys.argv[1][2:]
    # fetch sys.argv[1] but without the first two characters
    if option == 'version':
    print 'Version 1.2'
    elif option == 'help':
    print '''\
    This program prints files to the standard output.
    Any number of files can be specified.
    Options include:
      --version : Prints the version number
      --help: Display this help'''
    else:
    print 'Unknown option.'
    sys.exit()
    else:
    for filename in sys.argv[1:]:
    readfile(filename)

```

（源文件：[code/cat.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/cat.py)）

**输出**

```

    $ python cat.py
    No action specified.
    
    $ python cat.py --help
    This program prints files to the standard output.
    Any number of files can be specified.
    Options include:
      --version : Prints the version number
      --help    : Display this help

    $ python cat.py --version
    Version 1.2
    
    $ python cat.py --nonsense
    Unknown option.
    
    $ python cat.py poem.txt
    Programming is fun
    When the work is done
    if you wanna make your work also fun:
            use Python!

```

**它如何工作**

这个程序用来模范 Linux/Unix 用户熟悉的 cat 命令。你只需要指明某些文本文件的名字，这个程序会把它们打印输出。

在 Python 程序运行的时候，即不是在交互模式下，在 sys.argv 列表中总是至少有一个项目。它就是当前运行的程序名称，作为 sys.argv[0]（由于 Python 从 0 开始计数）。其他的命令行参数在这个项目之后。

为了使这个程序对用户更加友好，我们提供了一些用户可以指定的选项来了解更多程序的内容。我们使用第一个参数来检验我们的程序是否被指定了选项。如果使用了--version 选项，程序的版本号将被打印出来。类似地，如果指定了--help 选项，我们提供一些关于程序的解释。我们使用 sys.exit 函数退出正在运行的程序。和以往一样，你可以看一下 help(sys.exit)来了解更多详情。

如果没有指定任何选项，而是为程序提供文件名的话，它就简单地打印出每个文件地每一行，按照命令行中的顺序一个文件接着一个文件地打印。

顺便说一下，名称 cat 是 concatenate 的缩写，它基本上表明了程序的功能——它可以在输出打印一个文件或者把两个或两个以上文件连接/级连在一起打印。
     