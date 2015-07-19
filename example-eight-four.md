# 例 8.4 使用 dir 函数

```

    $ python
    >>> import sys
    >>> dir(sys) # get list of attributes for sys module
    ['__displayhook__', '__doc__', '__excepthook__', '__name__', '__stderr__',
    '__stdin__', '__stdout__', '_getframe', 'api_version', 'argv',
    'builtin_module_names', 'byteorder', 'call_tracing', 'callstats',
    'copyright', 'displayhook', 'exc_clear', 'exc_info', 'exc_type',
    'excepthook', 'exec_prefix', 'executable', 'exit', 'getcheckinterval',
    'getdefaultencoding', 'getdlopenflags', 'getfilesystemencoding',
    'getrecursionlimit', 'getrefcount', 'hexversion', 'maxint', 'maxunicode',
    'meta_path','modules', 'path', 'path_hooks', 'path_importer_cache',
    'platform', 'prefix', 'ps1', 'ps2', 'setcheckinterval', 'setdlopenflags',
    'setprofile', 'setrecursionlimit', 'settrace', 'stderr', 'stdin', 'stdout',
    'version', 'version_info', 'warnoptions']
    >>> dir() # get list of attributes for current module
    ['__builtins__', '__doc__', '__name__', 'sys']
    >>>
    >>> a = 5 # create a new variable 'a'
    >>> dir()
    ['__builtins__', '__doc__', '__name__', 'a', 'sys']
    >>>
    >>> del a # delete/remove a name
    >>>
    >>> dir()
    ['__builtins__', '__doc__', '__name__', 'sys']
    >>>

```

**它如何工作**

首先，我们来看一下在输入的 sys 模块上使用 dir。我们看到它包含一个庞大的属性列表。

接下来，我们不给 dir 函数传递参数而使用它——默认地，它返回当前模块的属性列表。注意，输入的模块同样是列表的一部分。

为了观察 dir 的作用，我们定义一个新的变量 a 并且给它赋一个值，然后检验 dir，我们观察到在列表中增加了以上相同的值。我们使用del语句删除当前模块中的变量/属性，这个变化再一次反映在 dir 的输出中。

关于 del 的一点注释——这个语句在运行后被用来 *删除* 一个变量/名称。在这个例子中，del a，你将无法再使用变量 a——它就好像从来没有存在过一样。

