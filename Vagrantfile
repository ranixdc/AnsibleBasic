# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|

# Ansible server to be build on Ubuntu 14.04
  config.vm.define "ansible" do |ansible|
    ansible.vm.box = "ubuntu/trusty64"
    ansible.vm.hostname = "ansible"
    ansible.vm.network "private_network", ip: "10.1.1.1"
  end

# Web01 Server - Ubuntu 14.04
  config.vm.define "web01" do |web01|
    web01.vm.box = "ubuntu/trusty64"
    web01.vm.hostname = "web01"
    web01.vm.network = "private_network", ip: "10.1.1.11"
    web01.vm.network = "forwarded_port", guest: 80, host:8080
  end

# db01 Server - Rhel CentOS
  config.vm.define "db01" do |db01|
    db01.vm.box = "nrel/CentOS-6.5-x86_64"
    db01.vm.hostname = "db01"
    db01.vm.network = "private_network", ip: "10.1.1.21"
  end
end
