<a href="head-tag-java.html">查看详情请点此</a>

### <div align="center">java:class - 得到类名</div> ###


&lt;java:package&gt;
<pre>
得到java类或者接口的名称，来源是生成文件的名称
</pre>

#### 属性 ####

<pre>
<b>classNameVar（可选）</b>
设置一个参数存放类名或者接口名（不包含前置的包名），默认存放到context中
</pre>

<pre>
<b>fullyClassNameVar（可选）</b>
设置一个参数存放完整的类名或者接口名(包含前置的包名)，默认存放到context中
</pre>

<pre>
<b>setScope（可选）</b>
设置classNameVar和fullyClassNameVar的作用域

<b>属性</b>
context:设置参数到context中（默认）
session:设置参数到session中
</pre>

#### 其它 ####

<pre>
根据java规则，生成java文件的文件名，和类名或者接口名必须一致。
</pre>