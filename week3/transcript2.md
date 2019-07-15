## Transcript Output After Stopping SSHD

ubuntu@ip-10-0-1-84:/etc/puppet$ sudo service sshd stop
ubuntu@ip-10-0-1-84:/etc/puppet$ service sshd status
● ssh.service - OpenBSD Secure Shell server
   Loaded: loaded (/lib/systemd/system/ssh.service; enabled; vendor preset: enabled)
   Active: inactive (dead) since Mon 2019-07-15 22:08:42 UTC; 6s ago
  Process: 8397 ExecStart=/usr/sbin/sshd -D $SSHD_OPTS (code=exited, status=0/SUCCESS)
 Main PID: 8397 (code=exited, status=0/SUCCESS)

Jul 15 22:06:21 ip-10-0-1-84 systemd[1]: Starting OpenBSD Secure Shell server...
Jul 15 22:06:21 ip-10-0-1-84 sshd[8397]: Server listening on 0.0.0.0 port 22.
Jul 15 22:06:21 ip-10-0-1-84 sshd[8397]: Server listening on :: port 22.
Jul 15 22:06:21 ip-10-0-1-84 systemd[1]: Started OpenBSD Secure Shell server.
Jul 15 22:08:42 ip-10-0-1-84 systemd[1]: Stopping OpenBSD Secure Shell server...
Jul 15 22:08:42 ip-10-0-1-84 sshd[8397]: Received signal 15; terminating.
Jul 15 22:08:42 ip-10-0-1-84 systemd[1]: Stopped OpenBSD Secure Shell server.
ubuntu@ip-10-0-1-84:/etc/puppet$ sudo puppet apply -t --modulepath=/etc/puppet/code/modules /etc/puppet/manifests/site.pp
Notice: Compiled catalog for ip-10-0-1-84.us-west-2.compute.internal in environment production in 0.43 seconds
Info: Applying configuration version '1563228548'
Notice: /Stage[main]/Sshd/Service[sshd]/ensure: ensure changed 'stopped' to 'running'
Info: /Stage[main]/Sshd/Service[sshd]: Unscheduling refresh on Service[sshd]
Notice: Applied catalog in 0.35 seconds
ubuntu@ip-10-0-1-84:/etc/puppet$ service sshd status
● ssh.service - OpenBSD Secure Shell server
   Loaded: loaded (/lib/systemd/system/ssh.service; enabled; vendor preset: enabled)
   Active: active (running) since Mon 2019-07-15 22:09:09 UTC; 4s ago
  Process: 8658 ExecStartPre=/usr/sbin/sshd -t (code=exited, status=0/SUCCESS)
 Main PID: 8668 (sshd)
    Tasks: 1 (limit: 547)
   CGroup: /system.slice/ssh.service
           └─8668 /usr/sbin/sshd -D

Jul 15 22:09:09 ip-10-0-1-84 systemd[1]: Starting OpenBSD Secure Shell server...
Jul 15 22:09:09 ip-10-0-1-84 sshd[8668]: Server listening on 0.0.0.0 port 22.
Jul 15 22:09:09 ip-10-0-1-84 sshd[8668]: Server listening on :: port 22.
Jul 15 22:09:09 ip-10-0-1-84 systemd[1]: Started OpenBSD Secure Shell server.
