# 更多 Python 的内容

到目前为止，我们已经学习了绝大多数常用的 Python 知识。在这一章中，我们将要学习另外一些方面的 Python 知识，从而使我们对 Python 的了解更加 *完整* 。

## 特殊的方法

在类中有一些特殊的方法具有特殊的意义，比如 __init__ 和 __del__ 方法，它们的重要性我们已经学习过了。

一般说来，特殊的方法都被用来模仿某个行为。例如，如果你想要为你的类使用 x[key]这样的索引操作（就像列表和元组一样），那么你只需要实现 __getitem__()方法就可以了。想一下，Python 就是对 list 类这样做的！

下面这个表中列出了一些有用的特殊方法。如果你想要知道所有的特殊方法，你可以在《Python 参考手册》中找到一个庞大的列表。

**表 15.1 一些特殊的方法**

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg .tg-hgcj{font-weight:bold;text-align:center}
</style>
<table class="tg">
  <tr>
    <th class="tg-hgcj">名称</th>
    <th class="tg-hgcj">说明</th>
  </tr>
  <tr>
    <td class="tg-031e">__init__(self,...)</td>
    <td class="tg-031e">这个方法在新建对象恰好要被返回使用之前被调用。</td>
  </tr>
  <tr>
    <td class="tg-031e">__del__(self)</td>
    <td class="tg-031e">恰好在对象要被删除之前调用。</td>
  </tr>
  <tr>
    <td class="tg-031e">__str__(self)</td>
    <td class="tg-031e">在我们对对象使用 print 语句或是使用 str()的时候调用。</td>
  </tr>
  <tr>
    <td class="tg-031e">__lt__(self,other)</td>
    <td class="tg-031e">当使用 小于 运算符（&lt;）的时候调用。类似地，对于所有的运算符（+，&gt;等等）都有特殊的方法。</td>
  </tr>
  <tr>
    <td class="tg-031e">__getitem__(self,key)</td>
    <td class="tg-031e">使用x[key]索引操作符的时候调用。</td>
  </tr>
  <tr>
    <td class="tg-031e">__len__(self)</td>
    <td class="tg-031e">对序列对象使用内建的len()函数的时候调用。</td>
  </tr>
</table>


## 单语句块

现在，你已经很深刻地理解了每一个语句块是通过它的缩进层次与其它块区分开来的。然而这在大多数情况下是正确的，但是并非 100％的准确。如果你的语句块只包含一句语句，那么你可以在条件语句或循环语句的同一行指明它。下面这个例子清晰地说明了这一点：

```

    >>> flag = True
    >>> if flag: print 'Yes'
    ...
    Yes

```

就如你所看见的，单个语句被直接使用而不是作为一个独立的块使用。虽然这样做可以使你的程序变得 小一些 ，但是除了检验错误之外我**强烈**建议你不要使用这种缩略方法。不使用它的一个主要的理由是一旦你使用了恰当的缩进，你就可以很方便地添加一个额外的语句。

另外，注意在使用交互模式的 Python 解释器的时候，它会通过恰当地改变提示符来帮助你输入语句。在上面这个例子中，当你输入了关键字 if 之后，Python 解释器把提示符改变为...以表示语句还没有结束。在这种情况下，我们按**回车键**用来确认语句已经完整了。然后，Python 完成整个语句的执行，并且返回原来的提示符并且等待下一句输入。

## 列表综合

通过列表综合，可以从一个已有的列表导出一个新的列表。例如，你有一个数的列表，而你想要得到一个对应的列表，使其中所有大于 2 的数都是原来的2倍。对于这种应用，列表综合是最理想的方法。
     
### 使用列表综合

**例 15.1 使用列表综合**

```

    #!/usr/bin/python
    # Filename: list_comprehension.py
    
    listone = [2, 3, 4]
    listtwo = [2*i for i in listone if i > 2]
    print listtwo

```

