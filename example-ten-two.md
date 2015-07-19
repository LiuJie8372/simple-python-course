# 例 10.2 备份脚本——版本二

```

    #!/usr/bin/python
    # Filename: backup_ver2.py
    
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
    
    # Create the subdirectory if it isn't already there
    if not os.path.exists(today):
        os.mkdir(today) # make directory
        print 'Successfully created directory', today

    # The name of the zip file
    target = today + os.sep + now + '.zip'
    
    # 5. We use the zip command (in Unix/Linux) to put the files in a zip archive
    zip_command = "zip -qr '%s' %s" % (target, ' '.join(source))
    
    # Run the backup
    if os.system(zip_command) == 0:
        print 'Successful backup to', target
    else:
        print 'Backup FAILED'

```

（源文件：[code/backup_ver2.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/backup_ver2.py)）

**输出**

```

    $ python backup_ver2.py
    Successfully created directory /mnt/e/backup/20041208
    Successful backup to /mnt/e/backup/20041208/080020.zip
    
    $ python backup_ver2.py
    Successful backup to /mnt/e/backup/20041208/080428.zip

```

**它如何工作**

两个程序的大部分是相同的。改变的部分主要是使用 os.exists 函数检验在主备份目录中是否有以当前日期作为名称的目录。如果没有，我们使用 os.mkdir 函数创建。

注意 os.sep 变量的用法——这会根据你的操作系统给出目录分隔符，即在 Linux、Unix 下它是'/'，在 Windows 下它是'\\'，而在 Mac OS 下它是':'。使用 os.sep 而非直接使用字符，会使我们的程序具有移植性，可以在上述这些系统下工作。