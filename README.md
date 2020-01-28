# GNB
GNB是一个具有NAT穿透能力通过P2P进行三层网络交换的VPN， GNB可以让用户把异地的办公环境以及家庭环境组成一个虚拟的局域网，这个虚拟的局域网中的机器不需要公网服务器中转就可以实现TCP/IP通讯。

与大多数内网穿透的软件实现应用层协议代理不同，GNB是通过虚拟网卡实现IP分组转发，支持应用层所有基于TCP/IP的通信协议。

GNB的的安全基于ED25519交换密钥，IP分组的加密有XOR与RC4两个加密算法可选，也可以选择不加密；IP分组加密密钥会根据时钟每隔一段时间会更新一次，因此必须要确保节点中的机器时间必须同步。

![net to net](images/net_to_net.jpeg)

GNB用C语言开发，编译时不需要引用第三方库文件，可以方便移植到当前流行的操作系统上。

现有支持平台：
树莓派
Linux_X86_64
Windows10_X86_64
macOS
FreeBSD_AMD64
OpenBSD_AMD64
Windows7_X86_64
OpenWRT
