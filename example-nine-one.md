# 例 9.1 使用列表

```

    #!/usr/bin/python
    # Filename: using_list.py
    
    # This is my shopping list
    shoplist = ['apple', 'mango', 'carrot', 'banana']
    
    print 'I have', len(shoplist),'items to purchase.'
    
    print 'These items are:', # Notice the comma at end of the line
    for item in shoplist:
    print item,
    
    print '\nI also have to buy rice.'
    shoplist.append('rice')
    print 'My shopping list is now', shoplist
    
    print 'I will sort my list now'
    shoplist.sort()
    print 'Sorted shopping list is', shoplist
    
    print 'The first item I will buy is', shoplist[0]
    olditem = shoplist[0]
    del shoplist[0]
    print 'I bought the', olditem
    print 'My shopping list is now', shoplist

```

（源文件：[code/using_list.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/using_list.py)）

**输出**

```

    $ python using_list.py
    I have 4 items to purchase.
    These items are: apple mango carrot banana
    I also have to buy rice.
    My shopping list is now ['apple', 'mango', 'carrot', 'banana', 'rice']
    I will sort my list now
    Sorted shopping list is ['apple', 'banana', 'carrot', 'mango', 'rice']
    The first item I will buy is apple
    I bought the apple
    My shopping list is now ['banana', 'carrot', 'mango', 'rice']

```

**它如何工作**

变量 shoplist 是某人的购物列表。在 shoplist 中，我们只存储购买的东西的名字字符串，但是记住，你可以在列表中添加 *任何种类的对象* 包括数甚至其他列表。

我们也使用了 for..in 循环在列表中各项目间递归。从现在开始，你一定已经意识到列表也是一个序列。序列的特性会在后面的[章节](http://woodpecker.org.cn/abyteofpython_cn/chinese/ch09s05.html)中讨论。

注意，我们在 print 语句的结尾使用了一个 *逗号* 来消除每个 print 语句自动打印的换行符。这样做有点难看，不过确实简单有效。

接下来，我们使用 append 方法在列表中添加了一个项目，就如前面已经讨论过的一样。然后我们通过打印列表的内容来检验这个项目是否确实被添加进列表了。打印列表只需简单地把列表传递给 print 语句，我们可以得到一个整洁的输出。

再接下来，我们使用列表的 sort 方法来对列表排序。需要理解的是，这个方法影响列表本身，而不是返回一个修改后的列表——这与字符串工作的方法不同。这就是我们所说的列表是 *可变的* 而字符串是 *不可变的* 。

最后，但我们完成了在市场购买一样东西的时候，我们想要把它从列表中删除。我们使用 del 语句来完成这个工作。这里，我们指出我们想要删除列表中的哪个项目，而 del 语句为我们从列表中删除它。我们指明我们想要删除列表中的第一个元素，因此我们使用 del shoplist[0]（记住，Python 从 0 开始计数）。

如果你想要知道列表对象定义的所有方法，可以通过 help(list)获得完整的知识。
