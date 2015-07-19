# 例 10.3 备份脚本——版本三（不工作！）

```

    #!/usr/bin/python
    # Filename: backup_ver3.py
    
    import os
    import time
    
    # 1. The files and directories to be backed up are specified in a list.
    source = ['/home/swaroop/byte', '/home/swaroop/bin']
    # If you are using Windows, use source = [r'C:\Documents', r'D:\Work'] or something like that
    
    # 2. The backup must be stored in a main backup directory
    target_dir = '/mnt/e/backup/' # Remember to change this to what you will be using
    
    # 3. The files are backed up into a zip file.
    # 4. The current day is the name of the subdirectory in the main directory
    today = target_dir + time.strftime('%Y%m%d')
    # The current time is the name of the zip archive
    now = time.strftime('%H%M%S')
    
    # Take a comment from the user to create the name of the zip file
    comment = raw_input('Enter a comment --> ')
    if len(comment) == 0: # check if a comment was entered
        target = today + os.sep + now + '.zip'
    else:
        target = today + os.sep + now + '_' +
            comment.replace(' ', '_') + '.zip'

    # Create the subdirectory if it isn't already there
    if not os.path.exists(today):
        os.mkdir(today) # make directory
        print 'Successfully created directory', today

    # 5. We use the zip command (in Unix/Linux) to put the files in a zip archive
    zip_command = "zip -qr '%s' %s" % (target, ' '.join(source))
    
    # Run the backup
    if os.system(zip_command) == 0:
        print 'Successful backup to', target
    else:
        print 'Backup FAILED'

```


（源文件：[code/backup_ver3.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/backup_ver3.py)）

**输出**

```

    $ python backup_ver3.py
    File "backup_ver3.py", line 25
    target = today + os.sep + now + '_' +
                                   ^
    SyntaxError: invalid syntax

```

**它如何（不）工作**

**这个程序不工作**！Python 说有一个语法错误，这意味着脚本不满足 Python 可以识别的结构。当我们观察 Python 给出的错误的时候，它也告诉了我们它检测出错误的位置。所以我们从那行开始 *调试* 我们的程序。

通过仔细的观察，我们发现一个逻辑行被分成了两个物理行，但是我们并没有指明这两个物理行属于同一逻辑行。基本上，Python 发现加法操作符（＋）在那一逻辑行没有任何操作数，因此它不知道该如何继续。记住我们可以使用物理行尾的反斜杠来表示逻辑行在下一物理行继续。所以，我们修正了程序。这被称为**修订**。
     