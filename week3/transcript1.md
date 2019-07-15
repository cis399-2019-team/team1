## Transcript Output After Removing the sshd package

ubuntu@ip-10-0-1-84:/etc/puppet$ sudo apt-get remove openssh-server
Reading package lists... Done
Building dependency tree
Reading state information... Done
The following packages will be REMOVED:
  openssh-server
0 upgraded, 0 newly installed, 1 to remove and 0 not upgraded.
After this operation, 898 kB disk space will be freed.
Do you want to continue? [Y/n]
(Reading database ... 90679 files and directories currently installed.)
Removing openssh-server (1:7.6p1-4ubuntu0.3) ...
Processing triggers for man-db (2.8.3-2ubuntu0.1) ...
ubuntu@ip-10-0-1-84:/etc/puppet$ cd ../
ubuntu@ip-10-0-1-84:/etc$ cd puppet
ubuntu@ip-10-0-1-84:/etc/puppet$ sudo puppet apply --modulepath=/etc/puppet/code/modules /etc/puppet/manifests/site.pp
Notice: Compiled catalog for ip-10-0-1-84.us-west-2.compute.internal in environment production in 0.46 seconds
Notice: /Stage[main]/Sshd/Package[openssh-server]/ensure: created
Notice: Applied catalog in 5.16 seconds
ubuntu@ip-10-0-1-84:/etc/puppet$ service sshd status
● ssh.service - OpenBSD Secure Shell server
   Loaded: loaded (/lib/systemd/system/ssh.service; enabled; vendor preset: enabled)
   Active: active (running) since Mon 2019-07-15 22:04:38 UTC; 58s ago
 Main PID: 7740 (sshd)
    Tasks: 1 (limit: 547)
   CGroup: /system.slice/ssh.service
           └─7740 /usr/sbin/sshd -D

Jul 15 22:04:38 ip-10-0-1-84 systemd[1]: Starting OpenBSD Secure Shell server...
Jul 15 22:04:38 ip-10-0-1-84 sshd[7740]: Server listening on 0.0.0.0 port 22.
Jul 15 22:04:38 ip-10-0-1-84 sshd[7740]: Server listening on :: port 22.
Jul 15 22:04:38 ip-10-0-1-84 systemd[1]: Started OpenBSD Secure Shell server.
ubuntu@ip-10-0-1-84:/etc/puppet$ sudo apt-get remove openssh-server
Reading package lists... Done
Building dependency tree
Reading state information... Done
The following packages will be REMOVED:
  openssh-server
0 upgraded, 0 newly installed, 1 to remove and 0 not upgraded.
After this operation, 898 kB disk space will be freed.
Do you want to continue? [Y/n]
(Reading database ... 90679 files and directories currently installed.)
Removing openssh-server (1:7.6p1-4ubuntu0.3) ...
Processing triggers for man-db (2.8.3-2ubuntu0.1) ...
ubuntu@ip-10-0-1-84:/etc/puppet$ service sshd status
Unit sshd.service could not be found.
ubuntu@ip-10-0-1-84:/etc/puppet$ sudo puppet apply -t --modulepath=/etc/puppet/code/modules /etc/puppet/manifests/site.pp
Notice: Compiled catalog for ip-10-0-1-84.us-west-2.compute.internal in environment production in 0.37 seconds
Info: Applying configuration version '1563228378'
Notice: /Stage[main]/Sshd/Package[openssh-server]/ensure: created
Notice: Applied catalog in 4.63 seconds
ubuntu@ip-10-0-1-84:/etc/puppet$ service sshd status
● ssh.service - OpenBSD Secure Shell server
   Loaded: loaded (/lib/systemd/system/ssh.service; enabled; vendor preset: enabled)
   Active: active (running) since Mon 2019-07-15 22:06:21 UTC; 12s ago
 Main PID: 8397 (sshd)
    Tasks: 1 (limit: 547)
   CGroup: /system.slice/ssh.service
           └─8397 /usr/sbin/sshd -D

Jul 15 22:06:21 ip-10-0-1-84 systemd[1]: Starting OpenBSD Secure Shell server...
Jul 15 22:06:21 ip-10-0-1-84 sshd[8397]: Server listening on 0.0.0.0 port 22.
Jul 15 22:06:21 ip-10-0-1-84 sshd[8397]: Server listening on :: port 22.
Jul 15 22:06:21 ip-10-0-1-84 systemd[1]: Started OpenBSD Secure Shell server.
