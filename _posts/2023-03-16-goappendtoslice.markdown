---
layout: post
title: "go append to slice"
date: "2023-03-16"
categories: 
---
<p><a href="https://go.dev/tour/moretypes/15">https://go.dev/tour/moretypes/15</a></p>
<p>附加到切片 : 将新元素附加到切片是很​​常见的，因此 Go 提供了一个内置的 {% highlight html %}append{% endhighlight %}功能。 文档 <a href="https://go.dev/pkg/builtin/#append" target="_self">_ </a> 内置包的描述 {% highlight html %}append{% endhighlight %}.</p>
{% highlight html %}func append(s []T, vs ...T) []T {% endhighlight %}
<p>第一个参数 {% highlight html %}s{% endhighlight %}的 {% highlight html %}append{% endhighlight %}是类型的一部分 {% highlight html %}T{% endhighlight %}，其余的是 {% highlight html %}T{% endhighlight %}要附加到切片的值。</p>
<p>结果值 {% highlight html %}append{% endhighlight %}是包含所有元素的切片 原始切片加上提供的值。</p>
<p>如果支持数组 {% highlight html %}s{% endhighlight %}太小而无法适应所有给定的值 数组将被分配。 返回的切片会指向新分配的 大批。</p>
{% highlight html %}package main
import &quot;fmt&quot;
func main() {
&nbsp;&nbsp; &nbsp;var s []int
&nbsp;&nbsp; &nbsp;printSlice(s)
&nbsp;&nbsp; &nbsp;// append works on nil slices.
&nbsp;&nbsp; &nbsp;s = append(s, 0)
&nbsp;&nbsp; &nbsp;printSlice(s){% endhighlight %}
<p>&nbsp;</p>
<p>&nbsp;&nbsp; &nbsp;// The slice grows as needed.<br />
&nbsp;&nbsp; &nbsp;s = append(s, 1)<br />
&nbsp;&nbsp; &nbsp;printSlice(s) &nbsp;&nbsp; &nbsp;// We can add more than one element at a time.<br />
&nbsp;&nbsp; &nbsp;s = append(s, 2, 3, 4)<br />
&nbsp;&nbsp; &nbsp;printSlice(s)<br />
} func printSlice(s []int) {<br />
&nbsp;&nbsp; &nbsp;fmt.Printf(&quot;len=%d cap=%d %v\n&quot;, len(s), cap(s), s)<br />
}</p>
{% highlight html %}go run appending_to_slice.go
len=0 cap=0 []
len=1 cap=1 [0]
len=2 cap=2 [0 1]
len=5 cap=6 [0 1 2 3 4]{% endhighlight %}
<p>&nbsp;</p>
