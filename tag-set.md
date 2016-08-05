# <div align="center">set - 设置新变量</div> #

&lt;set&gt;
<pre>
设置新变量
</pre>

#### 说明 ####

<pre>
设置新变量，从作用域context或者session中得到变量，
可使用Ognl表达式得到变量的属性和方法，或者自定义ognl类型变量。
</pre>

#### 属性 ####

<pre>
<b>var（必须）</b>
设置新的变量
</pre>

<pre>
<b>setScope（可选）</b>
设置变量的作用域

<b>属性</b>
context:设置变量到context中（默认）
session:设置变量到session中
</pre>

<pre>
<b>value（必须）</b>
得到变量值，也可以得到变量相关的Ognl值

<b>可选值</b>
"str":字符串格式
{"e1","e2","e3"}:List格式
#{"key1":"value1","key2":"value2"}:Map格式
</pre>

<pre>
<b>valueScope（可选）</b>
变量的作用域

<b>属性</b>
context:从context中得到变量（默认）
session:从session中得到变量
</pre>