---
layout: post
title: "ubuntu mysql: Access denied for user 'root'@'localhost'"
date: "2023-04-24"
categories: 
---
<p><a href="http://siwei.me/blog/posts/mysql--9">http://siwei.me/blog/posts/mysql--9</a></p>
<p>使用这个方法：（参考： <a href="https://stackoverflow.com/a/52674808/445908">https://stackoverflow.com/a/52674808/445908</a>）</p>
<p>sudo mysql -u root</p>
<p>可以正常进入数据库，但是使用rake db:create/migrate不能正常进行操作提示user@localhost不正确。</p>
<p>可以创建user然后继续操作：</p>
<p>首先创建了数据库：first_database, first_database_test</p>
<p>Then create a normal user, set a password, then use that user to work.</p>
<p>{% highlight html %}create user &#39;user&#39;@&#39;localhost&#39; identified by &#39;user1234&#39;;<br />
grant all on your_database.* to &#39;user&#39;@&#39;localhost&#39;;{% endhighlight %}</p>
<p>{% highlight html %}（例如： grant all on first_database.* to &#39;user&#39;@&#39;localhost&#39;;）{% endhighlight %}</p>
<p>{% highlight html %}(grant all on first_database._test* to &#39;user&#39;@&#39;localhost&#39;;)<br />
select host, user from mysql.user;{% endhighlight %}</p>
<p>{% highlight html %}Then try to access:{% endhighlight %}</p>
<p>{% highlight html %}mysql -u user -puser1234{% endhighlight %}</p>
<p>然后在config/database.yml修改user和password就可以migrate了</p>
<p>{% highlight html %}user: user{% endhighlight %}</p>
<p>{% highlight html %}password: user1234{% endhighlight %}</p>
<p>&nbsp;</p>
