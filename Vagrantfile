# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.network :private_network, ip: '192.168.99.99'
  config.vm.provision :ansible do |ansible|
    ansible.playbook = 'playbook.yml'
  end

  config.vm.provider :virtualbox do |v|
    v.memory = 8192
    v.cpus = 4
  end
end
