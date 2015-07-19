# 例 7.7 使用字面意义上的语句

```

    #!/usr/bin/python
    # Filename: func_return.py
    
    def maximum(x, y):
    if x > y:
        return x
    else:
        return y
    
    print maximum(2, 3)

```

（源文件：[code/func_return.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/func_return.py)）

**输出**

```

    $ python func_return.py
    3

```

**它如何工作**

maximum 函数返回参数中的最大值，在这里是提供给函数的数。它使用简单的 if..else 语句来找出较大的值，然后 *返回* 那个值。

注意，没有返回值的 return 语句等价于 return None。None 是 Python 中表示没有任何东西的特殊类型。例如，如果一个变量的值为 None，可以表示它没有值。

除非你提供你自己的 return 语句，每个函数都在结尾暗含有 return None 语句。通过运行 print someFunction()，你可以明白这一点，函数 someFunction 没有使用 return语句，如同：

```

    def someFunction():
        pass

```

pass 语句在 Python 中表示一个空的语句块。
