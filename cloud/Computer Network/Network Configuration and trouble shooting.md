>date : 2025-12-28

1. ping 
    - Used to ensure that computer can communicate to the specific device over the network
   - sends ICMP [internet control message protocol] requests to the destinated computer in the form of packets and waits for response 
   - example : ping google.com
   -  ![[Screenshot-from-2017-05-26-23-30-29-1.png]] Ping commands
2. nslookup
   - queries DNS in order to fetch IP address or domain name from DNS records
   - ![[Screenshot-from-2017-05-26-23-31-57.png]]nslookup
3. traceroute 
   - used to get route of a packet
   - determine the path that packets uses
   - returns number of hops taken by the packet
   - tracert  {domain name} ![[64.webp]] traceroute
4. host
   - used to find a domain name associated with the IP address
   - find an IP address associated with the domain name
   - The returned IP address is either IPv4 or IPv6.![[Screenshot-from-2017-05-26-23-34-28.png]]
   - ![[Screenshot-from-2017-05-26-23-35-17.png]] 
5. netstat 
   - stands for network statistics
   -  used to display routing tables, connection information, the status of ports, etc. 
   - This command works with Linux Network Subsystem. 
   - This command basically displays the content of /proc/net file defined in the Linux file system.
   - ![[Screenshot-from-2017-05-26-23-37-19.png]] 
6. ARP
   - Address Resolution Protocol
   - used to display and modify ARP cache, which contains the mapping of IP address to MAC address
   - The system's TCP/IP stack uses ARP in order to determine the MAC address associated with an IP address.![[Screenshot-from-2017-05-26-23-38-28.png]]
 
7. ifconfig
   - utility in an operating system that is used to set or display the IP address and netmask of a network interface.
   - It also provides commands to enable or disable an interface. 
   - Many UNIX-like operating systems initialize their network interfaces using ifconfig at boot time. 
   - ifconfig is also used to view the MTU(Maximum transmission unit).
   - modern "***ip addr show***"
   >````sonu@LAPTOP-37P70OOC:~$ ifconfig
	eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 172.20.1.156  netmask 255.255.240.0  broadcast 172.20.15.255
        inet6 fe80::215:5dff:feac:d83d  prefixlen 64  scopeid 0x20<link>
        ether 00:15:5d:ac:d8:3d  txqueuelen 1000  (Ethernet)
        RX packets 66  bytes 62151 (62.1 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 86  bytes 8170 (8.1 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
	lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 42  bytes 12716 (12.7 KB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 42  bytes 12716 (12.7 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
   >```
8. dig
   - domain information groper
   - it is a tool used to find query information related to domain name and troubleshoot DNS issue in Linux.
   - This tool can provide various types of DNS records, such as CNAME, MX records and records etc.
   - ![[90-1.webp]]
9. route
   - helps us display and manipulate the routing table in Linux. 
   - Information contained by this is about how network packets should be routed through a network.
   - This command shows destination, mask, flags, metric, gateway, reference count, and interface.
   - We can also add or delete routes from a network with IP address.

	- ****For example:**** If we have "IP address: 192.168.90.0" and "Subnet mask = 24" and "gateway (gw) = 10.0.0.1"
	route add -net 192.168.90.0/24 gw 10.0.0.1
   - ![[91.webp]]
10. ethtool
    - The Ethtool is used to view and modify the settings of a network interface card (NIC) in Linux. 
    - It has replaced the old tool named mii-tool. 
    - This command can be used to view the current speed and duplex setting of the NIC. 
    - To view the settings for the NIC named "enp0s3" use the following command.
    - Syntax : enthool enp0s3
    - ![[92-1.webp]]
11. hostname
    - used to display the current hostname of the system.
    - to change the hostname
	     sudo hostnamectl set-hostname sonu
    - to see hostname , type "hostname"


#commands #networkCommands
