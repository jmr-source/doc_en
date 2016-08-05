# <div align="center">nl - Newline</div> #

&lt;nl&gt;
<pre>
Output newline in the template
</pre>

#### Description ####

<pre>
In the template according to the different system, 
output newline, can also set newline count.
</pre>

#### Property ####

<pre>
<b>count（optional）</b>
The number of newline characters in the output, the value must 
be a positive integer
</pre>

#### Other ####

<pre>
Enter "\n" in the template, and can not really realize the output 
line and operation line, and can only output the character "\n" 
itself. So you need to use this tag to output. You can also 
use &lt;% out.wirte("\n"); %&gt; to the same effect.

Different system output newline is not the same：
Mac \r
Unix/Linux \n
Windows \n or \r\n
</pre>

----------

#### Examples ####

<pre>
Example 1
</pre>


![](image/nl_tag_template1.png)

![](image/nl_tag_result1.png)