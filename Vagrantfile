 # -*- mode: ruby -*-
# vi: set ft=ruby :
# See README.md for details

#VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(2) do |config|

  config.vm.define "cantrol"  do |ctl|
    ctl.vm.synced_folder '.', '/vagrant', disabled: true
    ctl.vm.box = "centos/7"
	ctl.vm.hostname = "centos-cantrol"
	ctl.vm.network "private_network", ip: "172.31.0.2"
	ctl.vm.provider "virtualbox" do |vb|
	  vb.memory = 2048
	end
  end 	

  config.vm.define "webserver01"  do |web01|
    web01.vm.synced_folder '.', '/vagrant', disabled: true
    web01.vm.box = "ubuntu/trusty64"
	web01.vm.hostname = "webserver01"
	web01.vm.network "private_network", ip: "172.31.0.3"
	web01.vm.provider "virtualbox" do |vb|
	  vb.memory = 1024
	end
  end 
  
  config.vm.define "webserver02"  do |web02|
    web02.vm.synced_folder '.', '/vagrant', disabled: true
    web02.vm.box = "centos/7"
	web02.vm.hostname = "webserver02"
	web02.vm.network "private_network", ip: "172.31.0.4"
	web02.vm.provider "virtualbox" do |vb|
	  vb.memory = 1024
	end
  end 
end  

