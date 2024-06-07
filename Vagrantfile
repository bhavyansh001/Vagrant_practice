# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "the_website" do |the_website|
    the_website.vm.box = "ubuntu/focal64"
    the_website.vm.hostname = "the_website"
    the_website.vm.network "private_network", ip: "192.168.56.42"
  end

  config.vm.define "service_A" do |service_A|
    service_A.vm.box = "ubuntu/focal64"
    service_A.vm.hostname = "service_A"
    service_A.vm.network "private_network", ip: "192.168.56.43"
  end

  config.vm.define "service_B" do |service_B|
      service_B.vm.box = "ubuntu/focal64"
      service_B.vm.hostname = "service_B"
      service_B.vm.network "private_network", ip: "192.168.56.44"
    end

  config.vm.define "database" do |database|
    database.vm.box = "ubuntu/focal64"
    database.vm.hostname = "database"
    database.vm.network "private_network", ip: "192.168.56.44"
    database.vm.provision "shell", inline: <<-SHELL
      apt install -y wget unzip mariadb-server -y
      systemctl start mariadb
    SHELL
  end
end
