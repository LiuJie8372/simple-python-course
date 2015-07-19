# 例 10.1 备份脚本——版本一

```

    #!/usr/bin/python
    # Filename: backup_ver1.py
    
    import os
    import time
    
    # 1. The files and directories to be backed up are specified in a list.
    source = ['/home/swaroop/byte', '/home/swaroop/bin']
    # If you are using Windows, use source = [r'C:\Documents', r'D:\Work'] or something like that
    
    # 2. The backup must be stored in a main backup directory
    target_dir = '/mnt/e/backup/' # Remember to change this to what you will be using
    
    # 3. The files are backed up into a zip file.
    # 4. The name of the zip archive is the current date and time
    target = target_dir + time.strftime('%Y%m%d%H%M%S') + '.zip'
    
    # 5. We use the zip command (in Unix/Linux) to put the files in a zip archive
    zip_command = "zip -qr '%s' %s" % (target, ' '.join(source))
    
    # Run the backup
    if os.system(zip_command) == 0:
        print 'Successful backup to', target
    else:
        print 'Backup FAILED'

```

（源文件：[code/backup_ver1.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/backup_ver1.py)）

**输出**

```

    $ python backup_ver1.py
    Successful backup to /mnt/e/backup/20041208073244.zip

```

现在，我们已经处于**测试**环节了，在这个环节，我们测试我们的程序是否正确工作。如果它与我们所期望的不一样，我们就得**调试**我们的程序，即消除程序中的 *瑕疵* （错误）。

**它如何工作**

接下来你将看到我们如何把 设计 一步一步地转换为 代码 。

我们使用了 os 和 time 模块，所以我们输入它们。然后，我们在 source 列表中指定需要备份的文件和目录。目标目录是我们想要存储备份文件的地方，它由 target_dir 变量指定。zip 归档的名称是目前的日期和时间，我们使用 time.strftime()函数获得。它还包括.zip 扩展名，将被保存在 target_dir 目录中。

time.strftime()函数需要我们在上面的程序中使用的那种定制。%Y 会被无世纪的年份所替代。%m 会被 01 到 12 之间的一个十进制月份数替代，其他依次类推。这些定制的详细情况可以在《Python 参考手册》中获得。《Python 参考手册》包含在你的 Python 发行版中。注意这些定制与用于 print 语句的定制（%后跟一个元组）类似（但不完全相同）

我们使用加法操作符来 *级连* 字符串，即把两个字符串连接在一起返回一个新的字符串。通过这种方式，我们创建了目标 zip 文件的名称。接着我们创建了 zip_command 字符串，它包含我们将要执行的命令。你可以在 shell（Linux 终端或者 DOS 提示符）中运行它，以检验它是否工作。

**zip** 命令有一些选项和参数。-q 选项用来表示 zip 命令**安静地**工作。-r 选项表示 zip 命令对目录**递归地**工作，即它包括子目录以及子目录中的文件。两个选项可以组合成缩写形式-qr。选项后面跟着待创建的 zip 归档的名称，然后再是待备份的文件和目录列表。我们使用已经学习过的字符串 join 方法把 source 列表转换为字符串。

最后，我们使用 os.system 函数 运行 命令，利用这个函数就好像在 *系统* 中运行命令一样。即在 shell 中运行命令——如果命令成功运行，它返回 0，否则它返回错误号。

根据命令的输出，我们打印对应的消息，显示备份是否创建成功。好了，就是这样我们已经创建了一个脚本来对我们的重要文件做备份！

> **给 Windows 用户的注释**  
你可以把 source 列表和 target 目录设置成任何文件和目录名，但是在 Windows 中你得小心一些。问题是 Windows 把反斜杠（\）作为目录分隔符，而 Python 用反斜杠表示转义符！
所以，你得使用转义符来表示反斜杠本身或者使用自然字符串。例如，使用'C:\\Documents'或r'C:\Documents'而**不是**'C:\Documents'——你在使用一个不知名的转义符\D！

现在我们已经有了一个可以工作的备份脚本，我们可以在任何我们想要建立文件备份的时候使用它。建议 Linux/Unix 用户使用前面介绍的[可执行的方法](http://woodpecker.org.cn/abyteofpython_cn/chinese/ch03s05.html)，这样就可以在任何地方任何时候运行备份脚本了。这被称为软件的**实施**环节或**开发**环节。

上面的程序可以正确工作，但是（通常）第一个程序并不是与你所期望的完全一样。例如，可能有些问题你没有设计恰当，又或者你在输入代码的时候发生了一点错误，等等。正常情况下，你应该回到设计环节或者调试程序。