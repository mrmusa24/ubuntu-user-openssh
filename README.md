# ubuntu-user-openssh
user name and password

#
--
sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config &&  systemctl restart ssh
--
