# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
    config.vm.box = "Markard/base-homestead"

    config.vm.box_check_update = true
    config.vm.box_version = "=0.0.1"

    config.vm.network "private_network", ip: "192.168.10.10"

    config.vm.synced_folder "/var/www", "/var/www/"
    config.vm.synced_folder "/var/php", "/var/php/"

    config.vm.provider "virtualbox" do |vb|
        vb.name = "base_homestead"
        vb.gui = false
        vb.memory = "1024"
        vb.cpus = "2"
        vb.customize ["modifyvm", :id, "--cpuexecutioncap", "90"]
    end
end
