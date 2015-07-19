# 例 9.4 使用字典

```

    #!/usr/bin/python
    # Filename: using_dict.py
    
    # 'ab' is short for 'a'ddress'b'ook
    
    ab = {   'Swaroop'   : 'swaroopch@byteofpython.info',
     'Larry' : 'larry@wall.org',
     'Matsumoto' : 'matz@ruby-lang.org',
     'Spammer'   : 'spammer@hotmail.com'
     }
    
    print "Swaroop's address is %s" % ab['Swaroop']
    
    # Adding a key/value pair
    ab['Guido'] = 'guido@python.org'
    
    # Deleting a key/value pair
    del ab['Spammer']
    
    print '\nThere are %d contacts in the address-book\n' % len(ab)
    for name, address in ab.items():
    print 'Contact %s at %s' % (name, address)
    
    if 'Guido' in ab: # OR ab.has_key('Guido')
    print "\nGuido's address is %s" % ab['Guido']

```

（源文件：[code/using_dict.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/using_dict.py)）

**输出**

```

    $ python using_dict.py
    Swaroop's address is swaroopch@byteofpython.info
    
    There are 4 contacts in the address-book
    
    Contact Swaroop at swaroopch@byteofpython.info
    Contact Matsumoto at matz@ruby-lang.org
    Contact Larry at larry@wall.org
    Contact Guido at guido@python.org
    
    Guido's address is guido@python.org
    

```

**它如何工作**

我们使用已经介绍过的标记创建了字典 ab。然后我们使用在列表和元组章节中已经讨论过的索引操作符来指定键，从而使用键/值对。我们可以看到字典的语法同样十分简单。

我们可以使用索引操作符来寻址一个键并为它赋值，这样就增加了一个新的键/值对，就像在上面的例子中我们对 Guido 所做的一样。

我们可以使用我们的老朋友——del 语句来删除键/值对。我们只需要指明字典和用索引操作符指明要删除的键，然后把它们传递给 del 语句就可以了。执行这个操作的时候，我们无需知道那个键所对应的值。

接下来，我们使用字典的 items 方法，来使用字典中的每个键/值对。这会返回一个元组的列表，其中每个元组都包含一对项目——键与对应的值。我们抓取这个对，然后分别赋给 for..in 循环中的变量 name 和 address 然后在 for －块中打印这些值。

我们可以使用 in 操作符来检验一个键/值对是否存在，或者使用 dict 类的 has_key 方法。你可以使用 help(dict)来查看 dict 类的完整方法列表。

**关键字参数与字典。**如果换一个角度看待你在函数中使用的关键字参数的话，你已经使用了字典了！只需想一下——你在函数定义的参数列表中使用的键/值对。当你在函数中使用变量的时候，它只不过是使用一个字典的键（这在编译器设计的术语中被称作 *符号表* ）。