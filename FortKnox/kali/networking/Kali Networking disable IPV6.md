### Disable IPv6 protocol via Sysctl 

To temporarily disable IPv6, you only need to execute the following 3 commands in the Terminal:

> sysctl -w net.ipv6.conf.all.disable\_ipv6=1  
> sysctl -w net.ipv6.conf.default.disable\_ipv6=1  
> sysctl -w net.ipv6.conf.lo.disable\_ipv6=1

![](https://cdn-0.securityonline.info/wp-content/uploads/2019/06/Annotation-2019-06-05-105455.png)

The above command only **temporarily disables** the IPv6 protocol in the Kali Linux system. After the restart, the system will automatically enable IPv6 again.

To permanently disable IPv6 on your Kali Linux system, you can modify the /etc/sysctl.conf file with your editor. Add the following 3 lines to the /etc/sysctl.conf configuration file:

> _net.ipv6.conf.all.disable\_ipv6=1_  
> _net.ipv6.conf.default.disable\_ipv6=1_  
> _net.ipv6.conf.lo.disable\_ipv6=1_

To make the settings take effect, run command below

> _sysctl -p_



### Disable IPv6 Protocol via GRUB

1.  Edit the _/etc/default/grub_ configuration file
2.  Modify _GRUB\_CMDLINE\_LINUX\_DEFAULT_ and _GRUB\_CMDLINE\_LINUX_ to disable IPv6 at startup  
    [![](https://cdn-0.securityonline.info/wp-content/uploads/2019/06/Annotation-2019-06-05-104213.png)](https://cdn-0.securityonline.info/wp-content/uploads/2019/06/Annotation-2019-06-05-104213.png)_GRUB\_CMDLINE\_LINUX\_DEFAULT=”quiet splash ipv6.disable=1″_  
    _GRUB\_CMDLINE\_LINUX=”ipv6.disable=1″_
3.  To make the settings take effect, run command below  
    _update-grub_