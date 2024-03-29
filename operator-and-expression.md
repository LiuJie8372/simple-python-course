# 运算符与表达式

## 简介

你编写的大多数语句（逻辑行）都包含**表达式**。一个简单的表达式例子如 2 + 3。一个表达式可以分解为运算符和操作数。

运算符 的功能是完成某件事，它们由如+这样的符号或者其他特定的关键字表示。运算符需要数据来进行运算，这样的数据被称为 *操作数* 。在这个例子中，2 和 3 是操作数。

## 运算符

我们将简单浏览一下运算符和它们的用法：

**技巧**

你可以交互地使用解释器来计算例子中给出的表达式。例如，为了测试表达式 2 + 3，使用交互式的带提示符的 Python 解释器：

```

    >>> 2 + 3
    5
    >>> 3 * 5
    15
    >>>

```

**表 5.1 运算符与它们的用法**  

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg .tg-s6z2{text-align:center}
</style>
<table class="tg">
  <tr>
    <th class="tg-s6z2">运算符</th>
    <th class="tg-s6z2">名称</th>
    <th class="tg-s6z2">说明</th>
    <th class="tg-s6z2">例子</th>
  </tr>
  <tr>
    <td class="tg-031e">+</td>
    <td class="tg-031e">加</td>
    <td class="tg-031e">两个对象相加</td>
    <td class="tg-031e">3 + 5得到8。'a' + 'b'得到'ab'。</td>
  </tr>
  <tr>
    <td class="tg-031e">-</td>
    <td class="tg-031e">减</td>
    <td class="tg-031e">得到负数或是一个数减去另一个数</td>
    <td class="tg-031e">-5.2得到一个负数。50 - 24得到26。</td>
  </tr>
  <tr>
    <td class="tg-031e">*</td>
    <td class="tg-031e">乘</td>
    <td class="tg-031e">两个数相乘或是返回一个被重复若干次的字符串</td>
    <td class="tg-031e">2 * 3得到6。'la' * 3得到'lalala'。</td>
  </tr>
  <tr>
    <td class="tg-031e">**</td>
    <td class="tg-031e">幂</td>
    <td class="tg-031e">返回x的y次幂</td>
    <td class="tg-031e">3 ** 4得到81（即3 * 3 * 3 * 3）</td>
  </tr>
  <tr>
    <td class="tg-031e">/</td>
    <td class="tg-031e">除</td>
    <td class="tg-031e">x除以y</td>
    <td class="tg-031e">4/3得到1（整数的除法得到整数结果）。4.0/3或4/3.0得到1.3333333333333333</td>
  </tr>
  <tr>
    <td class="tg-031e">//</td>
    <td class="tg-031e">取整除</td>
    <td class="tg-031e">返回商的整数部分</td>
    <td class="tg-031e">4 // 3.0得到1.0</td>
  </tr>
  <tr>
    <td class="tg-031e">%</td>
    <td class="tg-031e">取模</td>
    <td class="tg-031e">返回除法的余数</td>
    <td class="tg-031e">8%3得到2。-25.5%2.25得到1.5</td>
  </tr>
  <tr>
    <td class="tg-031e">&lt;&lt;</td>
    <td class="tg-031e">左移</td>
    <td class="tg-031e">把一个数的比特向左移一定数目（每个数在内存中都表示为比特或二进制数字，即0和1）</td>
    <td class="tg-031e">2 &lt;&lt; 2得到8。——2按比特表示为10</td>
  </tr>
  <tr>
    <td class="tg-031e">&gt;&gt;</td>
    <td class="tg-031e">右移</td>
    <td class="tg-031e">把一个数的比特向右移一定数目</td>
    <td class="tg-031e">11 &gt;&gt; 1得到5。——11按比特表示为1011，向右移动1比特后得到101，即十进制的5。</td>
  </tr>
  <tr>
    <td class="tg-031e">&amp;</td>
    <td class="tg-031e">按位与</td>
    <td class="tg-031e">数的按位与</td>
    <td class="tg-031e">5 &amp; 3得到1。</td>
  </tr>
  <tr>
    <td class="tg-031e">|</td>
    <td class="tg-031e">按位或</td>
    <td class="tg-031e">数的按位或</td>
    <td class="tg-031e">5 | 3得到7。</td>
  </tr>
  <tr>
    <td class="tg-031e">^</td>
    <td class="tg-031e">按位异或</td>
    <td class="tg-031e">数的按位异或</td>
    <td class="tg-031e">5 ^ 3得到6</td>
  </tr>
  <tr>
    <td class="tg-031e">~</td>
    <td class="tg-031e">按位翻转</td>
    <td class="tg-031e">x的按位翻转是-(x+1)</td>
    <td class="tg-031e">~5得到6。</td>
  </tr>
  <tr>
    <td class="tg-031e">&lt;</td>
    <td class="tg-031e">小于</td>
    <td class="tg-031e">返回x是否小于y。所有比较运算符返回1表示真，返回0表示假。这分别与特殊的变量True和False等价。注意，这些变量名的大写。</td>
    <td class="tg-031e">5 &lt; 3返回0（即False）而3 &lt; 5返回1（即True）。比较可以被任意连接：3 &lt; 5 &lt; 7返回True。</td>
  </tr>
  <tr>
    <td class="tg-031e">&gt;</td>
    <td class="tg-031e">大于</td>
    <td class="tg-031e">返回x是否大于y</td>
    <td class="tg-031e">5 &gt; 3返回True。如果两个操作数都是数字，它们首先被转换为一个共同的类型。否则，它总是返回False。</td>
  </tr>
  <tr>
    <td class="tg-031e">&lt;=</td>
    <td class="tg-031e">小于等于</td>
    <td class="tg-031e">返回x是否小于等于y</td>
    <td class="tg-031e">x = 3; y = 6; x &lt;= y返回True。</td>
  </tr>
  <tr>
    <td class="tg-031e">&gt;=</td>
    <td class="tg-031e">大于等于</td>
    <td class="tg-031e">返回x是否大于等于y</td>
    <td class="tg-031e">x = 4; y = 3; x &gt;= y返回True。</td>
  </tr>
  <tr>
    <td class="tg-031e">==</td>
    <td class="tg-031e">等于</td>
    <td class="tg-031e">比较对象是否相等</td>
    <td class="tg-031e">x = 2; y = 2; x == y返回True。x = 'str'; y = 'stR'; x == y返回False。x = 'str'; y = 'str'; x == y返回True。</td>
  </tr>
  <tr>
    <td class="tg-031e">!=</td>
    <td class="tg-031e">不等于</td>
    <td class="tg-031e">比较两个对象是否不相等</td>
    <td class="tg-031e">x = 2; y = 3; x != y返回True。</td>
  </tr>
  <tr>
    <td class="tg-031e">not</td>
    <td class="tg-031e">布尔“非”</td>
    <td class="tg-031e">如果x为True，返回False。如果x为False，它返回True。</td>
    <td class="tg-031e">x = True; not y返回False。</td>
  </tr>
  <tr>
    <td class="tg-031e">and</td>
    <td class="tg-031e">布尔“与”</td>
    <td class="tg-031e">如果x为False，x and y返回False，否则它返回y的计算值。</td>
    <td class="tg-031e">x = False; y = True; x and y，由于x是False，返回False。在这里，Python不会计算y，因为它知道这个表达式的值肯定是False（因为x是False）。这个现象称为短路计算。</td>
  </tr>
  <tr>
    <td class="tg-031e">or</td>
    <td class="tg-031e">布尔“或”</td>
    <td class="tg-031e">如果x是True，它返回True，否则它返回y的计算值。</td>
    <td class="tg-031e">x = True; y = False; x or y返回True。短路计算在这里也适用。</td>
  </tr>
