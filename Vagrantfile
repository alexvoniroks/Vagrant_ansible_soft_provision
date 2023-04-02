# -*- mode: -*-
# vi: set ft-ruby :
# VM A
Vagrant.configure("2") do |config|
  config.vm.define "vm-a" do |a|
    a.vm.box = "ubuntu/focal64"
    a.vm.hostname = "vm-a"
    a.vm.network "public_network", ip: "192.168.50.25"
    a.vm.network "private_network", ip: "192.168.100.10"
    a.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook_a.yml"
    end
  end


# VM B

  config.vm.define "vm-b" do |b|
    b.vm.box = "ubuntu/focal64"
    b.vm.hostname = "vm-b"
    b.vm.network "private_network", ip: "192.168.101.5"
    b.vm.network "private_network", ip: "192.168.100.20"
    b.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook_b.yml"
    end
  end


# VM C

  config.vm.define "vm-c" do |c|
    c.vm.box = "ubuntu/focal64"
    c.vm.hostname = "vm-c"
    c.vm.network "public_network", ip: "192.168.100.30"
    c.vm.network "private_network", ip: "192.168.102.5"
    c.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook_c.yml"
    end
  end
end
