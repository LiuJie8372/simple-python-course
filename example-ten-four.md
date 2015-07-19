# 例 10.4 备份脚本——版本四

```

    #!/usr/bin/python
    # Filename: backup_ver4.py
    
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
        target = today + os.sep + now + '_' + \
            comment.replace(' ', '_') + '.zip'
        # Notice the backslash!

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

（源文件：[code/backup_ver4.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/backup_ver4.py)）

**输出**

```

    $ python backup_ver4.py
    Enter a comment --> added new examples
    Successful backup to /mnt/e/backup/20041208/082156_added_new_examples.zip
    
    $ python backup_ver4.py
    Enter a comment -->
    Successful backup to /mnt/e/backup/20041208/082316.zip

```

**它如何工作**

这个程序现在工作了！让我们看一下版本三中作出的实质性改进。我们使用 raw_input 函数得到用户的注释，然后通过 len 函数找出输入的长度以检验用户是否确实输入了什么东西。如果用户只是按了**回车**（比如这只是一个惯例备份，没有做什么特别的修改），那么我们就如之前那样继续操作。

然而，如果提供了注释，那么它会被附加到 zip 归档名，就在.zip 扩展名之前。注意我们把注释中的空格替换成下划线——这是因为处理这样的文件名要容易得多。