<a href="head-tag-java.html">查看详情请点此</a>

### <div align="center">java:package - 得到包名</div> ###

&lt;java:package&gt;
<pre>
得到java类的包名。
</pre>

#### 属性 ####

<pre>
<b>packageNameVar（可选）：设置一个参数存放得到的包名，默认存放到context中</b>。
</pre>

<pre>
<b>valueScope(可选)：packageNameVar参数的作用域。</b>
context:参数设置到context中(默认)
session:参数设置到session中
</pre>

#### 说明 ####

<pre>
如果生成的路径不为java源文件夹，则输出空字符。
</pre>