[（源文件：code/list_comprehension.py）](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/list_comprehension.py)

**输出**

```

    $ python list_comprehension.py
    [6, 8]

```

**它如何工作**

这里我们为满足条件（if i > 2）的数指定了一个操作（2*i），从而导出一个新的列表。注意原来的列表并没有发生变化。在很多时候，我们都是使用循环来处理列表中的每一个元素，而使用列表综合可以用一种更加精确、简洁、清楚的方法完成相同的工作。

## 在函数中接收元组和列表

当要使函数接收元组或字典形式的参数的时候，有一种特殊的方法，它分别使用*和**前缀。这种方法在函数需要获取可变数量的参数的时候特别有用。

```

    >>> def powersum(power, *args):
    ... '''Return the sum of each argument raised to specified power.'''
    ... total = 0
    ... for i in args:
    ...  total += pow(i, power)
    ... return total
    ...
    >>> powersum(2, 3, 4)
    25
    
    >>> powersum(2, 10)
    100

```

由于在 args 变量前有*前缀，所有多余的函数参数都会作为一个元组存储在 args 中。如果使用的是**前缀，多余的参数则会被认为是一个字典的键/值对。

## lambda 形式

lambda 语句被用来创建新的函数对象，并且在运行时返回它们。
     
### 使用 lambda 形式

**例 15.2 使用 lambda 形式**

```

    #!/usr/bin/python
    # Filename: lambda.py
    
    def make_repeater(n):
        return lambda s: s*n
    
    twice = make_repeater(2)
    
    print twice('word')
    print twice(5)

```

（源文件：[code/lambda.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/lambda.py)）

**输出**

```

    $ python lambda.py
    wordword
    10

```

**它如何工作**

这里，我们使用了 make_repeater 函数在运行时创建新的函数对象，并且返回它。lambda 语句用来创建函数对象。本质上，lambda 需要一个参数，后面仅跟单个表达式作为函数体，而表达式的值被这个新建的函数返回。注意，即便是 print 语句也不能用在 lambda 形式中，只能使用表达式。



## exec 和 eval 语句

exec 语句用来执行储存在字符串或文件中的 Python 语句。例如，我们可以在运行时生成一个包含 Python 代码的字符串，然后使用 exec 语句执行这些语句。下面是一个简单的例子。

```

    >>> exec 'print "Hello World"'
    Hello World

```

eval语句用来计算存储在字符串中的有效 Python 表达式。下面是一个简单的例子。

```

    >>> eval('2*3')
    6

```

## assert 语句

assert 语句用来声明某个条件是真的。例如，如果你非常确信某个你使用的列表中至少有一个元素，而你想要检验这一点，并且在它非真的时候引发一个错误，那么 assert 语句是应用在这种情形下的理想语句。当 assert 语句失败的时候，会引发一个 AssertionError。

```

    >>> mylist = ['item']
    >>> assert len(mylist) >= 1
    >>> mylist.pop()
    'item'
    >>> assert len(mylist) >= 1
    Traceback (most recent call last):
      File "<stdin>", line 1, in ?
    AssertionError

```


## repr 函数

repr 函数用来取得对象的规范字符串表示。反引号（也称转换符）可以完成相同的功能。注意，在大多数时候有 eval(repr(object)) == object。

```
    
    >>> i = []
    >>> i.append('item')
    >>> `i`
    "['item']"
    >>> repr(i)
    "['item']"

```

基本上，repr 函数和反引号用来获取对象的可打印的表示形式。你可以通过定义类的 __repr__ 方法来控制你的对象在被 repr 函数调用的时候返回的内容。

## 概括

在这一章中，我们又学习了一些 Python 的特色，然而你可以肯定我们并没有学习完 Python 的所有特色。不过，到目前为止，我们确实已经学习了绝大多数你在实际中会使用的内容。这些已经足以让你去创建任何程序了。

接下来，我们会讨论一下如何进一步深入探索 Python。

