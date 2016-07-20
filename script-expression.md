# <div align="center"><%= %> - 表达式</div> #

----------

###目录:###

* [格式与用法](#1)
* [原理](#2)

----------

##<span id="1">格式与用法</span>##

格式：<font color="blue"><%= %> </font>，输出值，这个值可以是个变量，字符串，数值，返回函数等，  
可以看成<% out.write() %>，关于out内置对象(<a href="out.html">详细请点击</a>)。

![](image/tag_expression.png)

----------

##<span id="2">原理</span>##

查看这个模板的编译类后，可以看到，<%=%>块的内容编译到方法generate()中成为<% out.write() %>。

![](image/tag_expression_class.png)

----------