# 例 6.2 使用 while 语句

```

    #!/usr/bin/python
    # Filename: while.py
    
    number = 23
    running = True
    
    while running:
    guess = int(raw_input('Enter an integer : '))
    
    if guess == number:
    print 'Congratulations, you guessed it.' 
    running = False # this causes the while loop to stop
    elif guess < number:
    print 'No, it is a little higher than that' 
    else:
    print 'No, it is a little lower than that' 
    else:
    print 'The while loop is over.' 
    # Do anything else you want to do here
    
    print 'Done'

```

（源文件：[code/while.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/while.py)）

**输出**

```

    $ python while.py
    Enter an integer : 50
    No, it is a little lower than that.
    Enter an integer : 22
    No, it is a little higher than that.
    Enter an integer : 23
    Congratulations, you guessed it.
    The while loop is over.
    Done

```

**它如何工作**

在这个程序中，我们仍然使用了猜数游戏作为例子，但是这个例子的优势在于用户可以不断的猜数，直到他猜对为止——这样就不需要像前面那个例子那样为每次猜测重复执行一遍程序。这个例子恰当地说明了 while 语句的使用。

我们把 raw_input 和 if 语句移到了 while 循环内，并且在 while 循环开始前把 running 变量设置为 True。首先，我们检验变量 running 是否为 True，然后执行后面的  while-块 。在执行了这块程序之后，再次检验条件，在这个例子中，条件是 running 变量。如果它是真的，我们再次执行 while-块，否则，我们继续执行可选的 else-块，并接着执行下一个语句。

当 while 循环条件变为 False 的时候，else 块才被执行——这甚至也可能是在条件第一次被检验的时候。如果 while 循环有一个 else 从句，它将始终被执行，除非你的 while 循环将永远循环下去不会结束！

True 和 False 被称为布尔类型。你可以分别把它们等效地理解为值 1 和 0。在检验重要条件的时候，布尔类型十分重要，它们并不是真实的值 1。

else 块事实上是多余的，因为你可以把其中的语句放在同一块（与 while  相同）中，跟在 while 语句之后，这样可以取得相同的效果。

> **给 C/C++程序员的注释**  
记住，你可以在 while 循环中使用一个 else 从句。