# 端口扫描

## 端口扫描

这一章将会演示如何通过 Python 的网络连接来开发一个基础的端口扫描器,我们的设计思路是使用 socket 一遍又一遍的去连接 ip 与端口的组合的新值,为了方面我们能够快速的完成它，首先需要介绍一点新的概念,for 循环:

```py
>>>
>>> for port in range(1000,1024):
...   print "[+] The port is: "+str(port)
...
[+] The port is: 1000
[+] The port is: 1001
[+] The port is: 1002
[+] The port is: 1003
[+] The port is: 1004
[+] The port is: 1005
[+] The port is: 1006
[+] The port is: 1007
[+] The port is: 1008
[+] The port is: 1009
[+] The port is: 1010
[+] The port is: 1011
[+] The port is: 1012
[+] The port is: 1013
[+] The port is: 1014
[+] The port is: 1015
[+] The port is: 1016
[+] The port is: 1017
[+] The port is: 1018
[+] The port is: 1019
[+] The port is: 1020
[+] The port is: 1021
[+] The port is: 1022
[+] The port is: 1023 
```

注意上面那段代码在循环体内的缩进，通常情况下是空两格或一个 tab 键，但这都没有关系，只要你的整个代码一直就可以了。我么所写的那个简短的端口扫描器的核心代码会写在上面代码中的输出块部分，然后建立一个 socket 连接。下面的代码就演示了如何使用内建的 socket 模块去建立一个 socket 连接：

```py
>>>
>>> import socket
>>>
>>> s = socket.socket()
>>> s.connect(('127.0.0.1s', 22))
>>> s.send('Primal Security \n')
17
>>> banner = s.recv(1024)
>>> print banner
OpenSSH 
```

上面这个例子：我们先 import 这 socket 模块并且调用 connect()函数去连接指定的 IP 地址与端口。它就会建立一个 TCP 连接(SYN/SYN-ACK/ACK)并且我们再通过 send()函数给服务器发送一个真实的数据，然后使用 recv()打印出响应的内容。现在教大家如何容错 socket，对于不能打开的连接:

```py
>>>
>>> s.connect(('127.0.0.1', 23))
Traceback (most recent call last):
  File "<stdin>", line 1, in ?
  File "<string>", line 1, in connect
socket.error: (111, 'Connection refused') 
```

对于上面的错误有若干中处理方式，这里我们使用最简单的一种方式：使用"try/except"循环来处理错误:

```py
>>>
>>> try:
...   s.connect(('127.0.0.1', 23))
... except: pass
...
>>> 
```

现在就不会出现错误了，一行很简单的代码就让你的程序能够继续工作下去^_^。现在让我们使用之前学到的知识，使用 for 循环来写一个简单的端口扫描器:

```py
>>>
>>> for port in range(20,25):
...   try:
...    print "[+] Attempting to connect to 127.0.0.1:"+str(port)
...     s.connect(('127.0.0.1', port))
...     s.send('Primal Security \n')    
...     banner = s.recv(1024)
...     if banner:
...       print "[+] Port "+str(port)+" open: "+banner
...     s.close()
...   except: pass
...
17
[+] Attempting to connect to 127.0.0.1:20
[+] Attempting to connect to 127.0.0.1:21
[+] Attempting to connect to 127.0.0.1:22
[+] Port 22 open: OpenSSH
[+] Attempting to connect to 127.0.0.1:23
[+] Attempting to connect to 127.0.0.1:24
[+] Attempting to connect to 127.0.0.1:25 
```

上面我们演示了使用"try/except"循环来处理当 socket 连接的时候遇到端口关闭的错误，同时上面还演示了如何使用"if"语句打印出可以连接成功的端口。下面我们将创建一个我们扫描指定端口的扫描器，这里的端口号，我们使用数组来存储，然后遍历这一个数组:

```py
>>>
>>> ports = [22, 445, 80, 443, 3389]
>>> for port in ports:
...   print port
...
22
445
80
443
3389
>>> 
```

如果我们想一次性扫描多台主机，可以使用一个 for 循环嵌套。最外层的是主机的 ip，然后里面的 for 循环是端口。下面有一个基础的例子，展示了如何通过循环嵌套来构建一个简单的扫描器:

```py
>>>
>>> hosts = ['127.0.0.1', '192.168.1.5', '10.0.0.1']
>>>
>>> ports = [22, 445, 80, 443, 3389]
>>>
>>> for host in hosts:
...   for port in ports:
...     try:
...        print "[+] Connecting to "+host+":"+str(port)
...        s.connect((host, port))
...        s.send('Primal Security \n')
...        banner = s.recv(1024)
...        if banner:
...          print "[+] Port "+str(port)+" open: "+banner
...        s.close()
...     except:pass
...
[+] Connecting to 127.0.0.1:22
[+] Port 22 open: OpenSSH
[+] Connecting to 127.0.0.1:445
[+] Connecting to 127.0.0.1:80
[+] Connecting to 127.0.0.1:443
[+] Connecting to 127.0.0.1:3389
[+] Connecting to 192.168.1.5:22
[+] Connecting to 192.168.1.5:445
[+] Connecting to 192.168.1.5:80
[+] Connecting to 192.168.1.5:443
[+] Connecting to 192.168.1.5:3389
[+] Connecting to 10.0.0.1:22
[+] Connecting to 10.0.0.1:445
[+] Connecting to 10.0.0.1:80
[+] Connecting to 10.0.0.1:443
[+] Connecting to 10.0.0.1:3389 
```

正如你所看到的结果，它把 hosts 数组里面的所有值都遍历了一次 ports 数组，等 hosts[0]扫描完成之后再扫描 hosts[1]依次类推。在这个例子里面你也可以修改里面的代码，只让它显示出可以打开的端口。

在这最后，你会发现还是 Nmap 最好用，但是我们将在后面的文章里面继续完善这个实例，大家可以花点时间去学习一些 socket 模块其他的功能函数，大家可以使用"dir(socket)"来了解更多，当然还有'help()'.