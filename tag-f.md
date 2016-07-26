# <div align="center">f - 格式化</div> #


&lt;f&gt;
<pre>
用于格式化输出
</pre>

#### 说明 ####

<pre>
把标签内的文本按指定格式输出。
</pre>

#### 属性 ####

<pre>
<b>partten（必须）</b>
使用指定的格式字符串和参数来格式化字符串
参考java的方法String.format(String fmt, Object... args)
</pre>

<pre>
<b>values（可选）</b>
指定参数，可填写多个参数，每个参数用","隔开
</pre>

<pre>
<b>valueScope（可选）</b>
变量的作用域

<b>属性</b>
context:从context中得到变量（默认）
session:从session中得到变量
</pre>

#### 其它 ####

<pre>
这个标签有2种格式
1.&lt;f parrten="" values=""/&gt;

e.g.
&lt;f var="s" set value="'Hello Jmr!'"/&gt;
&lt;f partten="Demo: %s" values="s"/&gt;
-->Demo: Hello Jmr!

2.&lt;f parrten=""&gt;&lt;/f&gt;

e.g.
&lt;f var="s" set value="'Hello Jmr!'"/&gt;
&lt;f partten="Demo: %s"&gt;&lt;get value="s"/&gt;&lt;/f&gt;
-->Demo: Hello Jmr!
</pre>

----------

#### 实例演示 ####

<pre>
<b>具体用法请参考：String.format(String fmt, Object... args)</b>
String fmt     --&gt;   parrten = ""
Object... args --&gt;   values = ""
<b>占位符完整格式为： %[index$][标识]*[最小宽度][.精度]转换符</b>
</pre>

<pre>
例子1
</pre>

![](image/f_tag_template1.png)

![](image/f_tag_result1.png)

<pre>
例子2
</pre>

![](image/f_tag_template2.png)

<pre>
请在eclipse外部打开生成的文件，eclipse由于字体大小问题，显示内容可能不对齐。
</pre>

![](image/f_tag_result2.png)




