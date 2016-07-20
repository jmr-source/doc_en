
<a href="tag-f.html">查看文档请点此</a>

### <div align="center">f - 格式化</div> ###

&lt;f&gt;
<pre>
用于格式化输出。
</pre>

#### 说明 ####

<pre>
把标签内的文本按指定格式输出。
</pre>

#### 属性 ####

<pre><b>partten（必须）：指定的格式字符串,可使用占位符。</b>
参考String.format(String fmt, Object... args)。
</pre>

<pre>
<b>values（可选）：指定参数，可填写多个参数，每个参数用","隔开。</b>
如果没有指定values，将把标签文本中的内容作为唯一参数。
</pre>

<pre>
<b>valueScope(可选)：参数的作用域</b>
context:参数来自context中(默认)
session:参数来自session中
</pre>

#### 其它 ####

<pre>
这个标签有2种格式
1.&lt;f parrten="" values=""/&gt;

ex:
&lt;f var="s" set value="'Hello Jmr!'"/&gt;
&lt;f partten="Demo: %s" values="s"/&gt;
-->Demo: Hello Jmr!

2.&lt;f parrten=""&gt;&lt;/f&gt;

ex:
&lt;f var="s" set value="'Hello Jmr!'"/&gt;
&lt;f partten="Demo: %s"&gt;&lt;get value="s"/&gt;&lt;/f&gt;
-->Demo: Hello Jmr!
</pre>





