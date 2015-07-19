# 例 6.4 使用 break 语句

```

    #!/usr/bin/python
    # Filename: break.py
    
    while True:
    s = raw_input('Enter something : ')
    if s == 'quit':
    break
    print 'Length of the string is', len(s)
    print 'Done'

```

（源文件：[code/break.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/break.py)）

**输出**

```

    $ python break.py
    Enter something : Programming is fun
    Length of the string is 18
    Enter something : When the work is done
    Length of the string is 21
    Enter something : if you wanna make your work also fun:
    Length of the string is 37
    Enter something :   use Python!
    Length of the string is 12
    Enter something : quit
    Done

```


**它如何工作**

在这个程序中，我们反复地取得用户地输入，然后打印每次输入地长度。我们提供了一个特别的条件来停止程序，即检验用户的输入是否是'quit'。通过 终止 循环到达程序结尾来停止程序。

输入字符串的长度通过内建的 len 函数取得。

记住，break 语句也可以在 for 循环中使用。

### G2 的 Python 诗

我在这里输入的是我所写的一段小诗，称为 **G2 的 Python 诗**：

```

    Programming is fun
    When the work is done
    if you wanna make your work also fun:
      use Python!

```