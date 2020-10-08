docker pull centos:8
yum groupinstall "Development Tools"
yum install perf
yum install cmake
yum install vim 
yum install openssh*


yum install passwd -y

修改密码
passwd

ssh-keygen -t rsa -f /etc/ssh/ssh_host_rsa_key
ssh-keygen -t rsa -f /etc/ssh/ssh_host_ecdsa_key
ssh-keygen -t rsa -f /etc/ssh/ssh_host_ed25519_key

docker commit c0f87b31249a sshd:centos


# cat /run.sh 
#!/bin/bash
/usr/sbin/sshd -D

docker run -p 8022:22 -d sshd:centos /run.sh


yum install rsync
