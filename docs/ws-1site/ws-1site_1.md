# （一）：Wireshark 基本用法

> 原文出处：[EMC 中文支持论坛](https://community.emc.com/thread/194901)

按照国际惯例，从最基本的说起。

**抓取报文****:**

下载和安装好 Wireshark 之后，启动 Wireshark 并且在接口列表中选择接口名，然后开始在此接口上抓包。例如，如果想要在无线网络上抓取流量，点击无线接口。点击 Capture Options 可以配置高级属性，但现在无此必要。

点击接口名称之后，就可以看到实时接收的报文。Wireshark 会捕捉系统发送和接收的每一个报文。如果抓取的接口是无线并且选项选取的是混合模式，那么也会看到网络上其他报文。

上端面板每一行对应一个网络报文，默认显示报文接收时间（相对开始抓取的时间点），源和目标 IP 地址，使用协议和报文相关信息。点击某一行可以在下面两个窗口看到更多信息。“+”图标显示报文里面每一层的详细信息。底端窗口同时以十六进制和 ASCII 码的方式列出报文内容。

需要停止抓取报文的时候，点击左上角的停止按键。

**色彩标识****:**

进行到这里已经看到报文以绿色，蓝色，黑色显示出来。Wireshark 通过颜色让各种流量的报文一目了然。比如默认绿色是 TCP 报文，深蓝色是 DNS，浅蓝是 UDP，黑色标识出有问题的 TCP 报文——比如乱序报文。

**报文样本****:**

比如说你在家安装了 Wireshark，但家用 LAN 环境下没有感兴趣的报文可供观察，那么可以去 Wireshark wiki 下载[报文样本文件](http://wiki.wireshark.org/SampleCaptures)。

打开一个抓取文件相当简单，在主界面上点击 Open 并浏览文件即可。也可以在 Wireshark 里保存自己的抓包文件并稍后打开。

**过滤报文****:**

如果正在尝试分析问题，比如打电话的时候某一程序发送的报文，可以关闭所有其他使用网络的应用来减少流量。但还是可能有大批报文需要筛选，这时要用到 Wireshark 过滤器。

最基本的方式就是在窗口顶端过滤栏输入并点击 Apply（或按下回车）。例如，输入“dns”就会只看到 DNS 报文。输入的时候，Wireshark 会帮助自动完成过滤条件。

也可以点击 Analyze 菜单并选择 Display Filters 来创建新的过滤条件。

另一件很有趣的事情是你可以右键报文并选择 Follow TCP Stream。

你会看到在服务器和目标端之间的全部会话。

关闭窗口之后，你会发现过滤条件自动被引用了——Wireshark 显示构成会话的报文。

**检查报文****:**

选中一个报文之后，就可以深入挖掘它的内容了。

也可以在这里创建过滤条件——只需右键细节并使用 Apply as Filter 子菜单，就可以根据此细节创建过滤条件。

Wireshark 是一个非常之强大的工具，第一节只介绍它的最基本用法。网络专家用它来 debug 网络协议实现细节，检查安全问题，网络协议内部构件等等。