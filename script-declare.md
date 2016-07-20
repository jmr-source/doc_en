# <div align="center"><%! %> - 声明</div> #

----------

###目录:###

* [格式与用法](#1)
* [原理](#2)

----------

##<span id="1">格式与用法</span>##

格式：<font color="blue"><%! %> </font>，在此可以声明模板的变量和函数，相当于类成员。

![](image/tag_delcare.png)

----------

##<span id="2">原理</span>##

查看这个模板的编译类后，可以看到，<%! %>块的内容转换成java类成员。

![](image/tag_declare_class.png)

----------





