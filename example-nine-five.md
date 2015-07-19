# 例 9.5 使用序列

```

    #!/usr/bin/python
    # Filename: seq.py
    
    shoplist = ['apple', 'mango', 'carrot', 'banana']
    
    # Indexing or 'Subscription' operation
    print 'Item 0 is', shoplist[0]
    print 'Item 1 is', shoplist[1]
    print 'Item 2 is', shoplist[2]
    print 'Item 3 is', shoplist[3]
    print 'Item -1 is', shoplist[-1]
    print 'Item -2 is', shoplist[-2]
    
    # Slicing on a list
    print 'Item 1 to 3 is', shoplist[1:3]
    print 'Item 2 to end is', shoplist[2:]
    print 'Item 1 to -1 is', shoplist[1:-1]
    print 'Item start to end is', shoplist[:]
    
    # Slicing on a string
    name = 'swaroop'
    print 'characters 1 to 3 is', name[1:3]
    print 'characters 2 to end is', name[2:]
    print 'characters 1 to -1 is', name[1:-1]
    print 'characters start to end is', name[:]

```

（源文件：[code/seq.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/seq.py)）

**输出**

```

    $ python seq.py
    Item 0 is apple
    Item 1 is mango
    Item 2 is carrot
    Item 3 is banana
    Item -1 is banana
    Item -2 is carrot
    Item 1 to 3 is ['mango', 'carrot']
    Item 2 to end is ['carrot', 'banana']
    Item 1 to -1 is ['mango', 'carrot']
    Item start to end is ['apple', 'mango', 'carrot', 'banana']
    characters 1 to 3 is wa
    characters 2 to end is aroop
    characters 1 to -1 is waroo
    characters start to end is swaroop

```

**它如何工作**

首先，我们来学习如何使用索引来取得序列中的单个项目。这也被称作是下标操作。每当你用方括号中的一个数来指定一个序列的时候，Python 会为你抓取序列中对应位置的项目。记住，Python 从 0 开始计数。因此，shoplist[0]抓取第一个项目，shoplist[3]抓取 shoplist 序列中的第四个元素。

索引同样可以是负数，在那样的情况下，位置是从序列尾开始计算的。因此，shoplist[-1]表示序列的最后一个元素而 shoplist[-2]抓取序列的倒数第二个项目。

切片操作符是序列名后跟一个方括号，方括号中有一对可选的数字，并用冒号分割。注意这与你使用的索引操作符十分相似。记住数是可选的，而冒号是必须的。

切片操作符中的第一个数（冒号之前）表示切片开始的位置，第二个数（冒号之后）表示切片到哪里结束。如果不指定第一个数，Python 就从序列首开始。如果没有指定第二个数，则 Python 会停止在序列尾。注意，返回的序列从开始位置 开始 ，刚好在 *结束* 位置之前结束。即开始位置是包含在序列切片中的，而结束位置被排斥在切片外。

这样，shoplist[1:3]返回从位置 1 开始，包括位置 2，但是停止在位置 3 的一个序列切片，因此返回一个含有两个项目的切片。类似地，shoplist[:]返回整个序列的拷贝。

你可以用负数做切片。负数用在从序列尾开始计算的位置。例如，shoplist[:-1]会返回除了最后一个项目外包含所有项目的序列切片。

使用 Python 解释器交互地尝试不同切片指定组合，即在提示符下你能够马上看到结果。序列的神奇之处在于你可以用相同的方法访问元组、列表和字符串
