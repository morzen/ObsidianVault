https://multiportmedia.com/setting-a-static-ip-address-in-kali-linux/

command:
vim /etc/network/interfaces

content of file:


```
#The primary network interface
allow-hotplug  eth0
#iface eth0 inet eth0
Inface eth0 inet static
	address [your IP]
	netmask [your netmask]
        broadcast [use 192.255.255.255 for a 192 address]
        Gateway [your gateway]
```
			
			
command:
		ifdown eth0 
		ifup eth0 
		ip a