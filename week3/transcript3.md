## Transcript Output After Deleting /etc/ssh/sshd_config

ubuntu@ip-10-0-1-84:/etc/puppet$ sudo rm /etc/ssh/sshd_config
ubuntu@ip-10-0-1-84:/etc/puppet$ sudo puppet apply -t --modulepath=/etc/puppet/code/modules /etc/puppet/manifests/site.pp
Notice: Compiled catalog for ip-10-0-1-84.us-west-2.compute.internal in environment production in 0.38 seconds
Info: Applying configuration version '1563228664'
Notice: /Stage[main]/Sshd/File[/etc/ssh/sshd_config]/ensure: defined content as '{md5}203e9b92fe3623aeba277ee44297f7dd'
Info: /Stage[main]/Sshd/File[/etc/ssh/sshd_config]: Scheduling refresh of Service[sshd]
Info: /Stage[main]/Sshd/File[/etc/ssh/sshd_config]: Scheduling refresh of Service[sshd]
Notice: /Stage[main]/Sshd/Service[sshd]: Triggered 'refresh' from 2 events
Notice: Applied catalog in 0.17 seconds
ubuntu@ip-10-0-1-84:/etc/puppet$ ls /etc/ssh/sshd_config
/etc/ssh/sshd_config