</table>


## 运算符优先级

如果你有一个如 2 + 3 * 4 那样的表达式，是先做加法呢，还是先做乘法？我们的中学数学告诉我们应当先做乘法——这意味着乘法运算符的优先级高于加法运算符。

下面这个表给出 Python 的运算符优先级，从最低的优先级（最松散地结合）到最高的优先级（最紧密地结合）。这意味着在一个表达式中，Python 会首先计算表中较下面的运算符，然后在计算列在表上部的运算符。

下面这张表（与 Python 参考手册中的那个表一模一样）已经顾及了完整的需要。事实上，我建议你使用圆括号来分组运算符和操作数，以便能够明确地指出运算的先后顺序，使程序尽可能地易读。例如，2 + (3 * 4)显然比 2 + 3 * 4 清晰。与此同时，圆括号也应该正确使用，而不应该用得过滥（比如 2 + (3 + 4)）。

**表 5.2 运算符优先级**

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg .tg-hgcj{font-weight:bold;text-align:center}
</style>
<table class="tg">
  <tr>
    <th class="tg-hgcj">运算符</th>
    <th class="tg-hgcj">描述</th>
  </tr>
  <tr>
    <td class="tg-031e">lambda</td>
    <td class="tg-031e">Lambda表达式</td>
  </tr>
  <tr>
    <td class="tg-031e">or</td>
    <td class="tg-031e">布尔“或”</td>
  </tr>
  <tr>
    <td class="tg-031e">and</td>
    <td class="tg-031e">布尔“与”</td>
  </tr>
  <tr>
    <td class="tg-031e">not x</td>
    <td class="tg-031e">布尔“非”</td>
  </tr>
  <tr>
    <td class="tg-031e">in，not in</td>
    <td class="tg-031e">成员测试</td>
  </tr>
  <tr>
    <td class="tg-031e">is，is not</td>
    <td class="tg-031e">同一性测试</td>
  </tr>
  <tr>
    <td class="tg-031e">&lt;，&lt;=，&gt;，&gt;=，!=，==</td>
    <td class="tg-031e">比较</td>
  </tr>
  <tr>
    <td class="tg-031e">|</td>
    <td class="tg-031e">按位或</td>
  </tr>
  <tr>
    <td class="tg-031e">^</td>
    <td class="tg-031e">按位异或</td>
  </tr>
  <tr>
    <td class="tg-031e">&amp;</td>
    <td class="tg-031e">按位与</td>
  </tr>
  <tr>
    <td class="tg-031e">&lt;&lt;，&gt;&gt;</td>
    <td class="tg-031e">移位</td>
  </tr>
  <tr>
    <td class="tg-031e">+，-</td>
    <td class="tg-031e">加法与减法</td>
  </tr>
  <tr>
    <td class="tg-031e">*，/，%</td>
    <td class="tg-031e">乘法、除法与取余</td>
  </tr>
  <tr>
    <td class="tg-031e">+x，-x</td>
    <td class="tg-031e">正负号</td>
  </tr>
  <tr>
    <td class="tg-031e">~x</td>
    <td class="tg-031e">按位翻转</td>
  </tr>
  <tr>
    <td class="tg-031e">**</td>
    <td class="tg-031e">指数</td>
  </tr>
  <tr>
    <td class="tg-031e">x.attribute</td>
    <td class="tg-031e">属性参考</td>
  </tr>
  <tr>
    <td class="tg-031e">x[index]</td>
    <td class="tg-031e">下标</td>
  </tr>
  <tr>
    <td class="tg-031e">x[index:index]</td>
    <td class="tg-031e">寻址段</td>
  </tr>
  <tr>
    <td class="tg-031e">f(arguments...)</td>
    <td class="tg-031e">函数调用</td>
  </tr>
  <tr>
    <td class="tg-031e">(experession,...)</td>
    <td class="tg-031e">绑定或元组显示</td>
  </tr>
  <tr>
    <td class="tg-031e">[expression,...]</td>
    <td class="tg-031e">列表显示</td>
  </tr>
  <tr>
    <td class="tg-031e">{key:datum,...}</td>
    <td class="tg-031e">字典显示</td>
  </tr>
  <tr>
    <td class="tg-031e">'expression,...'</td>
    <td class="tg-031e">字符串转换</td>
  </tr>
  
  </tr>
