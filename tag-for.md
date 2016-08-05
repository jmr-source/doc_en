# <div align="center">for - 循环</div> #

&lt;for&gt;
<pre>
循环
</pre>

#### 说明 ####

<pre>
得到集合变量，遍历集合。
从作用域context或者session中得到集合变量，
可使用Ognl表达式得到变量的集合，或者自定义ognl类型集合变量
</pre>

#### 属性 ####

<pre>
<b>value（必须）</b>
得到循环的集合，也可以得到变量相关的Ognl集合
</pre>

<pre>
<b>var（必须）</b>
存储集合的遍历对象
</pre>

<pre>
<b>status（可选）</b>
设置变量，存储循环信息</b>

符号    描述
<b>count</b>   循环总次数
<b>index</b>   当前循环索引
<b>isFirst</b> 当前循环是否为头索引
<b>isLast</b>  当前循环是否为尾索引
</pre>

<pre>
<b>trim（可选）</b>
是否保留输出值的前后空白字符</b>

<b>属性</b>
false:保留输出值的前后空白字符（默认）
true:删除输出值的前后空格（包括换行符）
</pre>

<pre>
<b>delimiter（可选）</b>
循环输出之间的分隔符
</pre>

<pre>
<b>test（可选）</b>
使用Ognl判断条件，判断结果是true，则运行当前循环，false则不运行

<b>符号</b>
==:等于
!=:不等于
&&:与
||:或
</pre>

<pre>
<b>duplicate（可选）</b>
是否输出重复内容

<b>属性</b>
true:已经有的重复内容仍然输出（默认）
false:已经有的重复内容不再输出
</pre>