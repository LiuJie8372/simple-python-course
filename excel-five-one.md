# 表 5.1 运算符与它们的用法



<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg .tg-hgcj{font-weight:bold;text-align:center}
</style>
<table class="tg">
  <tr>
    <th class="tg-hgcj">运算符</th>
    <th class="tg-hgcj">名称</th>
    <th class="tg-hgcj">说明</th>
    <th class="tg-hgcj">例子</th>
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