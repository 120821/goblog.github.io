---
layout: post
title: "Nuxt.js ---创建项目---hello world"
date: "2022-06-09"
categories: 
---
<blockquote> 
<p>创建有不同的方法，一是命令行系统创建，二是手动创建目录配置文件。</p> 
<p><strong>系统创建：</strong>首先在命令行输入命令即可创建项目</p> 
{% highlight html %}yarn create nuxt-app &lt;project-name&gt;
{% endhighlight %} 
<p style="text-align:center;"><img alt="" src="https://img-blog.csdnimg.cn/36ec6d47cb2d40e191bcc6e701760900.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6K645aKo44Gu5bCP6J206J22,size_20,color_FFFFFF,t_70,g_se,x_16"></p> 
</blockquote> 
<blockquote> 
<p style="text-align:center;">项目创建会有一些选中，根据需要进行选择即可，一般会选中</p> 
{% highlight html %}添加 axios module 以轻松地将 HTTP 请求发送到您的应用程序中。
添加 EsLint 以在保存时代码规范和错误检查您的代码。
添加 Prettier 以在保存时格式化/美化您的代码。{% endhighlight %} 
<p style="text-align:center;">项目创建好会有这样的提示<img alt="" src="https://img-blog.csdnimg.cn/4a22adf4779e47fc83fa078b1f7bf4f7.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6K645aKo44Gu5bCP6J206J22,size_20,color_FFFFFF,t_70,g_se,x_16"></p> 
</blockquote> 
<blockquote> 
<p>进入项目输入命令就可启动项目</p> 
{% highlight html %}npm run dev{% endhighlight %} 
<p style="text-align:center;"><img alt="" src="https://img-blog.csdnimg.cn/9ab429a3eac54360b5e161ca13ce48db.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6K645aKo44Gu5bCP6J206J22,size_20,color_FFFFFF,t_70,g_se,x_16"></p> 
</blockquote> 
<blockquote> 
<p><strong>手动创建</strong></p> 
<p>如果不使用 Nuxt.js 提供的 starter 模板，我们也可以从头开始新建一个 Nuxt.js 应用项目，过程非常简单，只需要 <em>1 个文件和 1 个目录</em>。如下所示：</p> 
{% highlight html %}$ mkdir &lt;项目名&gt;
$ cd &lt;项目名&gt;
{% endhighlight %} 
<h3 id="新建-packagejson-文件">新建 package.json 文件</h3> 
<p>{% highlight html %}package.json{% endhighlight %} 文件用来设定如何运行 {% highlight html %}nuxt{% endhighlight %}：</p> 
{% highlight html %}{
"name": "my-app",
"scripts": {
"dev": "nuxt"
}
}
{% endhighlight %} 
<p>上面的配置使得我们可以通过运行 {% highlight html %}npm run dev{% endhighlight %} 来运行 {% highlight html %}nuxt{% endhighlight %}</p> 
<p>过以下 npm 命令将 {% highlight html %}nuxt{% endhighlight %} <strong>安装</strong>至项目中：</p> 
{% highlight html %}$ npm install --save nuxt
{% endhighlight %} 
</blockquote> 
<blockquote> 
<p>创建 {% highlight html %}pages{% endhighlight %} 目录：</p> 
{% highlight html %}$ mkdir pages
{% endhighlight %} 
<p>创建我们的第一个页面 {% highlight html %}pages/index.vue{% endhighlight %}：</p> 
{% highlight html %}&lt;template&gt;
&lt;h1&gt;Hello world!&lt;/h1&gt;
&lt;/template&gt;
{% endhighlight %} 
</blockquote> 
<blockquote> 
<p>然后启动项目：</p> 
{% highlight html %}$ npm run dev
{% endhighlight %} 
<p>现在我们的应用运行在 http://localhost:3000 上运行</p> 
<img alt="" src="https://img-blog.csdnimg.cn/6f6ffd7f3c74453089999340af218f66.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA6K645aKo44Gu5bCP6J206J22,size_20,color_FFFFFF,t_70,g_se,x_16">
</blockquote>
