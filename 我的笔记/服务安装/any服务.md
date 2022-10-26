# any服务
1、github的地址: git@github.com:aplot249/anylink.git

2、开启bbr和ipv4地址转发：

`echo net.core.default_qdisc=fq >> /etc/sysctl.conf` 

`echo net.ipv4.tcp_congestion_control=bbr >> /etc/sysctl.conf`

`echo net.ipv4.ip_forward = 1` `>> /etc/sysctl.conf`

3、设置nat路由转发：

`iptables -t nat -A POSTROUTING -s 192.168.10.0/24 -o eth0 -j MASQUERADE`

`# 查看设置是否生效`

`iptables -nL -t nat`