---
layout: post
title: "Use SCP Local to Remote"
date: "2022-09-20"
categories: 
---
<p><a href="https://linuxize.com/post/how-to-use-scp-command-to-securely-transfer-files/">https://linuxize.com/post/how-to-use-scp-command-to-securely-transfer-files/</a></p>
<p>把文件从本地推送到远程服务器</p>
<p>首先进行压缩文件，zip -q -r&nbsp; asdf.zip *</p>
<p>然后进行文件的传送：</p>
{% highlight html %}scp file.txt remote_username@10.10.0.2:/remote/directory{% endhighlight %}
{% highlight html %}scp test_linlin_blog.zip root@linlin.fun:~/workspace/{% endhighlight %}
<p>{% highlight html %}这样就可以传送成功了：{% endhighlight %}</p>
<p><img height="72" src="/uploads/ckeditor/pictures/411/image-20220920091135-1.png" width="1920" /></p>
<p>在远程进行解压缩:</p>
{% highlight html %}unzip asdf.zip{% endhighlight %}
