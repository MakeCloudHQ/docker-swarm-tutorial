# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.hostmanager.enabled = true
  config.vbguest.auto_update = false
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "swarm.yml"
 end
  
  config.vm.define "manager1" do |manager1|
    manager1.vm.hostname = "manager1"
    manager1.vm.network "private_network", ip: "192.168.99.100"
  end

  config.vm.define "worker1" do |worker1|
    worker1.vm.hostname = "worker1"
    worker1.vm.network "private_network", ip: "192.168.99.101"
  end

  config.vm.define "worker2" do |worker2|
    worker2.vm.hostname = "worker2"
    worker2.vm.network "private_network", ip: "192.168.99.102"
  end

end