</table>

其中我们还没有接触过的运算符将在后面的章节中介绍。

在表中列在同一行的运算符具有 *相同优先级* 。例如，+和-有相同的优先级。
     
### 计算顺序

默认地，运算符优先级表决定了哪个运算符在别的运算符之前计算。然而，如果你想要改变它们的计算顺序，你得使用圆括号。例如，你想要在一个表达式中让加法在乘法之前计算，那么你就得写成类似(2 + 3) * 4的样子。
     
### 结合规律

运算符通常由左向右结合，即具有相同优先级的运算符按照从左向右的顺序计算。例如，2 + 3 + 4 被计算成(2 + 3) + 4。一些如赋值运算符那样的运算符是由右向左结合的，即 a = b = c 被处理为 a = (b = c)。

## 表达式
     
### 使用表达式

**例 5.1 使用表达式**

```

    #!/usr/bin/python
    # Filename: expression.py
    
    length = 5
    breadth = 2
    area = length * breadth
    print 'Area is', area
    print 'Perimeter is', 2 * (length + breadth)

```

（源文件：[code/expression.py](http://woodpecker.org.cn/abyteofpython_cn/chinese/code/expression.py)）

**输出**

```

    $ python expression.py
    Area is 10
    Perimeter is 14

```

**它如何工作**

矩形的长度与宽度存储在以它们命名的变量中。我们借助表达式使用它们计算矩形的面积和边长。我们表达式 length * breadth 的结果存储在变量 area 中，然后用 print 语句打印。在另一个打印语句中，我们直接使用表达式 2 * (length + breadth)的值。

另外，注意 Python 如何打印“漂亮的”输出。尽管我们没有在'Area is'和变量 area 之间指定空格，Python 自动在那里放了一个空格，这样我们就可以得到一个清晰漂亮的输出，而程序也变得更加易读（因为我们不需要担心输出之间的空格问题）。这是 Python 如何使程序员的生活变得更加轻松的一个例子。

## 概括

我们已经学习了如何使用运算符、操作数和表达式——这些使任何程序的基本组成部分。接下来，我们将学习如何通过语句在我们的程序中使用这些部分。