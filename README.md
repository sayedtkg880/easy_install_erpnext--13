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

wget https://github.com/sayedtkg880/easy_install_erpnext--13/blob/34ecb22cad9313643a7837e678c262e4e36f01d1/install.py

Now run the Installation Script

sudo python3 install.py --verbose --production --frappe-branch version-13 --erpnext-branch version-13 --user [username]

Wait for the Installation to complete it will take time depending upon the server processor and disk speed. In my case, it took 14 minutes in total. But you need to keep monitoring it because it will ask for the password for MySQL during the installation.

Wait until you see the final line saying

# Bench + Frappe + ERPNext has been successfully installed.

Now you can validate the installation by checking the status of the frappe. Use the following command

sudo supervisorctl status all

It will show you the list of all the processes running.

# Congratulations! you have successfully installed ERPNext. Now you can open a browser and type the IP address of your server. It should work. user ID Administrator and password will be the ones that you selected during installation.
