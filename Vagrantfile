# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"                                                  # first change

  config.vm.network "private_network", ip: "192.168.56.99"                          # second change

  config.vm.network "public_network"                                                # third change

  config.vm.provider "virtualbox" do |vb|                                           # fourth change
    # Display the VirtualBox GUI when booting the machine
    vb.gui = true

    # Customize the amount of memory on the VM:
    vb.memory = "1024"                                                              # change as per need
  end
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install sl -y                                                           # use -y to make it noninteractive
  SHELL
end
