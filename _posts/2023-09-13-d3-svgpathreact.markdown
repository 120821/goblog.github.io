---
layout: post
title: "d3 - svg path react 标签的简单使用"
date: "2023-09-13"
categories: 
---
<p>refer: <a href="http://siwei.me/blog/posts/d3-svg-path">http://siwei.me/blog/posts/d3-svg-path</a></p>

<p><a href="https://www.w3schools.com/graphics/svg_path.asp">https://www.w3schools.com/graphics/svg_path.asp</a></p>

<p>1.安装依赖d3库</p>

<pre>
<code>npm install d3</code></pre>

<p><code>或</code></p>

<pre>
<code>yarn add d3</code></pre>

<p><code>2.</code>在React组件中导入D3和react的useEffect钩子</p>

<pre>
<code>import React, { useEffect } from &#39;react&#39;;
import * as d3 from &#39;d3&#39;;</code></pre>

<p><code>3.</code>在钩子里使用D3：</p>

<pre>
<code>const MyComponent = () =&gt; {
  useEffect(() =&gt; {
    // D3 的路径生成器
    const pathGenerator = d3.path();

    // 设置路径命令
    pathGenerator.moveTo(50, 50);
    pathGenerator.lineTo(200, 50);
    pathGenerator.lineTo(200, 200);
    pathGenerator.closePath();

    // 创建 SVG 路径元素
    const svgPath = pathGenerator.toString();

    // 在控制台输出 SVG 路径字符串
    console.log(svgPath);
  }, []);

  return &lt;svg /&gt;;
};</code></pre>

<p><code>4.</code>在jsx中渲染svg:</p>

<pre>
<code>const MyComponent = () =&gt; {
  const svgRef = useRef(null);

  useEffect(() =&gt; {
    // D3 的路径生成器...
    // ...

    // 获取 SVG 元素的引用
    const svgElement = d3.select(svgRef.current);

    // 添加 SVG 路径元素到 SVG 元素中
    svgElement.append(&#39;path&#39;).attr(&#39;d&#39;, svgPath);
  }, []);

  return &lt;svg ref={svgRef} /&gt;;
};</code></pre>

<p>做了一个简单的Demo：<a href="https://github.com/120821/react_learn_for_d3_svg_path_20230912">https://github.com/120821/react_learn_for_d3_svg_path_20230912</a></p>
