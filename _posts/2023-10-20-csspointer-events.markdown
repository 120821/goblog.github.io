---
layout: post
title: "css pointer-events的三种使用"
date: "2023-10-20"
categories: 
---
<p>对于多层中国地图导致不能正常显示tooltip的情况，使用css pointer-events禁用元素的鼠标事件响应，可以解决，</p>
{% highlight html %}.disable-events {
pointer-events: none;
}
{% endhighlight %}
<p>禁用元素的鼠标事件响应，但保持鼠标指针可见，&nbsp;鼠标事件会穿透到元素下面的元素</p>
{% highlight html %}.disable-events-visible-pointer {
pointer-events: none;
cursor: default;
}{% endhighlight %}
<p>禁用元素的鼠标事件响应，并隐藏鼠标指针</p>
{% highlight html %}.hide-pointer-events {
pointer-events: none;
cursor: none;
}{% endhighlight %}
