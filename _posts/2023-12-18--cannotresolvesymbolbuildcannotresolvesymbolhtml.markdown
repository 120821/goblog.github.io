---
layout: post
title: "安卓逆向-Cannot resolve symbol 'Build' Cannot resolve symbol 'Html'"
date: "2023-12-18"
categories: 
---
<p>在使用raw的时候，提示：<br />
Cannot resolve symbol &#39;Build&#39;<br />
Cannot resolve symbol &#39;Html&#39;</p>
<p>需要先安装依赖：</p>
<p>1.在配置文件里增加：</p>
<p>在你的模块级别的 {% highlight html %}build.gradle{% endhighlight %} 文件中</p>
{% highlight html %}implementation <span style="color:#abe338">&#39;androidx.appcompat:appcompat:1.3.1&#39;</span>
implementation <span style="color:#abe338">&#39;androidx.core:core-ktx:1.6.0&#39;</span>{% endhighlight %}
<p>在.java文件里增加：</p>
{% highlight html %}<span style="color:#dcc6e0">import</span> android.os.Build;
<span style="color:#dcc6e0">import</span> android.text.Html;{% endhighlight %}
<p>2.在顶部菜单里进行rebuild</p>
<p>3.然后重新运行</p>
<p>&nbsp;</p>
