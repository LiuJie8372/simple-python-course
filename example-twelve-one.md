# 例 12.1 使用文件

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
