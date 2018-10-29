## charles mac版手机抓包

- [官网](http://front-docs.adbaitai.com/%E6%95%99%E7%A8%8B%E5%9F%B9%E8%AE%AD/charles%E6%95%99%E7%A8%8B.html#%E5%AE%98%E7%BD%91)
- [安装设置](http://front-docs.adbaitai.com/%E6%95%99%E7%A8%8B%E5%9F%B9%E8%AE%AD/charles%E6%95%99%E7%A8%8B.html#%E5%AE%89%E8%A3%85%E8%AE%BE%E7%BD%AE)
- [手机抓包设置](http://front-docs.adbaitai.com/%E6%95%99%E7%A8%8B%E5%9F%B9%E8%AE%AD/charles%E6%95%99%E7%A8%8B.html#%E9%93%BE%E6%8E%A5%E8%AE%BE%E7%BD%AE)
- 抓包分析
  - [overview](http://front-docs.adbaitai.com/%E6%95%99%E7%A8%8B%E5%9F%B9%E8%AE%AD/charles%E6%95%99%E7%A8%8B.html#overview)
  - [request](http://front-docs.adbaitai.com/%E6%95%99%E7%A8%8B%E5%9F%B9%E8%AE%AD/charles%E6%95%99%E7%A8%8B.html#request)
  - [response](http://front-docs.adbaitai.com/%E6%95%99%E7%A8%8B%E5%9F%B9%E8%AE%AD/charles%E6%95%99%E7%A8%8B.html#response)
- 高级功能
  - [禁止缓存](http://front-docs.adbaitai.com/%E6%95%99%E7%A8%8B%E5%9F%B9%E8%AE%AD/charles%E6%95%99%E7%A8%8B.html#%E7%A6%81%E6%AD%A2%E7%BC%93%E5%AD%98)
  - [禁止cookie](http://front-docs.adbaitai.com/%E6%95%99%E7%A8%8B%E5%9F%B9%E8%AE%AD/charles%E6%95%99%E7%A8%8B.html#%E7%A6%81%E6%AD%A2cookie)
  - 远程映射
    - [设置](http://front-docs.adbaitai.com/%E6%95%99%E7%A8%8B%E5%9F%B9%E8%AE%AD/charles%E6%95%99%E7%A8%8B.html#%E8%BF%9C%E7%A8%8B%E6%98%A0%E5%B0%84)
    - [查看远程映射记录](http://front-docs.adbaitai.com/%E6%95%99%E7%A8%8B%E5%9F%B9%E8%AE%AD/charles%E6%95%99%E7%A8%8B.html#%E6%9F%A5%E7%9C%8B%E8%BF%9C%E7%A8%8B%E6%98%A0%E5%B0%84%E8%AE%B0%E5%BD%95)
    - [远程映射非常有用](http://front-docs.adbaitai.com/%E6%95%99%E7%A8%8B%E5%9F%B9%E8%AE%AD/charles%E6%95%99%E7%A8%8B.html#%E8%BF%9C%E7%A8%8B%E6%98%A0%E5%B0%84%E9%9D%9E%E5%B8%B8%E6%9C%89%E7%94%A8)
- 断点
  - [重要作用](http://front-docs.adbaitai.com/%E6%95%99%E7%A8%8B%E5%9F%B9%E8%AE%AD/charles%E6%95%99%E7%A8%8B.html#%E9%87%8D%E8%A6%81%E4%BD%9C%E7%94%A8)
  - [设置](http://front-docs.adbaitai.com/%E6%95%99%E7%A8%8B%E5%9F%B9%E8%AE%AD/charles%E6%95%99%E7%A8%8B.html#%E8%AE%BE%E7%BD%AE)
  - [使用示例，request修改cookie](http://front-docs.adbaitai.com/%E6%95%99%E7%A8%8B%E5%9F%B9%E8%AE%AD/charles%E6%95%99%E7%A8%8B.html#%E4%BD%BF%E7%94%A8%E7%A4%BA%E4%BE%8B%EF%BC%8Crequest%E4%BF%AE%E6%94%B9cookie)
- [https抓包](http://front-docs.adbaitai.com/%E6%95%99%E7%A8%8B%E5%9F%B9%E8%AE%AD/charles%E6%95%99%E7%A8%8B.html#https%E6%8A%93%E5%8C%85)
- [其它功能](http://front-docs.adbaitai.com/%E6%95%99%E7%A8%8B%E5%9F%B9%E8%AE%AD/charles%E6%95%99%E7%A8%8B.html#%E5%85%B6%E5%AE%83%E5%8A%9F%E8%83%BD)

### 官网

[http://www.charlesproxy.com](http://www.charlesproxy.com/)

### 安装设置

mac按提示安装

安装完成后需要给charles权限,如果没有给予权限，charles无法抓包。

点击proxy->MAC OS X proxy

![img](http://wd.geilicdn.com/5302846b55bfdd37e50cdffa911baaa1.png)

### 链接设置

![img](http://wd.geilicdn.com/9c9a8999f37e0dcb1a693b055072d8c3.jpg)

ifconfig 找到电脑ip 服务器填电脑ip 端口默认8888（下图）

![img](http://wd.geilicdn.com/7329b383030de145c512450f811debb3.jpg)

此时charles会自动弹出对话问是否允许通过chales代理访问。点击allow。如果想默认允许任何用户访问， 打开 面包Setting->Access Control Settings面板，点击add按钮 增加 <0.0.0.0>/0，以后就不会有该对话了。

### 抓包分析

#### overview

![img](http://wd.geilicdn.com/64c8e8965e4447ba28a330681b555a46.png)

（上图）包含了请求一些基本信息，如地址，请求方式、内容类型、耗时等等

#### request

![img](http://wd.geilicdn.com/733cc67d3051e3131cba5b6e2ec4c612.png)

(上图) 上图包含的信息非常重要， 说明此处http请求有多少数据发给服务端，如常用的cookie信息和user-agent（浏览器表示）信息

Query string 、 Cookies 和 Raw tab为格式化信息，方便查看（下图）

![img](http://wd.geilicdn.com/b30ed7940330a550e41ad8388f1d5cf5.png)

双击后可以复制里面信息，不可编辑（如下图）

![img](http://wd.geilicdn.com/856ec0ae20c2b094aa395db9557e1d2b.png)

#### response

可以看到非常详细返回信息,Set-cookie,表明本次请求服务端设置了哪些cookie（双击后可复制不可编辑）

![img](http://wd.geilicdn.com/31f24d8896fa3f1a11fc83a2fc370c94.png)

Summary、Chart、Notes等是请求耗时解析，建议在chrome浏览器查看，更加详细和一目了然（以下chrome截图）

![img](http://wd.geilicdn.com/01ea3a51a2c2c6700c8749385517af81.png)

> Queueing 浏览器有连接限制，当网页资源很多时就会出现排队的现象，排队的资源要等到上一个资源加载完毕释放后才能开始请求。比关键资源（如javascript与css）低优先级的请求会被浏览器推迟，一般推迟的都是图片。在许多资源同时发起请求时浏览器默认先加载css,然后javascript，最后才是图片。
>
> Stalled 浏览器得到要发出这个请求的指令，到请求可以发出的等待时间，一般是代理协商、以及等待可复用的TCP连接释放的时间，不包括DNS查询、建立TCP连接等时间等
>
> Request sent 请求第一个字节发出前到最后一个字节发出后的时间，也就是上传时间
>
> Waiting 请求发出完成后，到收到响应的第一个字节所花费的时间(Time To First Byte)，即响应时间
>
> Content Download 收到响应的第一个字节，到接受完最后一个字节的时间，就是下载时间

### 高级功能

#### 禁止缓存

![img](http://wd.geilicdn.com/e175b11d19b9ae5ee59f34ffd5aa0033.png)

#### 禁止cookie

![img](http://wd.geilicdn.com/50abc28165e013d235082fbb371d0a7a.png)

#### 远程映射

选中一个请求-》右键-》Map Remote(下图) 弹出（下图2）

![img](http://wd.geilicdn.com/6924af6c2d76434da988fa87affe9091.png)

![img](http://wd.geilicdn.com/18442d24d541f6ed726390c7a158858f.png)

如果请求的参数有随机数，一定要将参数设置为通配符（**），否者下次请求的时候讲无法配对，导致映射失败。

#### 查看远程映射记录

电脑菜单栏tools-》Map Remote

![img](http://wd.geilicdn.com/e7c746b7706f4562b93e03af1ce44466.png)

 弹出下图

![img](http://wd.geilicdn.com/a1fcbe29b318a336e375d1aaebf7b532.png)

#### 远程映射非常有用

其作用是可以将一个地址代理成其他地址，开发和测试的通过这种方式使用线上app来进行调试和开发，无需繁琐的后台配置。

或者通过这种方式修改api数据，调试线上js bug 等等。

### 断点

#### 重要作用

修改请求或者返回的header信息，包括cookie，修改请求的参数，修改返回的内容

#### 设置

右键点击请求，选择BreakPoints，刷新页面后碰到这个请求后断点生效。（如下图）

![img](http://wd.geilicdn.com/7b32fed2da0e1d7ea98147723f49e836.png)

此时会在request和response进行两次打断，

如果只需要打断一次可以对面板进行设置

点击电脑菜单栏Proxy-》Breakpoints Settings （如下图）

![img](http://wd.geilicdn.com/8a25a083a37f01d1d5aad8072e9b4730.png)

弹出下图

![img](http://wd.geilicdn.com/8a616e0a06d8d8d4c8e15d6d3c64473f.png)

双击列表数据进入编辑模式（如下图）

![img](http://wd.geilicdn.com/e3a32017eec58f3fa3c1dbf9b5881c72.png)

如果只选择了request，那么只会在发送请求的时候打断

如果只选择了response， 那么只会在返回的时候打断

如果都选，打断两次

#### 使用示例，request修改cookie

![img](http://wd.geilicdn.com/8bc7865f869f2a5395692b01fddde9f4.png)

#### https抓包

 step1：打开charles，选择菜单“Help” => “SSL Proxying” => “Install Charles Root Certificate”，安装根证书（如果是在手机上，请选择 Install Charles Root Certificate on a Mobile Device or Remote Browser…，在手机上安装根证书)

![img](http://wd.geilicdn.com/9c0cf311cdb5763706498f448f59854a.png)

 step2：打开钥匙串访问，找到 “Charles Proxy Custom Root Certificate证书”，系统默认提示“此证书已标记为不受此账户信任”

![img](http://wd.geilicdn.com/81aa4272d837b2b5089093ee37107feb.png)

 step3：选择“Charles Proxy Custom Root Certificate证书”，点击右键 =>显示简介 => 点击“信任”，设置信任该证书；

![img](http://wd.geilicdn.com/66198466e8ade7ef662f74191c3b6d17.png)

 step4：在charles菜单中选择"Proxy" => "SSL Proxying"，勾选“Enable SSL Proxying”，添加白名单域名列表

![img](http://wd.geilicdn.com/624f14bf20f84527c77ca7dbc164bb9a.png)

#### 其它功能

网速限制，本地映射，需要大家去摸索。

end