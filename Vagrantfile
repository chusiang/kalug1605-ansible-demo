# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  # Debian 8
  config.vm.define "debian8.local", primary: true do |node|
      node.vm.box = "debian/jessie64"
      node.vm.network "forwarded_port", guest: 80, host: 8080
      node.vm.provision "ansible" do |ansible|
          ansible.playbook = "setup.yml"
          ansible.sudo = true
      end
  end

  # Ubuntu 14.04
  #config.vm.define "ubuntu1404.local" do |node|
  #  node.vm.box = "ubuntu/trusty64"
  #  node.vm.provision "ansible" do |ansible|
  #    ansible.playbook = "setup.yml"
  #    ansible.sudo = true
  #  end
  #end

  # CentOS 7.2
  #config.vm.define "centos7.local" do |node|
  #    node.vm.box = "bento/centos-7.2"
  #    node.vm.provision "ansible" do |ansible|
  #        ansible.playbook = "setup.yml"
  #        ansible.sudo = true
  #    end
  #end
  
end
