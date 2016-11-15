sudo yum update
sudo yum install nano ntp nscd bind-utils
sudo systemctl start ntpd
sudo systemctl enable ntpd
sudo systemctl start nscd
sudo systemctl enable nscd

sudo sysctl vm.swappiness=1
echo "vm.swappiness=1" | sudo tee -a /etc/sysctl.conf

Add noatime to /etc/fstab:
UUID=ef6ba050-6cdc-416a-9380-c14304d0d206 /                       xfs     defaults,noatime        0 0

sudo mount -o remount /

--------------------------

NTP Service:
● ntpd.service - Network Time Service
   Loaded: loaded (/usr/lib/systemd/system/ntpd.service; enabled; vendor preset: disabled)
   Active: active (running) since Tue 2016-11-15 06:08:24 UTC; 22min ago
 Main PID: 29960 (ntpd)
   CGroup: /system.slice/ntpd.service
           └─29960 /usr/sbin/ntpd -u ntp:ntp -g

Nov 15 06:08:24 ip-172-31-59-253 ntpd[29960]: Listen normally on 3 eth0 172.31.59.253 UDP 123
Nov 15 06:08:24 ip-172-31-59-253 ntpd[29960]: Listen normally on 4 eth0 fe80::10a5:e8ff:fec6:98a2 UDP 123
Nov 15 06:08:24 ip-172-31-59-253 ntpd[29960]: Listen normally on 5 lo ::1 UDP 123
Nov 15 06:08:24 ip-172-31-59-253 ntpd[29960]: Listening on routing socket on fd #22 for interface updates
Nov 15 06:08:25 ip-172-31-59-253 ntpd[29960]: 0.0.0.0 c016 06 restart
Nov 15 06:08:25 ip-172-31-59-253 ntpd[29960]: 0.0.0.0 c012 02 freq_set kernel 0.000 PPM
Nov 15 06:08:25 ip-172-31-59-253 ntpd[29960]: 0.0.0.0 c011 01 freq_not_set
Nov 15 06:08:25 ip-172-31-59-253 ntpd[29960]: 0.0.0.0 c614 04 freq_mode
Nov 15 06:30:49 ip-172-31-59-253 ntpd[29960]: 0.0.0.0 0612 02 freq_set kernel -14.957 PPM
Nov 15 06:30:49 ip-172-31-59-253 ntpd[29960]: 0.0.0.0 0615 05 clock_sync

NSCD
● nscd.service - Name Service Cache Daemon
   Loaded: loaded (/usr/lib/systemd/system/nscd.service; enabled; vendor preset: disabled)
   Active: active (running) since Tue 2016-11-15 06:09:37 UTC; 21min ago
 Main PID: 29987 (nscd)
   CGroup: /system.slice/nscd.service
           └─29987 /usr/sbin/nscd

Nov 15 06:09:37 ip-172-31-59-253 nscd[29987]: 29987 monitoring directory `/etc` (2)
Nov 15 06:09:37 ip-172-31-59-253 nscd[29987]: 29987 monitoring file `/etc/resolv.conf` (5)
Nov 15 06:09:37 ip-172-31-59-253 nscd[29987]: 29987 monitoring directory `/etc` (2)
Nov 15 06:09:37 ip-172-31-59-253 nscd[29987]: 29987 monitoring file `/etc/services` (6)
Nov 15 06:09:37 ip-172-31-59-253 nscd[29987]: 29987 monitoring directory `/etc` (2)
Nov 15 06:09:37 ip-172-31-59-253 nscd[29987]: 29987 disabled inotify-based monitoring for file `/etc/netgroup': No such file or directory
Nov 15 06:09:37 ip-172-31-59-253 nscd[29987]: 29987 stat failed for file `/etc/netgroup'; will try again later: No such file or directory
Nov 15 06:09:37 ip-172-31-59-253 nscd[29987]: 29987 Access Vector Cache (AVC) started
Nov 15 06:09:37 ip-172-31-59-253 systemd[1]: Started Name Service Cache Daemon.
Nov 15 06:09:56 ip-172-31-59-253 nscd[29987]: 29987 checking for monitored file `/etc/netgroup': No such file or directory

Swappiness:
1

THP
HugePages_Total:       0

Host lookup
ip-172-31-59-253.ec2.internal has address 172.31.59.253
253.59.31.172.in-addr.arpa domain name pointer ip-172-31-59-253.ec2.internal.

Network Info:
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 9001
        inet 172.31.59.253  netmask 255.255.240.0  broadcast 172.31.63.255
        inet6 fe80::10a5:e8ff:fec6:98a2  prefixlen 64  scopeid 0x20<link>
        ether 12:a5:e8:c6:98:a2  txqueuelen 1000  (Ethernet)
        RX packets 101717  bytes 142536014 (135.9 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 57290  bytes 4811236 (4.5 MiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 0  (Local Loopback)
        RX packets 78  bytes 7572 (7.3 KiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 78  bytes 7572 (7.3 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0


FSTab:

#
# /etc/fstab
# Created by anaconda on Mon Feb 22 17:08:22 2016
#
# Accessible filesystems, by reference, are maintained under '/dev/disk'
# See man pages fstab(5), findfs(8), mount(8) and/or blkid(8) for more info
#
UUID=ef6ba050-6cdc-416a-9380-c14304d0d206 /                       xfs     defaults,noatime        0 0

Free Space:
Filesystem      Size  Used Avail Use% Mounted on
/dev/xvda1      100G  1.4G   99G   2% /
devtmpfs        7.3G     0  7.3G   0% /dev
tmpfs           7.2G     0  7.2G   0% /dev/shm
tmpfs           7.2G   25M  7.2G   1% /run
tmpfs           7.2G     0  7.2G   0% /sys/fs/cgroup
tmpfs           1.5G     0  1.5G   0% /run/user/1000
tmpfs           1.5G     0  1.5G   0% /run/user/0
