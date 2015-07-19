# 例 11.4 使用类与对象的变量

```

    #!/usr/bin/python
    # Filename: objvar.py
    
    class Person:
         '''Represents a person.'''
        population = 0

        def __init__(self, name):
            '''Initializes the person's data.'''
            self.name = name
            print '(Initializing %s)' % self.name

            # When this person is created, he/she
            # adds to the population
            Person.population += 1

        def __del__(self):
            '''I am dying.'''
             print '%s says bye.' % self.name

            Person.population -= 1

            if Person.population == 0:
                print 'I am the last one.'
            else:
                print 'There are still %d people left.' % Person.population

        def sayHi(self):
            '''Greeting by the person.

            Really, that's all it does.'''
            print 'Hi, my name is %s.' % self.name

        def howMany(self):
            '''Prints the current population.'''
             if Person.population == 1:
                 print 'I am the only person here.'
            else:
                print 'We have %d persons here.' % Person.population

    swaroop = Person('Swaroop')
    swaroop.sayHi()
    swaroop.howMany()
    
    kalam = Person('Abdul Kalam')
    kalam.sayHi()
    kalam.howMany()
    
    swaroop.sayHi()
    swaroop.howMany()

```


（源文件：[code/objvar.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/objvar.py)）

**输出**

```

    $ python objvar.py
    (Initializing Swaroop)
    Hi, my name is Swaroop.
    I am the only person here.
    (Initializing Abdul Kalam)
    Hi, my name is Abdul Kalam.
    We have 2 persons here.
    Hi, my name is Swaroop.
    We have 2 persons here.
    Abdul Kalam says bye.
    There are still 1 people left.
    Swaroop says bye.
    I am the last one.

```

**它如何工作**

这是一个很长的例子，但是它有助于说明类与对象的变量的本质。这里，population 属于 Person 类，因此是一个类的变量。name 变量属于对象（它使用 self 赋值）因此是对象的变量。

观察可以发现 __init__ 方法用一个名字来初始化 Person 实例。在这个方法中，我们让 population 增加 1，这是因为我们增加了一个人。同样可以发现，self.name 的值根据每个对象指定，这表明了它作为对象的变量的本质。

记住，你只能使用 self 变量来参考同一个对象的变量和方法。这被称为 *属性参考* 。

在这个程序中，我们还看到 docstring 对于类和方法同样有用。我们可以在运行时使用 Person.__doc__ 和 Person.sayHi.__doc__ 来分别访问类与方法的文档字符串。
 
就如同 __init__ 方法一样，还有一个特殊的方法__del__，它在对象消逝的时候被调用。对象消逝即对象不再被使用，它所占用的内存将返回给系统作它用。在这个方法里面，我们只是简单地把 Person.population 减 1。

当对象不再被使用时， __del__ 方法运行，但是很难保证这个方法究竟在 *什么时候* 运行。如果你想要指明它的运行，你就得使用 del 语句，就如同我们在以前的例子中使用的那样。

> **给 C++/Java/C#程序员的注释**  
Python 中所有的类成员（包括数据成员）都是 *公共的* ，所有的方法都是 *有效的* 。
只有一个例外：如果你使用的数据成员名称以 双下划线前缀 比如  __privatevar，Python 的名称管理体系会有效地把它作为私有变量。
这样就有一个惯例，如果某个变量只想在类或对象中使用，就应该以单下划线前缀。而其他的名称都将作为公共的，可以被其他类/对象使用。记住这只是一个惯例，并不是 Python 所要求的（与双下划线前缀不同）。
同样，注意 __del__ 方法与 *destructor* 的概念类似。