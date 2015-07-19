# 例 9.6 对象与参考

```

    #!/usr/bin/python
    # Filename: reference.py
    
    print 'Simple Assignment'
    shoplist = ['apple', 'mango', 'carrot', 'banana']
    mylist = shoplist # mylist is just another name pointing to the same object!
    
    del shoplist[0]
    
    print 'shoplist is', shoplist
    print 'mylist is', mylist
    # notice that both shoplist and mylist both print the same list without
    # the 'apple' confirming that they point to the same object
    
    print 'Copy by making a full slice'
    mylist = shoplist[:] # make a copy by doing a full slice
    del mylist[0] # remove first item
    
    print 'shoplist is', shoplist
    print 'mylist is', mylist
    # notice that now the two lists are different

```

（源文件：[code/reference.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/reference.py)）

**输出**

```

    $ python reference.py
    Simple Assignment
    shoplist is ['mango', 'carrot', 'banana']
    mylist is ['mango', 'carrot', 'banana']
    Copy by making a full slice
    shoplist is ['mango', 'carrot', 'banana']
    mylist is ['carrot', 'banana']

```

**它如何工作**

大多数解释已经在程序的注释中了。你需要记住的只是如果你想要复制一个列表或者类似的序列或者其他复杂的对象（不是如整数那样的简单 *对象* ），那么你必须使用切片操作符来取得拷贝。如果你只是想要使用另一个变量名，两个名称都 参考 同一个对象，那么如果你不小心的话，可能会引来各种麻烦。

> **给 Perl 程序员的注释**  
记住列表的赋值语句**不**创建拷贝。你得使用切片操作符来建立序列的拷贝。