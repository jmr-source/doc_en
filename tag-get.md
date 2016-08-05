# <div align="center">get - 得到变量值</div> #

&lt;get&gt;
<pre>
得到变量值
</pre>

#### 说明 ####

<pre>
从作用域context或者session中得到变量，
可使用Ognl表达式得到变量的属性和方法，或者自定义ognl类型变量
</pre>

#### 属性 ####

<pre>
<b>value（必须）</b>
得到变量值，也可以得到变量相关的Ognl值
</pre>

<pre>
<b>valueScope（可选）</b>
变量的作用域

<b>属性</b>
context:从context中得到变量（默认）
session:从session中得到变量
</pre>

<pre>
<b>case（可选）</b>
字符串大小写转换，可以使用“|”包含多个操作，如 lower|plural

<b>属性</b>
lr:字符串转成小写（同lower）
ur:字符串转成大写 （同upper）
hlr:头字母转成小写 （同headLower）
hur:头字母转成大写（同headUpper）
lower:字符串转成小写
upper:字符串转成大写
headLower:头字母转成小写
headUpper:头字母转成大写
plural:复数格式
singular:单数格式
</pre>

<pre>
<b>trim（可选）</b>
是否保留输出值的前后空白字符

<b>属性</b>
false:保留输出值的前后空白字符（默认）
true:删除输出值的前后空格（包括换行符）
</pre>

#### 用法详解 ####

##### &lt;get&gt;输出规则 #####

以下的方式都可以输出"Hello Jmr!"，  
四种方式本质上都是转换成out.write(Object object)

![](image/new_jet_compare.png)

输出的值：
<pre>
基本类型：输出的值是它们本身；
字符串：输出的是字符串；
Object：输出toString()方法的返回值。
</pre>

![](image/tag_get_out1.png)

<pre>
用&lt;get&gt;得到它们的值
</pre>

![](image/tag_get_out2.png)

<pre>
输出结果可以看到，List和array调用了toString()方法，
array因为没重写toString()方法，所以返回的是一个地址。
</pre>

![](image/tag_get_out3.png)

<pre>
小贴士：在&lt;get&gt;的value的中，把鼠标放在上面，或者选中，可以提示出这个变量的值。
</pre>

![](image/tag_get_out4.png)

##### &lt;get&gt;获取值的来源和作用域 #####

从context和session中获取变量，那么如何设置变量存放到context和session中呢？

1.在context中设置变量，作用域为当前任务，变量只能在当前任务下的模板和action中共享。
<pre>
此处在模板的&lt;% %&gt;中设置context的值，当然，也可以在action中设置context,
这里设置了String、boolean、int和List类型的变量。
</pre>

![](image/tag_get_from1.png)

<pre>
用&lt;get&gt;得到它们的值
</pre>

![](image/tag_get_from2.png)

<pre>
输出结果
</pre>

![](image/tag_get_from3.png)

<pre>
小贴士：在&lt;get&gt;的value中按提示键可以提示出可用的变量值。
</pre>

![](image/tag_get_from10.png)

2.在session中设置变量，作用域跨任务，变量能在多个任务的模板和action中共享。
<pre>
此处在模板的&lt;% %&gt;中设置context的值，当然，也可以在action中设置session,
这里设置了String、boolean、int和Map类型的变量。
</pre>

![](image/tag_get_from4.png)

<pre>
用&lt;get&gt;得到它们的值，作用域valueScope输入session
</pre>

![](image/tag_get_from5.png)

<pre>
输出结果
</pre>

![](image/tag_get_from6.png)

<pre>
小贴士：在&lt;get&gt;的value中按提示键可以提示出可用的变量值，
此处会根据作用域提示对应的变量。
</pre>

![](image/tag_get_from11.png)

3.在action中设置变量
<pre>
在action中可以设置context或者session变量，此处我们设置context变量为例。
这里设置了String、boolean、int和double[]类型的变量。
</pre>

![](image/tag_get_from7.png)

<pre>
用&lt;get&gt;得到它们的值
</pre>

![](image/tag_get_from8.png)

<pre>
输出结果
</pre>

![](image/tag_get_from9.png)

<pre>
小贴士：在&lt;get&gt;的value中按提示键可以提示出可用的变量值，
此处提示需要在模板的菜单中选中需要的action。
</pre>

![](image/tag_get_from12.png)

![](image/tag_get_from13.png)

4.在&lt;set&gt;、&lt;for&gt;等标签的var变量。
<pre>
在set、for中设置的变量本质上也是设置在context或者session中。
</pre>

![](image/tag_get_from14.png)

<pre>
用&lt;get&gt;得到它们的值，其中list用for标签循环输出，分隔符用","
</pre>

![](image/tag_get_from15.png)

<pre>
输出结果
</pre>

![](image/tag_get_from16.png)

##### &lt;get&gt;的ognl使用方法 #####

get不仅可以获得变量值，还可以得到变量的Ognl属性和方法的值

<pre>
以下是一个Student类，它有id和name这2个属性
</pre>

![](image/tag_get_ognl1.png)

<pre>
在action中new一个Student对象
</pre>

![](image/tag_get_ognl2.png)

<pre>
把模板中的action指向GetTagAction
</pre>

![](image/tag_get_from12.png)

可以得到对象的ognl values 和ognl methods
<pre>
Ognl values:对象的属性如果有对应的getXXX()方法， 就可以得到它本身
student有id和name，因为id和name有对应的getId和getName方法，所以可以得到它们的Ognl值。

Ognl methods:对象的方法
对象包含的方法，如果方法有返回值，可以得到返回值。
</pre>

![](image/tag_get_ognl3.png)

<pre>
不仅得到对象的Ognl值，还可以链式的得到其对应的Ognl值。
如student.name为String类型，所以还可以得到name对应的String方法。
</pre>

![](image/tag_get_ognl4.png)

<pre>
用&lt;get&gt;得到它们的值。
</pre>

![](image/tag_get_ognl5.png)

<pre>
输出结果
</pre>

![](image/tag_get_ognl6.png)

<pre>
小贴士：在&lt;get&gt;的value的中，把鼠标放在上面，或者选中，可以提示出这个变量的Ognl值。
</pre>

<pre>鼠标放在上面</pre>
![](image/tag_get_ognl7.png)

<pre>选中需要的部分</pre>
![](image/tag_get_ognl8.png)
