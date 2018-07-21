# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  
  # Load box from local file. In case of using local file comment configuation
  # for loading dvb box from remote host.
  # config.vm.box = "docksal_virtual_box.box"
  # You can download box from:
  # - https://drive.google.com/uc?id=1Wq8DQEw6imgnbUSJpHszkcLtCGP2P4lg&export=download

  # Load dvb box from remote host.
  # config.vm.box = 'docksal-virtual-box'
  config.vm.box_download_checksum_type='sha256'
  config.vm.box_download_checksum='588f6d0f442af181b35a2d61abe35eb3097d51482255ec854d051acb4db0ccfe'
  config.vm.box_url = 'https://www.dropbox.com/s/0pgii9uo4z3lnu7/docksal_virtual_box-v0.2.box?dl=1'

  # Setting hostname.
  config.vm.hostname = "docksal-xenial64"

  # To resize box install plugin
  # > vagrant plugin install vagrant-disksize
  # and uncomment line bellow. Important: it is possible to increase only.
  # config.disksize.size = '40GB'

  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  # config.vm.box_check_update = false

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # NOTE: This will enable public access to the opened port
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine and only allow access
  # via 127.0.0.1 to disable public access
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  config.vm.network "private_network", ip: "192.168.33.100"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
    # vb.gui = true

    # Customize the amount of memory on the VM:
    vb.memory = "4096"

    # Customize the number of CPU on the VM:
    vb.cpus = 2

    # VM is modified to have a host CPU execution cap of 50%.
    # v.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]

    # Setting VB name. Define vb name.
    vb.name = "docksal_virtual_box_dev"
  end

  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
end
