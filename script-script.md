# <div align="center"><% %> - 脚本</div> #

----------

###目录:###

* [格式与用法](#1)
* [原理](#2)

----------

##<span id="1">格式与用法</span>##

格式：<font color="blue"><% %> </font>，在此可以写java代码和逻辑。

![](image/tag_script.png)

----------

##<span id="2">原理</span>##

查看这个模板的编译类后，可以看到，<% %>块的内容编译到方法generate()中。

![](image/tag_script_class.png)

----------