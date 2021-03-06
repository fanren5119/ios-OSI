## 1.TCP/IP协议
        OSI模型所分的七层，在实际应用中，往往有一些层被整合，或者功能分散到其他层去，
    TCP/IP没有照搬OSI模型，也没有一个公认的TCP/IP层级模型，一般划分为三层到五层模型
    来描述TCP/IP协议。
        TCP/IP的设计，是吸取了分层模型的精华思想--封装。每层对上一层服务的时候，上一
    层的数据结构管是黑盒，直接作为本层的数据，而不需要关心上一层协议的任何细节；
![TCP/IP协议](Image/tcpip.png)
## 2.TCP/IP协议四层模型
        ① 网络接口层：
            网络接口层包括用于协作IP数据在已有网络介质上传输的协议；
            它定义像地址解析协议（Address Resolution Protocol，ARP）这样的协议，
        供TCP/IP协议的数据结构和实际物理硬件之间的接口。
            ps：该层确定了网络数据包的形式。
        ② 网间层：
            网间层对应于OSI七层参考模型的网络层，本层包含IP协议、RIP协议（Routing 
        Information Protocol，路由信息协议），负责数据的包装、寻址和路由。同时还
        包含网络控制报文协议（ICMP）用来供网络诊断信息；
            ps：该层确定计算机的位置。
        ③ 传输层：
            传输层对应于OSI七层参考模型的传输层，他供两种端到端的通信服务。其中
        TCP协议供可靠的数据运输服务，UDP协议供不可靠的用户数据报服务；
            ps：TCP三次握手、四次挥手；
                UDP：只发不管别人收不收得到；
        ④ 应用层：
            应用层对应于OSI七层模型的应用层和表达层；
## 3.TCP/IP协议族常用协议
        ① 应用层：TFTP，HTTP，SNMP，FTP，SMTP，DNS，Telnet等；
        ② 传输层：TCP， UDP；
        ③ 网络层：IP，ICMP，OSPF，ELGRP，IGMP
        ④ 数据链路层：SLIP，CSLIP，PPP，MTU；
## 4.重要TCP/IP协议族协议介绍
        ① IP（网络协议）：是网间层的主要协议，任务是在源地址和目的地地址之间传输
    数据。IP协议只是尽最大努力来传输数据包，并不保证所有的包都可以传输到目的地，
    也不保证数据包的顺序和唯一性。
        ps：IP定义了TCP/IP的地址，寻址方法，以及路由规则。
        ② ICMP（网络控制消息协议）：是TCP/IP的核心协议之一，用于在IP网络中发送控
    制消息，供通信过程中的各种问题反馈。ICMP直接使用IP数据包传输，但ICMP并不是IP
    协议的子协议。常见的联网状态诊断工具都依赖于ICMP协议；
        ③ TCP（传输控制协议）：是一种面向连接的，可靠地，基于字节流传输的通信协议，
    TCP具有端口号的概念，用来标识同一个地址上的不同应用。
        ④ UDP（用户数据包协议）是一个面向数据报的传输层协议。UDP的传输是不可靠的
    ，发送者不会知道目标地址的数据通路是否发生阻塞，也不知道数据是否到达，是否完整
    以及是否还是原来的次序。他同TCP一样用来标识本地应用的端口号，所以使用的UDP的
    应用，都能容忍一定量数据的错误和丢包，但是对传输性能敏感的，比如流媒体、DNS等；
        ⑤ FTP（文件传输协议）：用来进行文件传输的标准协议。FTP基于TCP使用端口号20
    来传输数据，21来传输控制信息；
        ⑥ HTTP（超文本传输协议）：是现在广为流行的WEB网络的基础，HTTPS是HTTP的加密
    安全版本，协议通过TCP传输，HTTP默认使用端口80，HTTPS使用443；
