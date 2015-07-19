# 表 15.1 一些特殊的方法

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
    <td class="tg-031e">在我们对对象使用print语句或是使用str()的时候调用。</td>
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