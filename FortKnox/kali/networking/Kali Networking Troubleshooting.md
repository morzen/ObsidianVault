[Stage 1]- Check **IP address** _(ifconfig)_  
(https://forums.kali.org/showthread.php?20846-Troubleshooting-Internet-Network-Access&p=32766&viewfull=1#post32766). 

[Stage 2] - Check **gateway** _(route -n)_ 
(https://forums.kali.org/showthread.php?20846-Troubleshooting-Internet-Network-Access&p=32787&viewfull=1#post32787). 

[Stage 3] - Check **DNS** _(cat /etc/resolv.conf)_  
(https://forums.kali.org/showthread.php?20846-Troubleshooting-Internet-Network-Access&p=32788&viewfull=1#post32788).

[Stage 4]- Check **network connectivity** _(ping google.com -c 4; traceroute google.com; curl ifconfig.me)_
(https://forums.kali.org/showthread.php?20846-Troubleshooting-Internet-Network-Access&p=32789&viewfull=1#post32789).  

_[Stage 5]-_ _\*Optional\*_ _Check **proxy settings** _(echo $http\_proxy)__  
(https://forums.kali.org/showthread.php?20846-Troubleshooting-Internet-Network-Access&p=32793&viewfull=1#post32793). 

_[Stage 6] - \*Optional\* Check **virtual machine network adapter** _(NAT? Bridged?)__
(https://forums.kali.org/showthread.php?20846-Troubleshooting-Internet-Network-Access&p=32794&viewfull=1#post32794).

Code:

ifconfig; route -n; cat /etc/resolv.conf; ping google.com -c 4; traceroute google.com; curl ifconfig.me; echo $http\_proxy

recap:
	ifconfig
	route -n
	cat /etc/resolv.conf