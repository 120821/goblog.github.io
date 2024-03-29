---
layout: post
title: "http https的区别"
date: "2023-06-28"
categories: 
---
<p>HTTP和HTTPS是网络通信协议，两者之间的主要区别在于安全性。</p>
<p>1. 安全性：HTTP是明文传输的协议，数据在传输过程中不加密，容易被窃听和篡改。而HTTPS是通过SSL/TLS协议进行加密传输，数据在传输过程中经过加密处理，更安全可靠。</p>
<p>2. 默认端口：HTTP默认使用端口号80进行通信，而HTTPS默认使用端口号443。</p>
<p>3. 证书：为了确保HTTPS连接的安全性，网站需要使用SSL证书。HTTPS连接在通信开始前会进行握手过程，浏览器会验证网站的证书是否有效，以确保安全连接。而HTTP不需要证书验证，通信者的身份和网站的真实性无法得到确认。</p>
<p>4. 使用场景：HTTP常用于一般的网页浏览、数据传输等场景，而HTTPS更常用于涉及用户个人隐私、金融支付等需要更高安全性的场景。</p>
<p>需要注意的是，HTTPS使用SSL/TLS协议进行加密通信，这会造成少许的额外计算和通信开销，使得HTTPS的传输速度稍慢于HTTP。但由于现代计算机和网络的快速发展，HTTPS的性能损耗已经大大减少，所以在绝大多数情况下，HTTPS是更安全、更推荐的通信协议。</p>
<p>解释：</p>
<p>为什么使用http://8.218.91.233:8888/managers/sign_in可以打开，使用https://8.218.91.233:8888/managers/sign_in不能打开</p>
<p>有几个可能的原因可以解释为什么使用HTTP可以打开，而使用HTTPS无法打开：</p>
<p>1. 证书问题：HTTPS通信需要使用有效的SSL证书。如果您在使用HTTPS时无法打开网站，可能是由于网站的SSL证书无效、过期或不受信任，或者您的浏览器没有正确识别该证书。在这种情况下，您的浏览器会提示您关于不信任证书的警告。您可以尝试忽略此警告继续访问，但这不推荐，因为可能存在安全风险。</p>
<p>2. 防火墙设置：有时，网络中的防火墙可能会阻止HTTPS流量通过特定端口（如8888端口）的传输。防火墙可能配置成只允许通过HTTP的传输而阻止HTTPS。如果您无法使用HTTPS访问网站，请检查您的网络设置或联系网络管理员。</p>
<p>3. 服务器配置问题：网站服务器可能未正确配置来处理HTTPS连接。服务器可能没有正确安装或配置SSL证书，或没有在指定的端口（如8888）上打开HTTPS服务。这将导致无法使用HTTPS访问服务器。</p>
<p>综上所述，您无法使用HTTPS访问给定的网址可能归因于无效的证书、防火墙设置或服务器配置问题。如果您希望使用HTTPS访问网站，请确保SSL证书有效，并检查网络设置和服务器配置。</p>
