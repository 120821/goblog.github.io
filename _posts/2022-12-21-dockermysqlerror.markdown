---
layout: post
title: "docker MySQL error "
date: "2022-12-21"
categories: 
---
<p>运行docker mysql 的时候，出现了错误，数据库不能成功创建：</p>
{% highlight html %}Can&#39;t connect to local MySQL server through socket &#39;/tmp/mysql.sock&#39; (2){% endhighlight %}
<p>{% highlight html %}查看MySQL的ip，进行替换 {% endhighlight %}</p>
<p>docker inspect [OPTIONS] NAME|ID [NAME|ID...]</p>
<p>{% highlight html %}sudo docker inspect mysql{% endhighlight %}</p>
<p>{% highlight html %}把ipaddress进行替换为config/database.yml的host{% endhighlight %}</p>
