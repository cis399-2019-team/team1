## Transcript Output After Deleting .ssh/authorized_keys in instance karmstr7_1

ubuntu@ip-10-0-1-84:/etc/puppet$ rm /home/ubuntu/.ssh/authorized_keys                                 ubuntu@ip-10-0-1-84:/etc/puppet$ sudo puppet apply -t --modulepath=/etc/puppet/code/modules /etc/puppet/manifests/site.pp
Notice: Compiled catalog for ip-10-0-1-84.us-west-2.compute.internal in environment production in 0.36 seconds
Info: Applying configuration version '1563228966'
Notice: /Stage[main]/Sshd/Ssh_authorized_key[karmstr7_1]/ensure: created
Notice: /Stage[main]/Sshd/Ssh_authorized_key[manhimf_key]/ensure: created
Notice: Applied catalog in 0.09 seconds
