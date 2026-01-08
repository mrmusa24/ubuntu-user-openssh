# ubuntu-user-openssh
user name and password

#
--
sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config &&  systemctl restart ssh
--
#
#If sshd install nai hole (1-line install + start)
CentOS 7:
yum install -y openssh-server && systemctl enable sshd && systemctl start sshd

CentOS Stream/8/9:
dnf install -y openssh-server && systemctl enable sshd && systemctl start sshd


Jodi original sed style e chai (SSHD file thakle only)
sed -i 's/^#\?PermitRootLogin.*/PermitRootLogin yes/' /etc/ssh/sshd_config && systemctl restart sshd


Chaile ekbar ei output dao:
rpm -qa | grep openssh

Tahole 100% perfect diye dibo.
