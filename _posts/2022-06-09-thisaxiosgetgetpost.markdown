---
layout: post
title: "this.$axios.$get 请求后台接口数据（get请求和post请求）"
date: "2022-06-09"
categories: 
---
<p>安装</p> 
{% highlight html %}npm install vue-axios --save
{% endhighlight %} 
<p>main.js文件</p> 
{% highlight html %}import axios from 'axios'
Vue.prototype.$http = axios{% endhighlight %} 
<p>.vue文件</p> 
{% highlight html %}test(){
var testUrl='http://localhost:8088/activiti/doneTask';
this.$http.get(testUrl).then(function(response){
alert(response.data);
}).catch(function (response) {
alert("error");
})
},{% endhighlight %} 
<p>  </p>
<hr>
<p><strong>请求后台接口数据（get请求和post请求）</strong><br><strong>1.get请求</strong></p> 
<ul><li>不需要带参数的get请求</li></ul>
{% highlight html %}
this.$axios.get(this.GLOBAL.host.+“后台接口地址”).then(res =&amp;gt; {
//获取你需要用到的数据
})
{% endhighlight %} 
<ul><li>需要带参数的get请求</li></ul>
{% highlight html %}
this.$axios.get(this.GLOBAL.host.+“后台接口地址”,{
params:{            
phone:12345678   //参数，键值对，key值：value值
name:hh
}
}).then(res =&amp;gt; {
//获取你需要用到的数据
});
{% endhighlight %} 
<p><strong>2.post请求</strong></p> 
{% highlight html %}
var data = {phone：12345678，name：hh}  //定义一个data储存需要带的参数
this.$axios.post(this.GLOBAL.host+“后台接口地址”，this.$qs.stringify(data)
).then(res =&amp;gt;{
//获取你需要的数据
});
{% endhighlight %} 
<p><strong>// main.js文件</strong></p> 
{% highlight html %}
import axios from "axios";
import qs from 'qs';
import Global from '../static/config/global';
Vue.prototype.$axios = axios
Vue.prototype.$qs = qs;
Vue.prototype.GLOBAL = Global;{% endhighlight %}
