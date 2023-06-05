# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.hostmanager.enabled = true
  config.hostmanager.manage_host = true

  config.vm.define "jenkins" do |jenkins|
    jenkins.vm.box = "ubuntu/focal64"
    jenkins.vm.hostname = "jenkins"
    jenkins.vm.network "public_network" #bridged
    jenkins.vm.network "private_network", ip: "192.168.1.10"
    jenkins.vm.provider "virtualbox" do |vb|
      vb.memory = 2048
    end
  end
  config.vm.define "nginx" do |nginx|
    nginx.vm.box = "ububtu/focal64"
    nginx.vm.hostname = "nginx"
    nginx.vm.network "public_network" #bridged
    nginx.vm.network "private_network", ip: "192.168.1.20"
    nginx.vm.provider "virtualbox" do |vb|
      vb.memory = 2048
    end
  end
end
