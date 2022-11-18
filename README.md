# easy_install_erpnext--13
## Erpnext Easy install in Ubuntu 22.04
This installation was the easiest install that I ever did on Ubuntu Server. 
I configured VM on Vmware with 2 vCPUs , 8GB RAM and 100GB Disk.


# Here is a step by step guide to install ERPNext on Ubuntu 20.04

sudo apt update && sudo apt -y upgrade -y

It is recommended to reboot your system whenever you do upgrade:

sudo reboot

# Create New Account in Ubuntu and Add to Sudoers List
To create a new account I will be using erpnext as a user account so follow the below code

sudo adduser [username]

Add the erpnext user to sudoerlist.

sudo usermod -aG sudo [username]

Now switch user to

su - [username]

Run below command

export LC_ALL=C.UTF-8

# Now download the Installation Script

wget https://raw.githubusercontent.com/
