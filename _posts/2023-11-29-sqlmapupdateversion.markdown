---
layout: post
title: "sqlmap update version"
date: "2023-11-29"
categories: 
---
<p><a href="https://zhuanlan.zhihu.com/p/607669763?utm_id=0">https://zhuanlan.zhihu.com/p/607669763?utm_id=0</a></p>
<p>1.需要已经安装了sqlmap，例如：</p>
{% highlight html %}sqlmap <span style="color:#d4d0ab">--version</span>
<span style="color:#f5ab35">1.6</span><span style="color:#f5ab35">.4</span>#<span style="color:#dcc6e0">stable</span>
[<span style="color:#f5ab35">09</span>:<span style="color:#f5ab35">09</span>:<span style="color:#f5ab35">05</span>] [<span style="color:#f5ab35">WARNING</span>] your sqlmap <span style="color:#dcc6e0">version</span> <span style="color:#dcc6e0">is</span> outdated{% endhighlight %}
<p>{% highlight html %}2.如果要消除警告，可以更新sqlmap的版本{% endhighlight %}</p>
{% highlight html %}sudo sqlmap --<span style="color:#dcc6e0">update</span>{% endhighlight %}
<p>3.查看安装的版本：</p>
{% highlight html %}sqlmap <span style="color:#d4d0ab">--version</span>
{% endhighlight %}
<p>或者使用</p>
{% highlight html %}<span style="color:#ffa07a">/usr/</span>bin<span style="color:#ffa07a">/python3 /</span>path<span style="color:#ffa07a">/to/</span>sqlmap --version{% endhighlight %}
{% highlight html %}将 `<span style="color:#ffa07a">/path/</span>to/sqlmap` 替换为实际的 `sqlmap` 路径。{% endhighlight %}
<p>{% highlight html %}得到了{% endhighlight %}，例如这样的</p>
<p>1.7.11.3#dev</p>
<p>&nbsp;</p>
