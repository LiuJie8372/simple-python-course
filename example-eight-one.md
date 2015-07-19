# 例 8.1 使用 sys 模块

```

    #!/usr/bin/python
    # Filename: using_sys.py

    import sys

    print 'The command line arguments are:'
    for i in sys.argv:
        print i

    print '\n\nThe PYTHONPATH is', sys.path, '\n'

```

（源文件：[code/using_sys.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/using_sys.py)）

**输出**

```

    $ python using_sys.py we are arguments
    The command line arguments are:
    using_sys.py
    we
    are
    arguments
    
    
    The PYTHONPATH is ['/home/swaroop/byte/code', '/usr/lib/python23.zip',
    '/usr/lib/python2.3', '/usr/lib/python2.3/plat-linux2',
    '/usr/lib/python2.3/lib-tk', '/usr/lib/python2.3/lib-dynload',
    '/usr/lib/python2.3/site-packages', '/usr/lib/python2.3/site-packages/gtk-2.0']

```

**它如何工作**

首先，我们利用 import 语句 *输入 sys 模块*。基本上，这句语句告诉 Python，我们想要使用这个模块。sys 模块包含了与 Python 解释器和它的环境有关的函数。

当 Python 执行 import sys 语句的时候，它在 sys.path 变量中所列目录中寻找 sys.py 模块。如果找到了这个文件，这个模块的主块中的语句将被运行，然后这个模块将能够被你 使用 。注意，初始化过程仅在我们 *第一次* 输入模块的时候进行。另外，“sys”是“system”的缩写。

sys 模块中的 argv 变量通过使用点号指明——sys.argv——这种方法的一个优势是这个名称不会与任何在你的程序中使用的 argv 变量冲突。另外，它也清晰地表明了这个名称是 sys 模块的一部分。

sys.argv 变量是一个字符串的 *列表*（列表会在后面的[章节](http://woodpecker.org.cn/abyteofpython_cn/chinese/ch09s02.html)详细解释）。特别地，sys.argv 包含了 *命令行参数* 的列表，即使用命令行传递给你的程序的参数。

如果你使用 IDE 编写运行这些程序，请在菜单里寻找一个指定程序的命令行参数的方法。

这里，当我们执行 python using_sys.py we are arguments 的时候，我们使用 **python** 命令运行 using_sys.py 模块，后面跟着的内容被作为参数传递给程序。Python 为我们把它存储在 sys.argv 变量中。

记住，脚本的名称总是 sys.argv 列表的第一个参数。所以，在这里，'using_sys.py'是sys.argv[0]、'we'是 sys.argv[1]、'are'是sys.argv[2]以及'arguments'是 sys.argv[3]。注意，Python 从 0 开始计数，而非从 1 开始。

sys.path 包含输入模块的目录名列表。我们可以观察到 sys.path 的第一个字符串是空的——这个空的字符串表示当前目录也是 sys.path 的一部分，这与 PYTHONPATH 环境变量是相同的。这意味着你可以直接输入位于当前目录的模块。否则，你得把你的模块放在 sys.path 所列的目录之一。
