# <div align="center">tab - Tab</div> #

&lt;tab&gt;
<pre>
Output tab in the template
</pre>

#### Description ####

<pre>
Output tab in the template, can also set tabs count.
</pre>

#### Property ####

<pre>
<b>count（optional）</b>
The number of tab characters in the output, 
the value must be a positive integer
</pre>

#### Other ####

<pre>
Enter the "\t" in the template, and can not really output tabs, 
and can only output the character "\t" itself. 
So you need to use this tag to output. You can also 
use &lt;% out.wirte("\t"); %&gt; to the same effect.
</pre>

----------

#### Examples ####

<pre>
Example 1
</pre>

![](image/tab_tag_template1.png)

<pre>
Please open the generated file outside the eclipse, eclipse due 
to the font size problem, the display content may not be aligned.
</pre>
![](image/tab_tag_result1.png)