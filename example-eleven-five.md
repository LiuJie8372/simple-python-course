# 例 11.5 使用继承

```

    #!/usr/bin/python
    # Filename: inherit.py

    class SchoolMember:
        '''Represents any school member.'''
        def __init__(self, name, age):
            self.name = name
            self.age = age
            print '(Initialized SchoolMember: %s)' % self.name

        def tell(self):
            '''Tell my details.'''
            print 'Name:"%s" Age:"%s"' % (self.name, self.age),

    class Teacher(SchoolMember):
        '''Represents a teacher.'''
        def __init__(self, name, age, salary):
            SchoolMember.__init__(self, name, age)
            self.salary = salary
            print '(Initialized Teacher: %s)' % self.name

        def tell(self):
            SchoolMember.tell(self)
            print 'Salary: "%d"' % self.salary

    class Student(SchoolMember):
        '''Represents a student.'''
        def __init__(self, name, age, marks):
            SchoolMember.__init__(self, name, age)
            self.marks = marks
            print '(Initialized Student: %s)' % self.name

        def tell(self):
            SchoolMember.tell(self)
            print 'Marks: "%d"' % self.marks

    t = Teacher('Mrs. Shrividya', 40, 30000)
    s = Student('Swaroop', 22, 75)
    
    print # prints a blank line
    
    members = [t, s]
    for member in members:
        member.tell() # works for both Teachers and Students

```

（源文件：[code/inherit.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/inherit.py)）

**输出**

```

    $ python inherit.py
    (Initialized SchoolMember: Mrs. Shrividya)
    (Initialized Teacher: Mrs. Shrividya)
    (Initialized SchoolMember: Swaroop)
    (Initialized Student: Swaroop)
    
    Name:"Mrs. Shrividya" Age:"40" Salary: "30000"
    Name:"Swaroop" Age:"22" Marks: "75"

```

**它如何工作**

为了使用继承，我们把基本类的名称作为一个元组跟在定义类时的类名称之后。然后，我们注意到基本类的 __init__ 方法专门使用 self 变量调用，这样我们就可以初始化对象的基本类部分。这一点十分重要——Python 不会自动调用基本类的 constructor，你得亲自专门调用它。

我们还观察到我们在方法调用之前加上类名称前缀，然后把 self 变量及其他参数传递给它。

注意，在我们使用 SchoolMember 类的 tell 方法的时候，我们把 Teacher 和 Student 的实例仅仅作为 SchoolMember 的实例。

另外，在这个例子中，我们调用了子类型的 tell 方法，而不是 SchoolMember 类的 tell 方法。可以这样来理解，Python 总是首先查找对应类型的方法，在这个例子中就是如此。如果它不能在导出类中找到对应的方法，它才开始到基本类中逐个查找。基本类是在类定义的时候，在元组之中指明的。

一个术语的注释——如果在继承元组中列了一个以上的类，那么它就被称作 *多重继承* 。