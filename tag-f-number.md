# <div align="center">f:number - 格式化数字</div> #

&lt;f:number&gt;
<pre>
格式化数字
</pre>

#### 说明 ####

<pre>
根据标签内填写的数字符串，输出格式化的数字，或者设置格式化的数字参数。
</pre>

#### 属性 ####

<pre>
<b>var（可选）</b>
存储格式化数字的变量
注：如果设置了var属性，不会输出结果
</pre>

<pre>
<b>setScope（可选）</b>
设置变量的作用域

<b>属性</b>
ontext:设置变量到context中（默认）
session:设置变量到session中
</pre>

<pre>
<b>pattern（可选）</b>
格式化的样式

如: 12.34
"0.0"      ->   12.3      
"#.#"      ->   12.3
"000.000"  ->   012.340
"###.###"  ->   12.34 
具体用法参考java.text.DecimalFormat
</pre>

<pre>
<b>type（可选）</b>
类型

<b>属性</b>
number:数值（默认）
currency:货币
percent:百分数
</pre>

<pre>
<b>groupingUsed（可选）</b>
是否对数字分组

<b>属性</b>
true:是
false:否（默认）
</pre>

<pre>
<b>currencyCode（可选）</b>
ISO 4217 货币码，默认为当前区域货的货币码，当type="currency"时可用
如：
人民币是 CNY
美元是 USD
</pre>

<pre>
<b>currencySymbol（可选）</b>
货币符号，默认为当前区域的货币符号，当type="currency"时可用
如：
人民币是 ￥
美元是 $
</pre>

<pre>
<b>locale（可选）</b>
国家，默认为当前所在国
如：
中国是 zh_CN
美国是 en_US
</pre>

<pre>
<b>integerOnly（可选）</b>
是否只解析整型数

<b>属性</b>
true:是，整数型
false:否，浮点数（默认）
</pre>

<pre>
<b>maxIntegerDigits（可选）</b>
整型数最大的位数
</pre>

<pre>
<b>minIntegerDigits（可选）</b>
整型数最小的位数
</pre>

<pre>
<b>maxFractionDigits（可选）</b>
小数点后最大的位数
</pre>

<pre>
<b>minFractionDigits（可选）</b>
小数点后最小的位数
</pre>

#### 其它 ####

<pre>
如果设置了var属性，不会输出结果
</pre>

----------

#### 实例演示 ####

<pre>
例子1
</pre>

![](image/f_number_tag_template1.png)

![](image/f_number_result1.png)