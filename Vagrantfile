# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://atlas.hashicorp.com/search.

## Used ubuntu/xennial cause NodeRed suggested it so
  config.vm.box = "ubuntu/xenial64"
##Publiqué un port forward de la maquina virtual  haia 1880
  config.vm.network "forwarded_port", guest: 1880, host: 1880
##Ansible Integration
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "nodered/playbook.yml"
  end
end
