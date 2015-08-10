# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

	# Box
	config.vm.box = "hashicorp/trusty32"
	
	#IP
	config.vm.network "private_network", ip: "192.168.11.100"

	# Ports
	config.vm.network "forwarded_port", guest: 80, host: 8000
	config.vm.network "forwarded_port", guest: 3000, host: 3000

	# Shared folder
	config.vm.synced_folder "android-sdk-linux/", "/usr/bin/android-sdk-linux", create: true   
	config.vm.synced_folder "./data", "/vagrant_data", create: true

end