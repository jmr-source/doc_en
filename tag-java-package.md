<a href="head-tag-java.html">查看详情请点此</a>

### <div align="center">java:package - 得到包名</div> ###

&lt;java:package&gt;
<pre>
得到java类的包名
</pre>

#### 属性 ####

<pre>
<b>packageNameVar（可选）</b>
设置一个变量存放得到的包名，默认存放到context中
</pre>

<pre>
<b>setScope（可选）</b>
设置packageNameVar的作用域

<b>属性</b>
context:设置参数到context中（默认）
session:设置参数到session中
</pre>

#### 其它 ####

<pre>
如果生成的路径不为java源文件夹，则输出为空字符串。
</pre>