# 例 3.2 使用源文件

```

    #!/usr/bin/python
    # Filename : helloworld.py
    print 'Hello World'

```

（源文件：[code/helloworld.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/helloworld.py)）

为了运行这个程序，请打开 shell（Linux 终端或者 DOS 提示符），然后键入命令 python helloworld.py。如果你使用 IDLE，请使用菜单 Edit->Run Script 或者使用键盘快捷方式 Ctrl-F5。输出如下所示。


**输出**

```

    $ python helloworld.py
    Hello World

```

如果你得到的输出与上面所示的一样，那么恭喜！——你已经成功地运行了你的第一个 Python 程序。

万一你得到一个错误，那么请确保你键入的程序 准确无误 ，然后再运行一下程序。注意 Python 是大小写敏感的，即 print 与 Print 不一样——注意前一个是小写 p 而后一个是大写 P。另外，确保在每一行的开始字符前没有空格或者制表符——我们将在后面讨论为什么这点是重要的。

**它如何工作**

让我们思考一下这个程序的前两行。它们被称作 注释 ——任何在#符号右面的内容都是注释。注释主要作为提供给程序读者的笔记。

Python 至少应当有第一行那样的特殊形式的注释。它被称作 组织行 ——源文件的头两个字符是#!，后面跟着一个程序。这行告诉你的 Linux/Unix 系统当你 执行 你的程序的时候，它应该运行哪个解释器。这会在下一节做详细解释。注意，你总是可以通过直接在命令行指定解释器，从而在任何平台上运行你的程序。就如同命令 ***python helloworld.py*** 一样。

> **重要**  
在你的程序中合理地使用注释以解释一些重要的细节——这将有助于你的程序的读者轻松地理解程序在干什么。记住，这个读者可能就是 6 个月以后的你！

跟在注释之后的是一句 Python 语句 ——它只是打印文本“Hello World”。print 实际上是一个操作符，而“Hello World”被称为一个字符串——别担心我们会在后面详细解释这些术语。


