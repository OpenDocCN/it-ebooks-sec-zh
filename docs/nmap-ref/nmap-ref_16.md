# 十六、 实例

## 十六、 实例

下面给出一些实例，简单的、复杂的到深奥的。为更具体，一 些例子使用了实际的 IP 地址和 域名。在这些位置，可以使用你自己网络 的地址/域名替换。注意，扫描其它网络不一定合法 一些网络管理员不愿看到 未申请过的扫描，会产生报怨。因此，先获得允许是最好的办法。

如果是为了测试，scanme.nmap.org 允许被扫描。但仅允许使用 Nmap 扫描并禁止测试漏洞或进 行 DoS 攻击。为 保证带宽，对该主机的扫描每天不要超过 12 次。如果这个免费扫描服务被 滥 用 系统将崩溃而且 Nmap 将报告解析 指定的主机名/IP 地址失败 scanme.nmap.org 这些免 费 扫描要求也适用于 scanme2.nmap.org、 scanme3.nmap.org 等等，虽然这些 主机目前还不存在

```
nmap -v scanme.nmap.org 
```

这个选项扫描主机 scanme.nmap.org 中 所有的保留 TCP 端口。选项-v 启用细节模式。

```
nmap -sS -O scanme.nmap.org/24 
```

进行秘密 SYN 扫描，对象为主机 Saznme 所在的“C 类”网段 的 255 台主机。同时尝试确定每台 工作主机的操作系统类型。因为进行 SYN 扫描 和操作系统检测，这个扫描需要有根权限。

```
nmap -sV -p 22，53，110，143，4564 198.116.0-255.1-127 
```

进行主机列举和 TCP 扫描，对象为 B 类 188.116 网段中 255 个 8 位子网。这 个测试用于确定系 统是否运行了 sshd、DNS、imapd 或 4564 端口。如果这些端口 打开，将使用版本检测来确定哪 种应用在运行。

```
nmap -v -iR 100000 -P0 -p 80 
```

随机选择 100000 台主机扫描是否运行 Web 服务器(80 端口)。由起始阶段 发送探测报文来确定 主机是否工作非常浪费时间，而且只需探测主机的一个端口，因 此使用-P0 禁止对主机列表。

```
nmap -P0 -p80 -oX logs/pb-port80scan.xml -oG logs/pb-port80scan.gnmap 216.163.128.20/20 
```

扫描 4096 个 IP 地址，查找 Web 服务器(不 ping)，将结果以 Grep 和 XML 格式保存。

```
host -l company.com | cut -d -f 4 | nmap -v -iL - 
```

进行 DNS 区域传输，以发现 company.com 中的主机，然后将 IP 地址提供给 Nmap。上述命令用 于 GNU/Linux -- 其它系统进行区域传输时有不同的命令。