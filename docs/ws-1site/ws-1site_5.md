# （五）：TCP 窗口与拥塞处理

TCP 通过滑动窗口机制检测丢包，并在丢包发生时调整数据传输速率。滑动窗口机制利用数据接收端的接收窗口来控制数据流。

接收窗口值由数据接收端指定，以字节数形式存储于 TCP 报文头，并告知传输设备有多少数据将会存储在 TCP 缓冲区。缓冲区就是数据暂时放置的地方，直至传递至应用层协议等待处理。因此，发送端每次只能发送 Window Size 字段指定的数据量。为了使发送端继续传送数据，接收端必须发送确认信息：之前的数据接收到了。同时必须对占用缓冲区的数据进行处理以释放缓存空间。下图显示了接收窗口是如何工作的：

上图中，客户端向服务器发送数据，服务器接收窗口是 5000 字节。客户端发送了 2500 字节，服务器缓冲区还剩 2500 字节，之后又发送了 2000 字节，从而缓冲区只剩 500 字节。服务器发送确认信息。对缓存中数据进行处理并清空缓存。此过程重复进行，客户端又发送 3000 字节和 1000 字节，服务器缓存减少至 1000 字节，客户端再次确认数据并处理缓存中内容。

# 更多信息

**调整窗口大小：**

当 TCP 堆 栈接收到数据的时候，生成一个确认信息并以回复的方式发送，但是放置在接收端缓存中的数据并不总是立即被处理。当服务器忙于处理从多个客户端接收的报文， 服务器很有可能因为清理缓存而变得缓慢，无法腾出空间接收新的数据，如果没有流控，则可能会造成丢包和数据损坏。好在，接收窗口所设定的速率无法使服务器 正常处理数据时，能够调整接收窗口大小。通过减小返回给发送端的 ACK 报文的 TCP 头窗口大小值来实现。如下图所示：

上图中，服务器初始窗口大小为 5000 字节。客户端发送 2000 字节，之后又发送了 2000 字节，缓冲区中只有 1000 字节可用。服务器意识到缓冲区正在快速填满，它知道如果数据继续以此速率传输，很快会有报文丢失。为了防止报文丢失，服务器发送确认信息给客户端，更新窗口大小为 1000 字节。结果，客户端减少数据发送，服务器以可以接受的速率处理缓存内容，即保持数据流以稳定的速率传输。

调整窗口大小在两个方向都是可行的。当服务器能够更加快速的处理报文时，它会发送一个较大窗口的 ACK 报文。

**零窗口暂停数据流：**

某些情况下，服务器无法再处理从客户端发送的数据。可能是由于内存不足，处理能力不够，或其他原因。这可能会造成数据被丢弃以及传输暂停，但接收窗口能够帮助减小负面影响。

当上述情况发生时，服务器会发送窗口为 0 的报文。当客户端接收到此报文时，它会暂停所有数据传输，但会保持与服务器的连接以传输探测（keep-alive）报文。探测报文在客户端以稳定间隙发送，以查看服务器接收窗口状态。一旦服务器能够再次处理数据，将会返回非零值窗口大小，传输会恢复。下图示例了零窗口通知过程。

服务器初始接收数据窗口为 5000 字节大小。从客户端接收 4000 字节数据之后，服务器负载变得非常繁重，无法继续处理客户端任何数据。服务器于是发送窗口大小值为 0 的报文。客户端暂停数据传输并发送一个探测报文。探测报文之后，服务器回复以告知客户端现在可以接收数据的报文，以及窗口大小为 1000 字节。客户端恢复传送数据。

**TCP 滑动窗口实战：**

本例中，开始从 192.168.0.20 发送至 192.168.0.30。我们关心的是窗口大小字段，可以从 Packet List 面板的 Info 栏以及 Packet Details 的 TCP 报文头看到。前三个报文后，可看到该值立刻减小，如下图所示：

窗口大小值从第一个报文的 8760 字节变成第二个报文的 5840 字节到第三个报文的 2920 字节①。窗口大小值的减小是主机延时的典型标志。在时间栏注意到这一过程发生的非常迅速②。当窗口大小迅速减小的时候，通常就有可能下降为零。这就是第四个报文所发生的，如下图所示：

第四个报文从 192.168.0.20 发送至 192.168.0.30，目的是告诉 192.168.0.30 它不再接收任何数据。0 值见于 TCP 报文头①，Wireshark 的 Packet List 面板 Info 栏，以及 TCP 报文头的 SEQ/ACK Analysis 字段②也告诉我们这是一个 0 窗口报文。

一旦发送了零窗口报文，192.168.0.30 的设备不会再发送任何数据，直到收到从 192.168.0.20 的窗口更新，告知窗口大小已经增加了。本例中导致零窗口的问题是暂时的，所以在下一个报文中发送了窗口更新信息，如下图所示。

本例中，窗口大小增加到一个非常健康的数值 64，240 字节①。Wireshark 再次在 SEQ/ACK Analysis 告诉我们这是一个窗口更新。

一旦收到更新报文，192.168.0.30 的主机就再次开始发送数据，在报文 6 和报文 7 中。这一过程发生很快。如果它持续时间再长一点，就可能会导致网络的潜在中断，引起数据传输减慢或失败。

下一个关于滑动窗口的例子，第一个报文是正常 HTTP，从 195.81.202.68 至 172.31.136.85。此报文之后立刻跟随一个从 172.31.136.85 发送的零窗口报文，如下图所示：

这与上一个例子中的零窗口报文十分类似，但结果显著不同，172.31.136.85 主机不是发送一个窗口更新并回复通讯，而是一个探测报文，如下图所示：

此报文被 Wireshark 标注为探测报文①。时间栏告诉我们这一报文发生于最后一个接收到的报文 3.4 秒之后。这一过程持续若干次，一端发送零窗口报文另一端发送探测报文，如下图所示：

探测报文发送间隙为 3.4，6.8，13.5 秒。这一过程可能会持续相当长一段时间，取决于通讯设备的操作系统。该情况下，把时间栏的值加起来，通讯暂停了 25 秒。

**TCP 差错控制和流控排查总结：**

**重传报文**

重 传的发生是由于客户端检测到服务器没有接收到它所发送的数据。因此，取决于你所分析的是通讯的哪一端，有可能是看不见重传的。如果从服务器端抓取数据，并 且它确实没有接收到客户端所发送的和重传报文，可能会一无所获因为无法看见重传报文。如果怀疑并不是服务器端导致的报文丢失，可以考虑在客户端尝试抓取报 文，以查看实际是否有重传发生。

**重复****ACK**

可以将重复 ACK 看作重传的“所谓相反面”，因为它是在服务器检测到客户端发送报文丢失的时候产生的。大多数情况下，在通讯两端抓取流量时都可以看到重复 ACK。需记住当接收报文乱序时会触发重复 ACK。例如，如果服务器之接收到发送的第一个和第三个报文，就会导致发送重复 ACK 引起客户端对第二个报文的快速重传，因为你已经收到了第一个和第三个报文，因此不管导致第二个报文丢弃的原因是什么，都很有可能是暂时的，因此大多数情况下重复 ACK 都会成功发送和接收。当然，这种情形并不一定永远会发生，因此当你怀疑在服务器端丢失报文而又看不到任何重复 ACK，考虑从通讯的客户端抓取报文。

**零窗口和探测报文**

滑动窗口直接与服务器无法接收和处理报文有关，任何窗口大小的缩小以及零值都是服务器问题的直接结果。所以如果你在哪里看到这两者之一发生，就应该在那里深入研究。通常应当在网络通讯两端一直主机窗口更新报文。