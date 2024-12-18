# ubuntu-user-openssh
user name and password
Step 1: Install OpenSSH Server
First, you need to install the OpenSSH server package if it’s not already installed:

bash
sudo apt update
sudo apt install openssh-server
Step 2: Start and Enable the SSH Service
Start the SSH service and enable it to run at boot:

bash
sudo systemctl start ssh
sudo systemctl enable ssh
Step 3: Configure SSH (Optional)
You can configure SSH by editing the SSH configuration file:

bash
sudo nano /etc/ssh/sshd_config
Ensure PermitRootLogin is set to no to enhance security.

To allow password authentication, ensure the following line is set:

config
PasswordAuthentication yes
Step 4: Create a New User
Create a new user account that you can use to log in via SSH:

bash
sudo adduser newusername
Replace newusername with your desired username. Follow the prompts to set a password and other user information.

Step 5: Add User to sudo Group (Optional)
If you want the new user to have administrative privileges, add them to the sudo group:

bash
sudo usermod -aG sudo newusername
Step 6: Open Port 22 in UFW Firewall
Ensure that the firewall allows SSH connections:

bash
sudo ufw allow ssh
sudo ufw allow 22/tcp
sudo ufw enable
sudo ufw status
You should see an entry allowing SSH connections on port 22.
