# <div align="center">elseif - 判断</div> #

&lt;elseif&gt;
<pre>
判断语句块
</pre>

#### 说明 ####

<pre>
在&lt;if&gt;或者&lt;elseif&gt;后使用，当前面的判断不成立时，进入当前判断。
</pre>

#### 属性 ####

<pre>
<b>test（必须）</b>
前面的if或者elseif判断不成立，则进入判断。
使用Ognl判断条件，判断结果是true，则运行elseif块内的代码，false则不运行

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