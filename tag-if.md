# <div align="center">if - 判断</div> #

&lt;if&gt;
<pre>
判断语句块
</pre>

#### 说明 ####

<pre>
通过Ognl表达式，判断语句快是否执行，可以配合&lt;elseif&gt;和&lt;else&gt;标签使用。
</pre>

#### 属性 ####

<pre>
<b>test（必须）</b>
使用Ognl判断条件，判断结果是true，则运行if块内的代码，false则不运行

<b>符号</b>
==:等于
!=:不等于
&&:与
||:或
</pre>

<pre>
<b>trim（可选）</b>
是否保留输出值的前后空白字符

<b>属性</b>
false:保留输出值的前后空白字符（默认）
true:删除输出值的前后空格（包括换行符）
</pre>

