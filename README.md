# How to Install Percona XtraDB Cluster on CentOS 7 with Ansible

1. Download the VagrantFile.

2. Vagrant up

3. Download project https://github.com/marandalucas/ansible-cluster-percona-centos7

4. Use the next commandline:

ansible-playbook database.yml -i enviro/lab/hosts --tags installation
ansible-playbook database.yml -i enviro/lab/hosts --tags configuration

You can see more in:
https://www.howtoforge.com/tutorial/how-to-install-percona-xtradb-cluster-on-centos-7/
