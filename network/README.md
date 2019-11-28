# 网络的传输协议

我们常见的网络协议可分为： `七层网络协议`，`TCP / IP协议`

#### 七层网络协议（大概了解）
应用层：FTP，WWW，Telnet，NFS，SMTP，Gateway，SNMP<BR>
表示层：TIFF，GIF，JPEG，PICT，ASCII，EBCDIC，encryption，MPEG，MIDI，HTML<BR>
会话层：RPC，SQL，NFS，NetBIOS，names，AppleTalk，ASP，DECnet，SCP<BR>
传输层：TCP，UDP，SPX<BR>
网络层：IP，IPX，AppleTalk DDP<BR>
数据链路层：Frame Relay，HDLC，PPP，IEEE802.3 / 802.2，FDDI，ATM，IEEE802.5 / 802.2<BR>
物理层：EIA / TIA - 232，EIA / TIA - 499，V.35，V.24，RJ45，Ethernet，802.3，802.5，FDDI，NRZI，NRZ，B8ZS


#### TCP / IP 协议（重点）

>什么是 `TCP/IP协议`?<br>
`TCP/IP协议` 不是一个协议，它是一个统称；它包含了 `IP协议`，`TCP协议`，`Http协议`，`Ftp协议`等等。

>网络协议本来就是一个大的体系，我们要弄清楚它不是一件容易的事情，这里我们主要来了解一下 `一个主机的数据是怎么安全到达到对方的主机上的`。

<br>
<br>

`TCP/IP协议` 分四层，每一层都要求它下面的一层来满足它的需求。<br>


应用层：Telnet，FTP，SMTP，SNMP<br>
传输层：TCP，UDP，UGP<br>
网络层： IP，ICMP，IGMP<br>
数据链路层：ARP，RARP


#### 各个层的功能
物理层：实现计算机系统与网络间的物理连接<br>
数据链路层：进行数据打包与解包，形成信息帧<br>
网络层：提供数据通过的路由<br>
传输层：提供传输顺序信息与响应<Br>
会话层：建立和中止连接<br>
表示层：数据转换、确认数据格式<br>
应用层：提供用户程序接口