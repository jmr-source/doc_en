
<a href="tag-include.html">查看文档请点此</a>

### <div align="center">include - 嵌套模板</div> ###

&lt;include&gt;
<pre>
用于模板之间的嵌套调用。
</pre>

#### 说明 ####

<pre>
为了方便模板的复用，可以在模板中调用其它模板的标签。
</pre>

#### 属性 ####
<span id="1"></span>
<pre>
src（必须）:嵌套的模板路径，可以是相对模板路径，也可以是相对项目根路径的路径。
</pre>

#### 其它 ####

<pre>
被嵌套的模板和当前模板，共享同一个context，它们有共同的参数。
</pre>