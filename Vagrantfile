# -*- mode: ruby -*-
# vi: set ft=ruby :

# Create 3 VM 


Vagrant.configure("2") do |config| 

  config.vm.define "web01" do |web| 
    web.vm.box = "ubuntu/focal64"
    web.vm.network "private_network", ip: "192.168.56.10" 
    web.vm.network "public_network", bridge: "wlo1" 
  end

  config.vm.define "db01" do |db|
    db.vm.box = "ubuntu/focal64"
    db.vm.network "private_network", ip: "192.168.56.11"
    db.vm.network "public_network", bridge: "wlo1"
    db.vm.provision "shell", path: "db01_prov.sh"

  end

  config.vm.define "mon01" do |mon|
    mon.vm.box = "ubuntu/focal64"
    mon.vm.network "private_network", ip: "192.168.56.12"
    mon.vm.network "public_network", bridge: "wlo1"
  end

end
