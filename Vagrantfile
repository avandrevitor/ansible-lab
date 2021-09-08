# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.box_check_update = false
  config.vm.provider :virtualbox

  config.vm.define "metallica" do |one|
    one.vm.hostname = "metallica"
    one.vm.network "private_network", ip: "192.168.50.20"
    one.vm.provider "virtualbox" do |v|
        v.memory = 512
        v.cpus = 1
    end
  end

  config.vm.define "bloodywood" do |two|
      two.vm.hostname = "bloodywood"
      two.vm.network "private_network", ip: "192.168.50.30"
      two.vm.provider "virtualbox" do |v|
          v.memory = 512
          v.cpus = 1
      end
  end

  config.vm.define "disturbed" do |three|
      three.vm.hostname = "disturbed"
      three.vm.network "private_network", ip: "192.168.50.40"
      three.vm.provider "virtualbox" do |v|
          v.memory = 512
          v.cpus = 1
      end
  end

  config.vm.define "stonesour" do |four|
      four.vm.hostname = "stonesour"
      four.vm.network "private_network", ip: "192.168.50.50"
      four.vm.provider "virtualbox" do |v|
          v.memory = 512
          v.cpus = 1
      end
  end

  config.vm.provision "shell",
    inline: "sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/g' /etc/ssh/sshd_config && systemctl reload sshd",
    privileged: true

end