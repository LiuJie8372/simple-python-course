# 例 12.2 储存与取储存

```

    #!/usr/bin/python
    # Filename: pickling.py
    
    import cPickle as p
    #import pickle as p
    
    shoplistfile = 'shoplist.data'
    # the name of the file where we will store the object
    
    shoplist = ['apple', 'mango', 'carrot']
    
    # Write to the file
    f = file(shoplistfile, 'w')
    p.dump(shoplist, f) # dump the object to a file
    f.close()
    
    del shoplist # remove the shoplist
    
    # Read back from the storage
    f = file(shoplistfile)
    storedlist = p.load(f)
    print storedlist

```

（源文件：[code/pickling.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/pickling.py)）

**输出**

```

    $ python pickling.py
    ['apple', 'mango', 'carrot']

```

**它如何工作**

首先，请注意我们使用了 import..as 语法。这是一种便利方法，以便于我们可以使用更短的模块名称。在这个例子中，它还让我们能够通过简单地改变一行就切换到另一个模块（cPickle 或者 pickle）！在程序的其余部分的时候，我们简单地把这个模块称为 p。

为了在文件里储存一个对象，首先以写模式打开一个 file 对象，然后调用储存器模块的 dump 函数，把对象储存到打开的文件中。这个过程称为 *储存* 。

接下来，我们使用 pickle 模块的 load 函数的返回来取回对象。这个过程称为 *取储存* 。


