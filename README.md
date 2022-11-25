# wireguard_natrouting

Add the following to wg0.conf:

PostUp = /etc/wireguard/add-nat-routing.sh

PostDown = /etc/wireguard/remove-nat-routing.sh



# ifconfig example

ens3: flags=4163<UP,BROADCAST,RUNNING,MULTICAST> mtu 9000 inet 10.0.0.100 netmask 255.255.255.0 broadcast 10.0.0.255 inet6 fe80::17ff:fe09:d2b2 prefixlen 64 scopeid 0x20<link> ether 02:00:17:09:d2:b2 txqueuelen 1000 (Ethernet) RX packets 4511152 bytes 4611316955 (4.6 GB) RX errors 0 dropped 0 overruns 0 frame 0 TX packets 5683904 bytes 4973265514 (4.9 GB) TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING> mtu 65536 inet 127.0.0.1 netmask 255.0.0.0 inet6 ::1 prefixlen 128 scopeid 0x10<host> loop txqueuelen 1000 (Local Loopback) RX packets 19788 bytes 3017642 (3.0 MB) RX errors 0 dropped 0 overruns 0 frame 0 TX packets 19788 bytes 3017642 (3.0 MB) TX errors 0 dropped 0 overruns 0 carrier 0 collisions 0

wg0: flags=209<UP,POINTOPOINT,RUNNING,NOARP> mtu 8920 inet 10.66.66.1 netmask 255.255.255.0 destination 10.66.66.1 inet6 fd42:42:42::1 prefixlen 64 scopeid 0x0<global> unspec 00-00-00-00-00-00-00-00-00-00-00-00-00-00-00-00 txqueuelen 1000 (UNSPEC) RX packets 1838804 bytes 436157622 (436.1 MB) RX errors 159 dropped 0 overruns 0 frame 159 TX packets 3674792 bytes 4176837380 (4.1 GB) TX errors 0 dropped 1763 overruns 0 carrier 0 collisions 0
