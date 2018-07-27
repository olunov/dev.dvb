# Docksal Virtual Box for Development
This box is created for working on Docksal running on Ubuntu virtual machine. The main reason
is to get performance of Linux machine on Windows OS.

# Description
That is based on ubuntu/xenial64, see original repo: https://github.com/olunov/dvb.
There is no need to re-generate box. It already exists, and uploaded to host.

# Setup
1. Setup VirtualBox and Vagrant.
2. Clone repo, go to it and run 
> vagrant up

# Resize disk.
To resize box install plugin:
> vagrant plugin install vagrant-disksize
and uncomment option config.disksize.size and set to new disk size:
config.disksize.size = '40GB'
Important: it is possible to increase only.

# Connect to Virtual Machine.
There is already setup samba server. To connect to it use ip address used in config.vm.network.
By default it is 192.168.33.100. Use username vagrant and password vagrant to connect to 'share'
folder:
\\192.168.33.100\share
It shares /www folder on virtual machine.
