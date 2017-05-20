# 第一步. 在浏览器输入URL

## 什么是URL

 　URL（Uniform Resource Locator：统一资源定位器）用于定位互联网上的资源

是WWW页的地址，它从左到右由下述部分组成：

 　Internet资源类型（scheme）：指出WWW客户程序用来操作的工具。如“http：//”表示WWW服务器，“ftp：//”表示FTP服务器，“gopher：//”表示Gopher服务器，而“new：”表示Newgroup新闻组。

 　服务器地址（host）：指出WWW页所在的服务器域名。

　 端口（port）：有时（并非总是这样），对某些资源的访问来说，需给出相应的服务器提供端口号。

　 路径（path）：指明服务器上某资源的位置（其格式与DOS系统中的格式一样，通常有目录/子目录/文件名这样结构组成）。与端口一样，路径并非总是需要的。

　 URL地址格式排列为：scheme：//host：port/path，例如http：//www.sohu.com/domain/HXWZ就是一个典型的URL地址。

它有如下 http、https、ftp、file 协议
    http 线上网站

    file  本地

    https 经过了安全加密处理的http协议

    //  相对于该网页，如果网页为http 则代表了 http目录下；如果为本地，那么该网页就是file的地址

    在地址栏，输入相应地址就可进入该网站　　例如:输入www.baidu.com　则进入百度

# 第二步. 域名解析

    对于http://www.baidu.com的URL，浏览器实际上不知道www.baidu.com到底是什么东西，需要查找www.baidu.com网站所在服务器的IP地址，才能找到目标

为什么要发明域名，不直接用IP?
方便记忆

    域名是什么?

    对于http://www.baidu.com:8080/blog,www.baidu.com就是域名

IP地址是什么?
    IP地址是在网络上分配给每台计算机或网络设备的32位数字标识。在Internet上，每台计算机或网络设备的IP地址是全世界唯一的。IP地址的格式是 xxx.xxx.xxx.xxx，其中xxx是 0 到 255 之间的任意整数。例如，每步站主机的IP地址是 219.134.132.131。

    每一台联网的计算机无权自行设定IP地址，有一个统一的机构—IANA负责对申请的组织分配唯一的网络ID,而该组织可以对自己的网络中的每一个主机分配一个唯一的主机ID，正如一个单位无权决定自己在所属城市的街道名称和门牌号，但可以自主决定本单位内部的各个办公室编号一样。

    分为公网和局域网

    每个处于互联网中的设备都有IP 地址，形如192.168.0.1

    局域网 IP 和公网 IP 是有差别的

    127.0.0.1代表本机的 IP

## 域名解析的流程
    - 浏览器缓存 – 浏览器会缓存DNS记录一段时间

    - 系统缓存 - 从 Hosts 文件查找是否有该域名和对应 IP。

    - 路由器缓存 – 一般路由器也会缓存域名信息。

    - ISP DNS 缓存 – 比如到电信的 DNS 上查找缓存。

    如果都没有找到，则向根域名服务器查找域名对应 IP，根域名服务器把请求转发到下一级，知道找到 IP

Question:电脑上不了网，为什么修改dns为8.8.8.8 或者114.114.114.114?

dns 劫持是什么？

Answer：之所以连不上网，就是因为DNS混乱，所以改为8.8.8.8直接访问谷歌，即可解决，114.114.114.114是国内一个比较大的运营网站。

    DNS劫持，会让一些伪站冒充正规网址，因为域名都一样，所以很容易上当受骗

# 第三步. 服务器处理

    服务器是一台安装系统的机器，常见的系统如Linux、windows server 2012

    系统里安装的处理请求的应用叫 Web server

Web服务器
    常见的 web服务器有 Apache、Nginx、IIS、Lighttpd

    web服务器接收用户的Request 交给网站代码，或者接受请求反向代理到其他 web服务器。


# 第四步. 网站处理流程

    MVC 模型(model)-视图(view)-控制器(controller)



# 第五步. 浏览器处理

    HTML字符串被浏览器接受后被一句句读取解析

    解析到link 标签后重新发送请求获取css

    解析到 script标签后发送请求获取 js，并执行代码

    解析到img 标签后发送请求获取图片资源

# 第六步. 绘制网页

    浏览器根据 HTML 和 CSS 计算得到渲染树，绘制到屏幕上

    js 会被执行
