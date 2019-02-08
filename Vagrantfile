# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "vagrant_machine"

  #config.vm.network :private_network, ip: "192.168.1.20"
  config.vm.network :forwarded_port, guest: 5001, host: 5010
  config.vm.network :forwarded_port, guest: 22, host: 2259

  # Forward X11
  #config.ssh.forward_x11 = true
  config.ssh.host = "192.168.1.16"
  config.ssh.username = "vagrant" # because of bug in Windows
  config.ssh.password = "vagrant" # version vagrant?
  config.ssh.insert_key = false   # 

 ## Using NFS as it has much better performance
 ## On linux install nfs-kernel-server, MacOS works by default
 ## Will ask for root password to set some things up
 config.vm.synced_folder ".", "/vagrant", :nfs => true
end
